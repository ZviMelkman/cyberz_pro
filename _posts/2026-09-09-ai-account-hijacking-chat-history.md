---
layout: post
title: "AI Account Hijacking: Infostealers Are Stealing Claude Sessions, and the Chat History Is the Prize"
date: 2026-09-09
description: "In early September 2026, Anthropic warned Claude users that infostealer malware stole their logged-in sessions, letting attackers walk into accounts without a password or an MFA prompt. Coverage focused on drained usage limits. The bigger exposure for a small regulated firm is what sits inside the account: months of chat history where staff pasted client records, PHI, and contract data. What happened, why MFA never got asked, and what to do this week."
category: AI Security
tags: [AI security, AI account hijacking, infostealer malware, session hijacking, Claude, shadow AI, session cookies, MFA bypass, HIPAA, FTC Safeguards Rule, NIST 800-171, small business cybersecurity]
image: /blog/images/1-ai-account-hijacking-infostealer-hero.png
author: CyberZ
---

*Anthropic spent the past week signing Claude users out of their accounts and deleting their saved payment cards. Not because Claude was breached. Because malware on users' own computers had already stolen their logged-in sessions, and someone started spending them. If your team uses AI tools with personal logins, the part of this story that matters to you is not the drained usage limits. It is the chat history the attacker can read once inside.*

**AI account hijacking is the takeover of a ChatGPT, Claude, Gemini, or similar account by stealing the browser session cookie that proves the user is already logged in, rather than by guessing a password. Because the stolen cookie represents an authenticated session, the attacker is never asked for a password or a multi-factor authentication code. In early September 2026, Anthropic notified affected Claude users that a threat actor was doing exactly this at scale, using common infostealer malware families including Vidar, Lumma, StealC, RedLine, and Acreed on Windows, plus Atomic Stealer on a small number of Macs. Once inside, an attacker can consume the account's paid usage, and can also read everything the account holder ever typed into the chat.**

<div style="border-left:4px solid #EE4C48;background:#18181c;padding:20px 24px;margin:28px 0;border-radius:4px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;line-height:1.65;color:#e6e6e6;">
<li>Anthropic emailed affected Claude users in early September 2026: a threat actor is using common infostealer malware to steal logged-in Claude sessions and access accounts. Anthropic signed those sessions out, removed saved payment methods, and refunded charges it identified as unauthorized.</li>
<li>The malware is general-purpose, not Claude-specific. Infostealers copy saved browser passwords, cookies, and app credentials from an infected computer. Anthropic said it has no reason to believe the malware is related to Claude or installed through it.</li>
<li>A stolen session cookie bypasses MFA entirely. The attacker replays an already-authenticated session, so no password prompt and no MFA challenge ever appears. Your MFA did not fail. It was never asked.</li>
<li>The scale is not niche: Flashpoint counted 7.4 million infostealer-infected devices in the first half of 2026, up 27 percent, harvesting about 1.7 billion credentials. The top three families were Vidar, StealC, and Lumma, the same names in Anthropic's notice.</li>
<li>For a regulated small firm, the exposure is the chat history: months of prompts where staff pasted client records, PHI, financial data, or contract details into an account nobody inventories. A hijacked session reads all of it.</li>
</ul>
</div>

## What Anthropic told its users

The notice went out by email to affected customers, and one recipient shared it publicly, which is how BleepingComputer and other outlets confirmed the campaign. Anthropic said it had "recently become aware of a bad actor that is using common infostealer malware to steal Claude login sessions from people's computers, then using those login sessions to access Claude accounts and consume their usage."

The visible symptom was strange enough that users noticed on their own: usage limits that appeared to refill and then drain while the account holder was not using Claude. That was the attacker, spending the account's paid capacity.

Anthropic's response was aggressive for a consumer notice. It signed affected users out of all sessions, removed the saved payment methods so the accounts could not be charged, refunded charges it identified as unauthorized, and told victims to re-add a card only after confirming the malware was actually gone from their machines. The company also warned it may sign users out again if it sees further misuse.

