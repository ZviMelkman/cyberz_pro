---
layout: post
title: "Does CMMC Require Phishing-Resistant MFA? What 3.5.3 Passes, What DoW's Top 10 Asks For, and What Microsoft Counted on October 1"
date: 2026-10-08
description: "NIST SP 800-171 requirement 3.5.3 scores a push prompt and a hardware key identically. The DoW CIO's IT Top 10 tells contractors to retire SMS and push for phishing-resistant MFA, and Microsoft's October 1 report measured why: phishing started 23% of intrusions, up from 7%, and 44.6% of phishing techniques were built to work after MFA. What a small defense contractor changes this month."
category: CMMC
tags: [CMMC, NIST 800-171, 3.5.3, multifactor authentication, phishing-resistant MFA, FIDO2, passkeys, Brilliant at the Basics, DoW CIO, Microsoft Digital Defense Report, adversary-in-the-middle, AI phishing, SPRS score, SSP, defense contractors]
image: /blog/images/1-phishing-resistant-mfa-cmmc-hero.png
author: CyberZ
---

*The control that decides more CMMC scores than any other is also the one with the widest gap between what it scores and what it stops. Last week that gap got measured.*

**Phishing-resistant MFA is multifactor authentication that cannot be relayed through a fake login page, because the authenticator is cryptographically bound to the real site: FIDO2 security keys, passkeys, and PIV or CAC smart cards. NIST SP 800-171 requirement 3.5.3, the control CMMC Level 2 scores at five points, requires multifactor authentication but does not require it to be phishing-resistant. SMS codes, push approvals, and authenticator-app codes all satisfy it. The Department of War CIO's Brilliant at the Basics IT Top 10 puts phishing-resistant MFA at item 1 and tells DIB partners to move away from SMS and push. Microsoft's Digital Defense Report 2026, published October 1, reported that phishing started 23% of the intrusions its responders handled, up from 7% a year earlier, and that 44.6% of the phishing techniques it identified were adversary-in-the-middle, the kind built to work after the victim passes MFA.**

<div class="key-takeaways" style="border-left:4px solid #EE4C48;background:#15151a;padding:18px 24px;margin:28px 0;border-radius:6px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;">
<li>NIST SP 800-171 Rev 2 requirement 3.5.3 requires MFA for privileged accounts and for all network access. It names factor types, not methods. The word phishing does not appear in the requirement, its discussion, or its four assessment objectives in 800-171A. Rev 3's 03.05.03 widens the scope and still names no method.</li>
<li>Under 32 CFR 170.24, 3.5.3 is a five-point requirement with the program's only sliding scale: three points off if MFA covers remote and privileged users but not everyone, five off if it covers no one. Under 32 CFR 170.21 it cannot sit on a POA&amp;M, so a NOT MET on MFA blocks Conditional status instead of costing points. A push prompt and a hardware key score identically.</li>
<li>Item 1 of the DoW CIO's Brilliant at the Basics IT Top 10, launched July 13 and relaunched October 1 for Cybersecurity Awareness Month, tells DIB partners to require phishing-resistant MFA and move away from SMS and push. It is a campaign, not a scored requirement. The Cyber AB called it the clearest published statement of what the Department wants.</li>
<li>Microsoft's Digital Defense Report 2026 (October 1) found phishing was the initial access vector in 23% of its incident response cases, up from 7%, and that adversary-in-the-middle kits made up 44.6% of identified phishing techniques. Those kits relay a real login and a real MFA prompt, then keep the session cookie. Microsoft's own fix is passkeys and phishing-resistant MFA.</li>
<li>This month's job for a small sub: hardware keys or passkeys for every admin and every CUI mailbox, legacy authentication off, shorter sessions on CUI apps, and a 3.5.3 implementation statement in the SSP that names the method per account class. The SPRS score does not move. What the score describes does.</li>
</ul>
</div>

## What 3.5.3 requires, word for word

NIST SP 800-171 Rev 2 requirement 3.5.3 reads: use multifactor authentication for local and network access to privileged accounts and for network access to non-privileged accounts. The discussion paragraph underneath defines multifactor authentication as two or more different factors, something you know, something you have, something you are, and gives examples of each. It does not rank them.

NIST SP 800-171A, the assessment companion, breaks 3.5.3 into four objectives. 3.5.3[a]: privileged accounts are identified. 3.5.3[b]: multifactor authentication is implemented for local access to privileged accounts. 3.5.3[c]: multifactor authentication is implemented for network access to privileged accounts. 3.5.3[d]: multifactor authentication is implemented for network access to non-privileged accounts. An assessor examines the configuration, interviews the people who run it, and tests whether a login actually gets challenged. Nothing in those four objectives asks what the second factor is made of.

