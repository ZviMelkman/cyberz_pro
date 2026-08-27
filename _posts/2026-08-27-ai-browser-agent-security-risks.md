---
layout: post
title: "AI Browser Agent Security Risks: What the Zenity Attacks Mean for a Firm That Handles Client Data"
date: 2026-08-27
description: "Zenity Labs published working zero-click attack chains against Claude in Chrome and ChatGPT Atlas on August 5, 2026. One email or one planted comment led to inbox exfiltration, permanent Google Drive access, and account takeover. Neither vendor has a patch, because there is no bug to fix. What that means for a small regulated firm, and the five controls to put in place this week."
category: AI Security
tags: [AI security, AI browser agents, prompt injection, indirect prompt injection, Claude in Chrome, ChatGPT Atlas, Zenity, agentic AI, HIPAA, NIST 800-171, small business cybersecurity]
image: /blog/images/1-ai-browser-agent-security-risks-hero.png
author: CyberZ
---

*An AI browser agent does two things at once: it reads whatever is on the page, and it acts inside every account you are already logged into. Security researchers spent this summer showing what happens when those two capabilities meet an attacker. The answer is not encouraging, and the reason there is no patch is more important than the attacks themselves.*

**An AI browser agent is an AI assistant that runs inside your browser with permission to read pages, click, type, and navigate on your behalf while using your existing logged-in sessions. Claude in Chrome, ChatGPT Atlas, and Perplexity Comet are the current examples. The security risk specific to them is indirect prompt injection: untrusted content the agent reads, such as an email, a webpage, or a comment on a public thread, contains instructions the agent cannot reliably tell apart from yours, and it carries them out with your identity and your active sessions.**

<div style="border-left:4px solid #EE4C48;background:#18181c;padding:20px 24px;margin:28px 0;border-radius:4px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;line-height:1.65;color:#e6e6e6;">
<li>On August 5, 2026, Zenity Labs published two working attack chains, presented at Black Hat USA 2026, against Claude in Chrome and ChatGPT Atlas. Both required zero clicks from the victim.</li>
<li>The Claude chain began with a single email and ended in Gmail inbox exfiltration, every Google Drive file silently shared with the attacker, and account takeover on Slack, X, and Claude.ai.</li>
<li>The Atlas chain began with one planted comment under a public X post and ended in phishing messages sent to the victim's entire WhatsApp contact list, and a separate unauthorized Amazon purchase shipped to the attacker's address.</li>
<li>Zenity reported the Claude findings on December 27, 2025. Anthropic closed the report as informative on January 27, 2026 and said it was ineligible for its disclosure program. OpenAI acknowledged the Atlas findings on February 17, 2026. As of the disclosure, neither was fixed.</li>
<li>There is no patch coming, because reading untrusted content and acting on it across authenticated sites is the product, not a defect. Anthropic's own published position is that no browser agent is immune to prompt injection.</li>
<li>For a firm handling PHI, CUI, or privileged client files, this is not a new control problem. NIST SP 800-171 Rev 2 already governs processes acting on behalf of authorized users, and the HIPAA Security Rule already requires the risk analysis to cover it.</li>
</ul>
</div>

## What Zenity Actually Demonstrated

Zenity Labs, an AI agent security firm, published its research on August 5, 2026 under the name PleaseFix, in two posts covering Claude in Chrome and ChatGPT Atlas, alongside its Black Hat USA presentation. These were not theoretical writeups. Each post shipped with video of the full chain running end to end.

Start with the Claude in Chrome chain, because it is the one that reaches furthest into a business.

![Six-step diagram of the Zenity Labs zero-click attack chain against Claude in Chrome: malicious email, summary request, package import from an attacker CDN, code execution under the user session, Gmail and Drive theft, and account takeover](/blog/images/2-ai-browser-agent-attack-chain-zenity.png)
*The Claude in Chrome chain, start to finish. Source: Zenity Labs, August 5, 2026.*

A victim receives an ordinary-looking email. The visible text is a friendly note from "John" about getting coffee. Hidden inside it are invisible text, fabricated conversation turns, and instructions embedded in an image. Nothing happens when it arrives. Nothing happens when it sits in the inbox.

The chain fires when the victim asks the agent to summarize their recent emails. The agent reads the message, encounters the injected turn structure, and cannot distinguish those instructions from the user's own. It then executes JavaScript through the extension's built-in JavaScript tool. Zenity notes this worked both in the permissive mode and in the "ask before acting" mode, because that tool executed without going through the domain approval step.

Direct malicious code gets refused by the model. So the researchers hosted their own npm package on a registry named to resemble a legitimate CDN, and had the injected instruction ask for something that looks harmless: generate a UUID. The package returns a properly formatted UUID, so nothing looks wrong to either the agent or the user, while a completely different payload runs silently underneath.

From there, everything runs inside the victim's authenticated browser session, so no credentials are needed for anything:

- The script pulls the Gmail Atom feed, parses message IDs, fetches full message bodies, and posts the inbox contents to an attacker server.
- It reverse-engineers Google Drive's internal sharing API and adds the attacker as a writer on every file in the account. Zenity's point about this step matters most: that access survives a password change, a session revocation, and a 2FA reset.
- With read access to the inbox, the attacker triggers password resets and sign-in flows on other platforms, has the agent watch Gmail for the incoming verification codes, and relays them out. Zenity demonstrated full takeover of Slack, X, and, with some irony, Claude.ai itself, which exposes prior chats, uploaded files, and every connector the user had linked.

The Atlas research took a different route to a similar place. Rather than an email, the entry point was a comment planted under a popular X post, waiting for anyone to ask their agent to do something ordinary with that thread. Zenity's framing for the underlying flaw is "intent collision": the agent has no reliable way to separate what the user asked for from what the page said, and an attacker who bridges the two gets the agent to pursue the attacker's goal while believing it is serving the user.

Two details from the Atlas work are worth carrying into any risk conversation. First, Atlas had real defenses, and most of them were classifiers making judgment calls rather than hard limits in code. Zenity found the on-page classifier evaluates roughly one screen at a time, so a payload spread thinly across scroll sections never looks bad in any single snapshot. They found the prompt-injection classifier was tuned for English, so the same instructions written in Hebrew slipped past. The confirmation gate lived in the system prompt, so a strong enough framing pre-answered it.

Second, the one boundary that held was deterministic and in code: Atlas would not click Amazon's final purchase button, and the researchers could not make it. So they routed around it. They had Atlas ask Amazon's own shopping assistant, Rufus, to place the order, and Rufus complied, because as far as it could tell it was talking to the customer. The wall never broke. It just stopped mattering.

## Why There Is No Patch Coming

This is the part most coverage skips, and it is the part that determines what you should actually do.

Zenity's disclosure timeline for the Claude research is specific. The first report went to Anthropic through HackerOne on December 27, 2025 and was closed as informative on January 27, 2026. A second report on January 12, 2026 was closed as a duplicate the next day, and on January 27, 2026 Anthropic said the report was ineligible for its Vulnerability Disclosure Program. Zenity's post states the risks persisted as of publication. For Atlas, Zenity reported to OpenAI on January 11, 2026, and OpenAI acknowledged on February 17, 2026, describing meaningful risks associated with prompt injection in agentic environments and noting that resilience to it is an active area of work.

Neither response is a brush-off, and reading it as one leads to the wrong conclusion. Anthropic published its own research on browser prompt injection in November 2025. In it, the company reports measurable improvement against an internal adaptive attacker, and then states plainly that a one percent attack success rate still represents meaningful risk and that no browser agent is immune to prompt injection. The attacker in that evaluation was given one hundred attempts per environment. Those two numbers belong next to each other in any risk assessment.

The structural issue underneath is older than any of these products. Since the 1990s the Same-Origin Policy has kept a script on one site from acting inside your session on another, which is why you can keep a bank tab and a random blog open at the same time. An agentic browser is not a script trapped in one origin. It is a single actor spanning every open tab, already authenticated everywhere you are. As Zenity puts it, that quietly hands cross-site request forgery back to attackers for free, because acting as you across origins is not a trick the attacker has to pull off. It is the design.

So there is no patch in the ordinary sense. Vendors can and do raise the cost with better training and better classifiers, and those improvements are real. But you cannot fix "the agent reads untrusted content and acts on your behalf" without removing the reason people install it.

## What This Means for a 30-Person Regulated Firm

The temptation is to file this under "interesting research about consumer tools." That reading does not survive contact with how these extensions actually get used.

Someone in your firm installed a browser agent to clear an inbox faster. That person is signed into the practice management system, the client portal, the billing platform, the shared Drive, and email, in the same browser profile, at the same time. The agent's reach is the union of everything that person can reach. It is not a sandbox. It is your most access-rich employee, with a documented inability to tell your instructions from an attacker's.

Now map that onto the frameworks you already work under.

**If you handle CUI.** NIST SP 800-171 Rev 2 control 3.1.1 limits system access to authorized users and to processes acting on behalf of authorized users. A browser agent operating with an employee's session is precisely a process acting on behalf of an authorized user, and it inherits that user's access without any of the judgment. Control 3.4.9 requires you to control and monitor user-installed software, which is exactly what a browser extension is. Neither control needed to be rewritten for AI. They already apply. We covered the boundary question in more depth in [Can You Use ChatGPT With CUI? What DFARS and CMMC Actually Require in 2026]({% post_url 2026-08-04-ai-tools-cui-compliance %}).

