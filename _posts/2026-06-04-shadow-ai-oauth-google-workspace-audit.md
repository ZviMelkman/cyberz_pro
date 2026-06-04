---
layout: post
title: "Shadow AI's Hidden OAuth Problem: How to Find Which AI Tools Can Reach Your Google Workspace"
date: 2026-06-04
description: "The April 2026 Vercel breach started with one employee clicking 'Allow All' on an AI tool. Here's the OAuth attack surface most small businesses can't see, and a step-by-step way to find and close it."
category: AI Security
tags: [shadow AI, OAuth, Google Workspace, Microsoft 365, third-party risk, AI security, SMB]
image: /blog/images/shadow-ai-oauth-cover.png
author: CyberZ
---

![Shadow AI's Hidden OAuth Problem: one employee, one "Allow All" click, unlimited days of access.](/blog/images/shadow-ai-oauth-cover.png)

On April 19, 2026, Vercel, the cloud platform behind the popular Next.js framework, disclosed that attackers had reached its internal systems. The intrusion did not start with a stolen password or an unpatched server. It started with one employee, months earlier, clicking a button.

That employee had signed up for an AI productivity tool called Context.ai using their corporate Google Workspace account, and during setup granted the app "Allow All" permissions. When Context.ai was later compromised, the attacker used the stolen OAuth token tied to that grant to step into Vercel's Google Workspace, then pivot into internal environments and pull environment variables, API keys, and GitHub and NPM tokens. Vercel confirmed the chain in its own security bulletin, and the incident was reported by Dark Reading, The Hacker News, and Help Net Security.

Here is the part that should keep a small business owner up at night: nothing about that attack required Vercel-scale infrastructure to go wrong. The weak point was a single OAuth grant that no one was watching. Your firm almost certainly has several.

## The breach that "logged in" instead of breaking in

The Context.ai compromise itself traces back further. According to a Hudson Rock analysis cited by The Hacker News, a Context.ai employee was infected with Lumma Stealer malware in February 2026, harvesting corporate credentials. Context.ai disclosed a March 2026 incident involving unauthorized access to its AWS environment, and it later emerged that OAuth tokens for some users were stolen too. One of those tokens belonged to the Vercel employee.

The mechanics matter, because they explain why traditional defenses missed it.

![The four-hop chain: an infostealer hits an AI vendor's employee, the attacker steals OAuth tokens, a token opens the customer's Google Workspace, and internal systems, keys and tokens are exposed.](/blog/images/shadow-ai-oauth-chain.png)

No one phished a Vercel employee. No malware ran on Vercel's network. The attacker held a valid token that the company itself had authorized. To most logging and endpoint tools, that activity looks like a legitimate app doing what it was permitted to do. As VentureBeat noted in its coverage, most security teams have no inventory of which AI tools their employees have granted OAuth access to, which means there is nothing to alert on in the first place.

## What "Allow All" actually hands over

When a tool asks to connect to your Google Workspace or Microsoft 365 and you approve broad permissions, you are not granting a one-time favor. You are issuing a standing credential that keeps working until someone revokes it. Depending on the scopes requested, a broad grant to a Google account can include all of the following at once.

![What one broad grant can unlock: read every file in Drive, read and send mail, contacts and directory, and calendar. No password needed, no MFA prompt, no expiry date.](/blog/images/shadow-ai-oauth-unlocks.png)

That last line is the trap. Passwords expire and rotate. MFA prompts on new logins. An OAuth grant does none of that by default. It sits there, invisible, doing exactly what it was told it could do, for as long as the tool exists, and sometimes after. That is why a stolen token is more dangerous than a stolen password.

![Password vs. live OAuth token: a stolen password triggers MFA, expires and rotates, and shows up as a login event; a live OAuth token bypasses MFA, never expires on its own, and looks like normal app activity.](/blog/images/shadow-ai-oauth-token-vs-password.png)

For a regulated small business, the compliance exposure stacks fast. A law firm employee who connects an AI meeting-notes tool with full Drive read access has potentially exposed privileged client files. A medical practice that lets a scheduling assistant read mail and calendar has created a path to protected health information that never appears in any HIPAA risk analysis, because no one knew the connection existed. The Stanford HAI AI Index reported that publicly disclosed AI security incidents rose more than 56 percent between 2023 and 2024, and the curve has steepened since. The Vercel case is simply the cleanest illustration of where the new exposure lives.

## Why this is a small-business problem specifically

Large enterprises are bad at this. Small firms are worse, for structural reasons. You do not have a security team reviewing app authorizations. Your staff sign up for AI tools the way they sign up for anything else, by clicking the fastest path through setup, which is almost always "sign in with Google" followed by approving whatever the app requests.

Meanwhile the number of tools is exploding. Every week brings another AI assistant that wants to plug into your inbox, your documents, or your calendar to be helpful. CrowdStrike's chief technology officer made the point bluntly at the RSAC 2026 conference: organizations should not hand an AI agent blanket access simply because limiting it is more work. Forrester analyst Jeff Pollard framed the Vercel breach as a reminder that AI tool permissions are a third-party risk problem, not a novelty. The result is an attack surface that grows on its own, that no one is inventorying, and that your existing controls were never designed to see.

## How to find what's connected (the part you can do this week)

You cannot govern what you cannot see, so the first job is discovery. The good news is that both major platforms expose this information directly. You do not need a product to start. You need an hour and a checklist.

![Where third-party AI access hides: Google Workspace admin console under Security and API controls; the per-user Google account security page; the Microsoft Entra admin center; and the per-user myapps.microsoft.com page.](/blog/images/shadow-ai-oauth-where-it-hides.png)

For each connected app, ask three questions: What is it? Who approved it, and is it still in use? And what can it actually reach? An AI tool with read access to all of Drive or full mailbox access is the highest-priority review, regardless of how trusted the vendor seems. Vercel trusted Context.ai too. Then close the gaps in order.

![This week's checklist: pull connected apps for every account, revoke unrecognized apps, flag AI tools with broad scopes, switch from allow-all to an allowlist, and require sign-off before connecting any new tool.](/blog/images/shadow-ai-oauth-checklist.png)

Switching to an allowlist is the highest-leverage single move, because it changes the default. Instead of every employee being able to authorize any app against company data, new connections require approval. That one configuration change would have stopped the Vercel chain at the door.

## Keeping the surface from regrowing

A one-time cleanup is not governance. The connections will reaccumulate the moment the next useful AI tool ships. Three habits keep the surface from coming back.

![Three habits after the cleanup: gate new connections behind a human decision, vet the vendor's data handling and breach posture, and review connected apps on a quarterly schedule.](/blog/images/shadow-ai-oauth-three-habits.png)

The first habit is to gate it: put a short vetting step between an employee and a standing credential, so a human decision sits in front of every new connection. The second is to vet the vendor, not just the feature, asking where the data goes, who can reach it, and what happens to it if the vendor is breached. The Vercel incident was a downstream consequence of a vendor's own employee getting infected, so your due diligence has to assume the vendor can be the weak link. The third is to review connected apps on a schedule, quarterly at minimum, the same way you would review who has keys to the building. An OAuth grant is exactly that: a key you handed out that is still working.

## The bottom line

The Vercel breach is not a story about a sophisticated zero-day. It is a story about a permission no one was tracking. The attacker did not break in; they used access the company had already granted and forgotten. Every small business running on Google Workspace or Microsoft 365 has the same gap, usually wider, because no one has ever looked. The fix starts with an hour, a list of connected apps, and the discipline to revoke what should not be there and to require approval for what comes next.

If you want a structured way to run that discovery across your business, the [Shadow AI Risk Assessment Discovery Kit](https://cyberzvi.gumroad.com/l/shadow-ai-risk-assessment) walks through finding every AI tool and connection your team has authorized, with the scope-review worksheets to triage what you find. Before approving the next tool, the [AI Vendor Due Diligence Checklist](https://cyberzvi.gumroad.com/l/ai-vendor-due-diligence-checklist) gives you the 50 questions to ask first. And if you are building the policy layer from scratch, the [AI Governance Framework for Small Business](https://cyberzvi.gumroad.com/l/ai-governance-framework-smbs) turns these one-off habits into a standing program your whole team can follow.

---

### Sources

- Vercel, April 2026 Security Incident Bulletin (vercel.com)
- Dark Reading, "Vercel Employee's AI Tool Access Led to Data Breach," April 21, 2026
- The Hacker News, "Vercel Breach Tied to Context AI Hack Exposes Limited Customer Credentials," April 22, 2026
- Help Net Security, "Vercel breached via compromised third-party AI tool," April 20, 2026
- VentureBeat, "Vercel breach exposes the OAuth gap most security teams cannot detect," April 21, 2026
- Stanford HAI, AI Index Report (AI security incident trend, 2023–2024)