Two details in the notice matter more than the rest. First, Anthropic named the malware families: Vidar, Lumma, StealC, RedLine, and Acreed on Windows, and Atomic Stealer (AMOS) on a small number of macOS devices. Second, it was explicit that this is not a Claude vulnerability: "We have no reason to believe that this malware is related to Claude, installed through Claude, or related to anything you did with Claude." The infections came the usual way, through unofficial downloads and malicious apps, and the malware scooped up everything of value on the machine. Claude sessions were simply one item in the haul that a buyer eventually decided to cash in.

## How a stolen cookie walks past your MFA

![Diagram of the session hijacking chain: infostealer infects the device, copies the authenticated browser cookie, the attacker replays the session, and no password or MFA prompt is ever triggered](/blog/images/2-ai-session-cookie-mfa-bypass-flow.png)

When you log into a web service and check "stay signed in," the service hands your browser a session cookie. That cookie is the proof, presented silently on every request, that you already authenticated. Infostealer malware copies the browser's cookie store along with saved passwords and autofill data, packages it into what the trade calls a "log," and ships it to the operator.

Whoever buys or uses that log does not log in as you. They resume being you. The service sees a valid, already-authenticated session, so there is no password prompt to fail and no MFA challenge to trip. This is why the standard advice to "turn on MFA" is necessary but not sufficient here. MFA protects the login event. Session theft skips the login event.

The scale of the supply side is documented. Flashpoint's 2026 Global Threat Intelligence Report, Midyear Edition, published August 13, 2026, counted 7.4 million devices infected with infostealers in the first half of 2026, a 27 percent increase over the prior six months, together harvesting roughly 1.7 billion credentials and identity data points, including cookies and authentication tokens. The three most prolific families in that data were Vidar, StealC, and Lumma. Those are the same names Anthropic listed. And if your office runs on Macs, the assumption of immunity is expired: KELA's State of Cybercrime 2026 report recorded macOS infostealer infections rising from under 1,000 devices in 2024 to more than 70,000 in 2025.

The Claude campaign is one buyer working one product category out of that inventory. The same logs contain sessions for banking portals, email, cloud storage, and every other AI tool your team is logged into. There is no reason to expect this stops with one vendor's accounts.

## The part the coverage missed: the chat history

Most reporting framed the damage as drained usage limits and hijacked paid capacity. For a home user, that is the damage. For a business, it is the smallest item on the invoice.

Think about what an AI account actually contains after six months of daily use. Every prompt, every pasted document, every draft, sitting in a scrollable history that the vendor helpfully preserves so users can pick up old threads. In practice, at a small firm, that history includes some mix of client names and matters, patient details typed into "summarize this intake note," financial statements pasted into "check my math on this," contract language, personnel issues, and passwords that someone pasted along with a config file without thinking.

An AI account is a data store. It never appears on the asset inventory, it is not covered by the backup policy, nobody reviews its access logs, and until last week nobody thought about who else might be reading it. A hijacked session reads all of it, silently, with no failed-login alert to tip anyone off.

We have written before about [what shadow AI use actually costs when it surfaces in a breach]({% post_url 2026-08-20-shadow-ai-breach-cost-2026 %}) and about [the transcript problem with AI meeting assistants]({% post_url 2026-08-19-ai-meeting-assistant-security-risks %}). This campaign is the collection mechanism those pieces were warning about, running live.

## What this means under HIPAA, the FTC Safeguards Rule, and NIST 800-171

If your firm is regulated, a hijacked AI account is not just an IT annoyance. It is a fact pattern your compliance obligations already speak to.