Rev 3 does not close the gap. Requirement 03.05.03 reads: implement multi-factor authentication for access to privileged accounts and non-privileged accounts. The scope grows, because local access to ordinary accounts now needs a second factor too. The method is still unspecified. The discussion mentions hardware authenticators and smart cards as examples of something you have, alongside the others. Examples, not a floor. CMMC still assesses against Rev 2 under 32 CFR Part 170, and the Cyber AB said at its September 30 town hall that the Rev 3 transition rule has been held in abeyance since the July 13 pause. The [Rev 2 versus Rev 3 breakdown]({% post_url 2026-06-30-nist-800-171-rev-2-vs-rev-3-cmmc %}) covers what that transition would change when it moves.

So an SMS code is MFA. A push notification is MFA. A six-digit code from an app is MFA. A FIDO2 key is MFA. As far as the standard is concerned, those are the same thing.

![Comparison card: NIST 800-171 Rev 2 requirement 3.5.3 requires MFA for admins and all network access with any factor type, while the DoW CIO's IT Top 10 item 1 asks for phishing-resistant MFA and tells contractors to move away from SMS and push, so a contractor can be MET on 3.5.3 with the exact method DoW says to retire](/blog/images/2-phishing-resistant-mfa-cmmc-353-vs-dow-top10.png)

## How 3.5.3 is scored, and why it cannot wait on a POA&M

The CMMC scoring methodology at 32 CFR 170.24 puts 3.5.3 among the requirements that cost five points when NOT MET, the tier reserved for controls whose absence could lead to significant exploitation of the network or exfiltration of CUI. It is one of only two requirements in the whole methodology that get partial credit. The rule says MFA is typically rolled out first to remote and privileged users and then to everyone else, so three points come off if MFA covers only remote and privileged users, and five points come off if it covers no one.

That is the entire scoring logic. The methodology has a column for who is covered. It has no column for how. A contractor whose every account is on SMS codes and a contractor whose every account is on hardware keys both deduct zero.

The other half of the scoring story is the POA&M rule. Under 32 CFR 170.21(a)(2)(ii), a Level 2 POA&M cannot include any requirement with a point value greater than one, with a single carve-out for FIPS-validated encryption. 3.5.3 is a five-point requirement. If it is NOT MET on assessment day, it cannot be deferred, which means there is no Conditional status to fall back on until it is fixed. The [POA&M eligibility breakdown]({% post_url 2026-06-15-cmmc-poam-eligibility-what-you-can-defer %}) lists the rest of the controls in that position.

Put the two halves together and the shape of the problem is clear. MFA is the control the program weights most heavily and refuses to let you defer. It is also the control the program measures with the least precision. Getting to MET is mandatory. Getting to defended is optional, as far as the score can tell.

![Scoring card: 3.5.3 is worth five points under 32 CFR 170.24 with partial credit of three when only admins and remote users have MFA, it cannot be placed on a POA&M under 32 CFR 170.21 so a NOT MET means no Conditional status, and SPRS scores push and passkeys the same even though only one stops phishing](/blog/images/4-phishing-resistant-mfa-cmmc-scoring-poam.png)

## What the DoW CIO's Top 10 asks for instead

On July 13, 2026, the same day the Department paused CMMC Phase 2, the DoW CIO launched Brilliant at the Basics, two Top 10 lists of cybersecurity practices for DIB partners, one for IT and one for operational technology. The IT list leads with phishing-resistant MFA. Item 1 tells contractors to upgrade their authentication to require strong phishing-resistant MFA for user accounts, and describes moving away from legacy methods such as SMS text messages or push notifications as the foundation of a modern security stack.

The list is a campaign. There is no Brilliant at the Basics score, assessment, or certificate, and nothing in 32 CFR Part 170 references it. On October 1 the CIO's office relaunched it as the Department's Cybersecurity Awareness Month theme, with four headings, Be Aware, Be Vigilant, Be Secure, Be Connected, and a promise to spend the month highlighting the no-cost services available to DIB partners that want to implement the lists. Be Vigilant is where strong authentication and anti-phishing practice sit.

The reason the list matters for a contractor planning spend is what people close to the program are saying about it. At the Cyber AB's September 30 town hall, CEO Matthew Travis called Brilliant at the Basics the clearest published statement of DoW cybersecurity priorities for the DIB, and the Cyber Education Foundation's Mike Snyder noted that most of its items crosswalk to 800-171. Travis also floated, with every slide labeled speculative and a statement that the Cyber AB has no inside information on the Reform Task Force, the idea that a partial 800-171 assessment mapped to these priorities is one direction a reformed program could take. That is not policy. The task force report is still unpublished, and Travis's own estimate for release was the back half of October at the earliest. But if a priority subset of the 110 controls is ever carved out for closer scrutiny, item 1 of the Department's own list is a reasonable guess at what sits at the top of it.

The two documents are answering different questions. 800-171 asks whether a second factor exists. The Top 10 asks whether the second factor survives a fake login page. A contractor can answer yes to the first and no to the second and be fully MET. The [Section 1532 piece]({% post_url 2026-10-06-ndaa-section-1532-ai-rules-defense-contractors %}) made the same point about item 8, the AI policy item: the Department has started publishing expectations that live outside the control set.

## Why the gap matters now: the October 1 numbers

Microsoft published its Digital Defense Report 2026 on October 1. It covers July 2025 through June 2026 and draws on the company's incident response work and threat intelligence telemetry. Three findings bear directly on 3.5.3.

First, phishing is back as a front door. In Microsoft's incident response cases, phishing was the initial access vector in 23% of intrusions, up from 7% the year before. Microsoft's Deputy General Counsel for Customer Security and Trust, writing on the company's policy blog the day the report came out, framed that number as evidence that compromised identities remain the entry point for broader attacks.

Second, the phishing has changed. Among the phishing techniques Microsoft's threat intelligence identified, adversary-in-the-middle made up 44.6%, ahead of standard URL phishing at 33.6% and attachments at 12.9%. The report says 87.7% of phishing intrusions involved credential or session harvesting, and that adversary-in-the-middle phishing and token theft more than doubled as a share of detected attacks in the first half of 2026, from a base Microsoft describes as still comparatively small.

Third, the compromise spreads. Of the intrusions that began with a valid account, 52.2% led to further credential theft.

Adversary-in-the-middle, or AiTM, is worth describing plainly because it is the reason push and SMS stopped being a control. The victim clicks a link and lands on a page that is a live proxy to the real Microsoft 365, Google, or VPN login. They type a real password. The real service sends a real MFA prompt. They approve it. The proxy sits between the two ends and keeps the session cookie the real service hands back. No factor was defeated. The login was legitimate. The attacker simply has the session now, and the user's 3.5.3[d] objective was MET at every step. Microsoft's March 2026 analysis of one such kit, Tycoon2FA, described it pushing tens of millions of messages a month at more than 500,000 organizations, with access sold for about $120.

Where AI fits is narrower than the headlines suggest, and the report is careful about it. Microsoft writes that AI lets attackers run larger campaigns, craft highly convincing personalized phishing, and automate work that used to need people. It also writes that most complex intrusions it observes still retain meaningful human direction, and it does not attribute the jump from 7% to 23% to AI-written lures. The honest version is this: AI has driven the cost of a convincing, personalized lure toward zero, and AiTM kits have removed MFA as the thing that used to catch the people who clicked. Each half was a manageable problem on its own. Together they turn push and SMS into a control that passes the assessment and fails the attack.

## Which MFA counts as phishing-resistant

CISA's October 2022 fact sheet, Implementing Phishing-Resistant MFA, is the reference most assessors and MSPs will recognize, and its hierarchy has not changed. Phishing-resistant methods are FIDO/WebAuthn authenticators and PKI-based authenticators such as PIV and CAC cards. App-based methods, meaning push approvals, number matching, and one-time codes, are better than SMS but can be phished. SMS and voice codes are the weakest tier. NIST SP 800-63B uses the term verifier impersonation resistance for the same property: the authenticator will only answer the site it was registered to, so a proxy page gets nothing it can replay.

Passkeys are FIDO2 credentials in consumer clothing, synced through a platform account or bound to a device, and they sit in the phishing-resistant tier. Windows Hello for Business, when configured with a key or certificate trust model, does the same job on a Windows endpoint. Number matching, which Microsoft began enforcing by default in 2023, defeats push fatigue attacks where a user approves prompts to make them stop. It does not defeat AiTM, because the proxy relays the number along with everything else.

For the SSP, the useful distinction is per account class and per access path, not per product. A shop can be phishing-resistant for its five admins and its CUI mailboxes while the shop-floor accounts stay on an authenticator app for another quarter. That is a defensible implementation statement. "We use MFA" is not.

![Table: SMS and voice codes, push approval with number matching, and authenticator app codes all satisfy 3.5.3 but do not stop adversary-in-the-middle phishing; FIDO2 keys, passkeys, and PIV or CAC cards satisfy 3.5.3 and are phishing-resistant per CISA](/blog/images/3-phishing-resistant-mfa-cmmc-mfa-methods-ladder.png)

## What a 12-person shop does this month

**Map the four objectives before buying anything.** List every privileged account by name. List every network access path into the CUI environment: Microsoft 365 or Google Workspace, VPN, remote desktop gateway, cloud consoles, the ERP if it is reachable from outside. For each path, confirm a login is challenged, and record what challenges it. That table is 3.5.3[a] through [d], and it is what an assessor or a DIBCAC auditor reconstructs on their own if you have not.

**Admins and mail first.** Every global, domain, and tenant admin gets a hardware key or a passkey, with a second enrolled as backup. Every mailbox that receives CUI gets the same. Microsoft Entra ships a built-in Conditional Access authentication strength called phishing-resistant MFA that enforces exactly this tier for the users and apps you scope it to. Check feature availability in your cloud, commercial, GCC, or GCC High, before writing a method into the SSP. The [GCC High piece]({% post_url 2026-09-23-do-i-need-gcc-high-for-cmmc %}) covers why that boundary matters for other reasons. Hardware keys are a line item in the tens of dollars per key.

**Turn off legacy authentication.** Basic authentication, IMAP, POP, and older SMTP paths do not prompt for a second factor at all. MFA enforced everywhere except the protocol an attacker chooses is MFA enforced nowhere. This is also where 3.5.3 bypass findings come from.

**Shorten the session.** AiTM steals a session cookie, so the length of the session is the length of the breach. Set a sign-in frequency on the apps that hold CUI, revoke sessions on risk signals if your license includes it, and make reauthentication cheap by making it a touch on a key.

**Write it into the SSP as it actually is.** The 3.5.3 implementation statement names the method per account class, the enforcement mechanism, and the exceptions still on an app code with a date to close them. The [SSP update requirements breakdown]({% post_url 2026-09-17-cmmc-ssp-update-requirements %}) covers what an authentication change does to the rest of the document, and last week's [AI-drafted SSP piece]({% post_url 2026-10-07-ai-generated-ssp-cmmc %}) covers why a statement that reads well and describes a different environment is worse than no statement at all.

**Collect the evidence while it is fresh.** The Conditional Access policy export, a screenshot of the authentication strength assignment, the registration report showing which users hold which method, and a dated test login that got challenged. That is Examine and Test for all four objectives, and it is the same packet a whistleblower's lawyer would want to see was true on the day you affirmed.

## The bottom line

NIST SP 800-171 requirement 3.5.3 is a five-point control with no POA&M path and no opinion about what kind of MFA you use. The DoW CIO's IT Top 10 has an opinion, and it put that opinion at the top of its list: phishing-resistant, and away from SMS and push. Microsoft's October 1 report is the measurement of why: phishing tripled as a share of intrusions, and the dominant phishing technique is one that works after MFA is passed. A contractor can be MET on 3.5.3 with the exact method the Department now says to retire. The score will not show the difference. The attacker will.

If the next step is rewriting the 3.5.3 statement so it names the method per account class, the [CMMC Level 2 System Security Plan (SSP) Template](https://payhip.com/b/gB6oD) ($77) has the control-by-control implementation structure. If the gap is proving it, the [CMMC Level 2 Evidence Tracker for NIST 800-171 Audit](https://payhip.com/b/LN2UB) ($67) lists the Examine, Interview, and Test artifacts for each requirement. If you are rebuilding the whole Level 2 posture around the self-assessment regime, before an affirmation deadline or a government audit forces the timeline, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) covers scoping, the SSP, the SPRS score, the POA&M, and the evidence trail in one set.

## Sources

- NIST SP 800-171 Rev 2, requirement 3.5.3, and NIST SP 800-171A, assessment objectives 3.5.3[a] through [d] (csrc.nist.gov)
- NIST SP 800-171 Rev 3, requirement 03.05.03 (csrc.nist.gov)
- 32 CFR 170.24, CMMC Scoring Methodology, paragraph (c)(2), including the partial-credit rule for IA.L2-3.5.3
- 32 CFR 170.21, Plan of Action and Milestones requirements, paragraph (a)(2)(ii)
- Department of War CIO, Brilliant at the Basics, Top 10 IT Cybersecurity Best Practices for Defense Industrial Base Partners, item 1, July 2026 (dodcio.defense.gov/BrilliantBasics)
- Department of War CIO, Cybersecurity Awareness Month launch of the Brilliant at the Basics campaign, October 1, 2026
- Cyber AB, September 2026 Town Hall, September 30, 2026, as recapped by CMMC.com
- Microsoft, Digital Defense Report 2026, published October 1, 2026, covering July 2025 through June 2026
- Microsoft On the Issues, "Preparing governments for an era of interconnected cyber risk," Mike Yeh, October 1, 2026
- Microsoft Security, analysis of the Tycoon2FA adversary-in-the-middle phishing kit, March 2026
- CISA, Implementing Phishing-Resistant MFA, fact sheet, October 2022
- NIST SP 800-63B, Digital Identity Guidelines: Authentication and Lifecycle Management, verifier impersonation resistance