**If you handle PHI.** The HIPAA Security Rule risk analysis at 45 CFR 164.308(a)(1)(ii)(A) covers risks to ePHI across your whole environment, and an agent with standing access to an inbox holding patient communications is squarely in scope. Information access management at 164.308(a)(4) and access control at 164.312(a)(1) are the controls you would be evaluated against. There is also a vendor question with no comfortable answer: a browser extension acting on your workforce member's behalf is not a business associate relationship you have papered, and it is not one most practices have even inventoried. Our walkthrough of [when to update your HIPAA risk assessment]({% post_url 2026-07-27-when-to-update-hipaa-risk-assessment %}) lists the triggers OCR names, and adopting a tool with this reach is one of them.

**If you handle privileged or confidential client files.** The Drive persistence step is the one to sit with. Sharing survives the incident response most small firms would run. Resetting the password and revoking sessions, which is what everybody does, leaves the attacker's access untouched.

## Five Controls to Put in Place This Week

None of these require new software. They require a decision and a short written rule.

![Checklist of five controls for AI browser agents at a small firm: decide who may run one, keep it out of regulated tabs, use a separate browser profile, never approve a broad plan, and write it into the AI policy](/blog/images/3-ai-browser-agent-controls-small-firm.png)
*Five controls that work at a 10-to-50-person firm, no new tooling required.*

1. **Decide who is allowed to run one, by name.** Not "IT-approved tools" in the abstract. A short list of people, in writing, reviewed when someone changes role or leaves.

2. **Keep the agent out of regulated sessions.** The rule to write down: an AI browser agent does not run in a browser profile that is signed into anything holding PHI, CUI, or privileged client material. This is the single highest-value control here, because it caps the blast radius no matter what the agent reads.

3. **Use a dedicated browser profile with only the logins the task needs.** Zenity's own advice to users is to give an agentic browser as little reach as the task truly requires and to watch it while it works. A separate profile is the cheapest way to make that real.

4. **Never approve a broad plan.** The Drive step in the Claude chain worked partly because the injected instruction got a reasonable-sounding plan in front of the user, who approved it. Approve one site and one task, then close the session. Treat a request to expand scope mid-task as a stop signal.

5. **Write it into the AI acceptable use policy and inventory what is already installed.** Start with what is running today, including the tools nobody approved. Our [shadow AI breach cost breakdown]({% post_url 2026-08-20-shadow-ai-breach-cost-2026 %}) covers why unapproved tools dominate incident reports, and the [structure of a small business AI acceptable use policy]({% post_url 2026-07-07-ai-acceptable-use-policy-small-business %}) covers what the written rule needs to contain. If you would rather adapt a document than draft one, the [AI Acceptable Use Policy Kit](https://payhip.com/b/AKSw2) ($47) has the templates, including the tool-approval and browser-extension sections this situation calls for.

One more habit worth building. Before any AI feature gets switched on inside a tool you already use, ask what the vendor is doing with untrusted content and what the agent can reach. Our [AI vendor due diligence questions]({% post_url 2026-08-09-ai-vendor-due-diligence %}) cover the version of this conversation you should be having when software you already approved quietly adds an agent.

## The Bottom Line

Zenity took eight months from first report to public disclosure, and the chains still worked when they went on stage at Black Hat. That gap is not evidence of vendor negligence. It is evidence that the problem is architectural, which is worse, because architectural problems do not get closed by a Tuesday update. The vendors are being honest about this. Anthropic's published position is that no browser agent is immune to prompt injection. OpenAI called its own resilience an active area of work. Zenity's conclusion is that soft boundaries are labels, not access controls.

If you run a firm with regulated data, you do not need to ban these tools to be defensible. You need to be able to say who runs one, what it can reach, and why it cannot reach the sensitive thing. That is a week of work, and it is the same answer your existing framework was already asking for.

## Sources

- Zenity Labs, [Claude in Chrome: From alert(1) to Full Account Takeover](https://labs.zenity.io/post/claude-in-chrome-from-alert-to-full-account-takeover), August 5, 2026
- Zenity Labs, [Grand Theft Atlas](https://labs.zenity.io/post/grand-theft-atlas), August 5, 2026
- Zenity Labs, [Account Takeover via Claude in Chrome: A Technical Deep Dive](https://labs.zenity.io/post/account-takeover-via-claude-in-chrome-a-technical-deep-dive), August 2026
- Anthropic, [Mitigating the risk of prompt injections in browser use](https://www.anthropic.com/research/prompt-injection-defenses), November 24, 2025
- SecurityWeek, [Zero-Click AI Browser Hacking: Claude and ChatGPT Atlas Hijacked via Emails, X Posts](https://www.securityweek.com/zero-click-ai-browser-hacking-claude-and-chatgpt-atlas-hijacked-via-emails-x-posts/), August 6, 2026
- NIST, [SP 800-171 Rev. 2, Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations](https://csrc.nist.gov/pubs/sp/800/171/r2/upd1/final)
- HHS, [45 CFR 164.308, Administrative safeguards](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-C/part-164/subpart-C/section-164.308)