**Healthcare.** If staff pasted patient information into an AI chat and that account was accessed by an unauthorized party, you are in breach-analysis territory. The HIPAA Breach Notification Rule at 45 CFR 164.402 presumes an impermissible acquisition of unsecured PHI is a breach unless you can demonstrate a low probability of compromise, and a stranger reading the chat history is hard to argue down. This is also exactly the kind of reasonably anticipated threat your Security Rule risk analysis under 45 CFR 164.308(a)(1)(ii)(A) is supposed to surface before it happens. If AI tools are nowhere in your current risk analysis, that is the gap to close. The [HIPAA Security Risk Assessment Tool](https://payhip.com/b/vXmYA) ($57) walks that process for a small practice.

**CPA and tax firms.** Client financial data in a compromised AI account is customer information under the FTC Safeguards Rule. Your written information security program is supposed to cover where that data lives (16 CFR 314.4), and the Rule's MFA requirement at 314.4(c)(5) is the control this attack specifically routes around, which is worth saying out loud in your next program review: MFA on the login, plus endpoint protection and session hygiene, because cookies are the workaround.

**Defense contractors.** If anyone in your shop pasted CUI into a personal AI account, the problem predates the hijacking, and we covered it in [our walkthrough of AI tools and CUI compliance]({% post_url 2026-08-04-ai-tools-cui-compliance %}). A compromise of that account turns a policy violation into a potential incident with DFARS 252.204-7012 reporting questions attached. The clean answer is upstream: CUI does not go into consumer AI accounts at all, and your NIST SP 800-171 access controls under 3.1.1 only mean something if the data stays inside the boundary they protect.

## What to do this week

![Five-step checklist for locking down business AI accounts after the Claude session hijacking campaign](/blog/images/3-ai-account-security-checklist.png)

None of this requires new tooling. It requires treating AI accounts like the systems they already are.

**1. Inventory the accounts.** List every AI tool in use, including the personal accounts staff use for work. Ask directly; the answers will surprise you. Each one is now on your asset list.

**2. Audit the histories.** Have each account holder scroll their own chat history and flag anything containing client, patient, or contract data. Delete conversations that should never have existed, and turn off history retention or memory features where the tool allows it. Deletion is not a perfect control, but a shorter history is a smaller prize.

**3. Kill the sessions.** Log out of AI tools on every device, then log back in. That rotates the session and invalidates any cookie already sitting in an infostealer log. Make "log out of everything" a standing step whenever malware is found on any machine, and add AI accounts to your offboarding checklist while you are at it.

**4. Move work accounts to workspace plans.** Business tiers of the major AI tools offer SSO, admin session control, and centralized user management. The ability for an admin to revoke sessions across the team is the control this whole incident argues for. Personal accounts have none of it.

**5. Put it in the policy.** Which tools are approved, what data may and may not be entered, history settings, and who to tell when something goes wrong. If an employee's account is hijacked and the history holds client data, you want that discovered by your process, not by a regulator's question. Our [AI Acceptable Use Policy Kit](https://payhip.com/b/AKSw2) ($47) has the templates.

And the unglamorous root cause: infostealers arrive through cracked software, fake installers, and malicious downloads. Endpoint protection on every work device and a real rule against unofficial software cover the infection vector itself.

## The bottom line

The Claude campaign is a preview, not an outlier. Infostealer logs are a commodity, the logs contain AI sessions alongside everything else, and this was simply the first buyer to work that product category publicly. Anthropic's response, force-logouts and stripped payment methods, was the right move and also a signal: the vendor can protect its billing surface, but only you can protect what your people typed into the box. Treat every AI account as a data store holding whatever your team pasted into it over the past year, because that is what the attacker sees when the session loads.

## Sources

- BleepingComputer, "Anthropic warns infostealer malware is hijacking Claude sessions to drain usage," September 2026
- SecurityWeek, "Anthropic Warns Claude Users of Infostealer Malware Infections," September 2026
- Malwarebytes Labs, "Infostealers are hijacking Claude accounts at users' expense," September 2026
- Flashpoint, "2026 Global Threat Intelligence Report: Midyear Edition," August 13, 2026
- KELA, "State of Cybercrime 2026," 2026
- U.S. Department of Health and Human Services, HIPAA Breach Notification Rule, 45 CFR 164.400–414, and Security Rule, 45 CFR 164.308
- Federal Trade Commission, Standards for Safeguarding Customer Information, 16 CFR Part 314
- NIST, SP 800-171 Rev 2, Protecting Controlled Unclassified Information in Nonfederal Systems
