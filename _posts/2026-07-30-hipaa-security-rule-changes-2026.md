---
layout: post
title: "HIPAA Security Rule Changes in 2026: What Actually Changed, and What Slipped to 2027"
date: 2026-07-30
description: "The HIPAA Security Rule overhaul is still a proposed rule, now targeted for July 2027. The 2026 deadline that did bind was February 16, and most coverage never mentioned it."
category: HIPAA
tags: [HIPAA, Security Rule, NPRM, Notice of Privacy Practices, 42 CFR Part 2, OCR, compliance]
image: /blog/images/1-hipaa-security-rule-changes-2026-hero.png
author: CyberZ
---

*Search "HIPAA security rule changes 2026" and page one will tell you that multi-factor authentication is now mandatory, that encryption at rest is required, and that the addressable designation has been eliminated. None of that is in force. Meanwhile the HIPAA deadline that genuinely did bind this year passed on February 16, and most of page one never mentions it.*

**There are no finalized HIPAA Security Rule changes in effect in 2026. The overhaul that most 2026 coverage describes is a Notice of Proposed Rulemaking, published January 6, 2025 at 90 FR 898 under RIN 0945-AA22, and it has not been finalized. In the Fall 2026 Unified Agenda, HHS moved it to the Long-Term Actions list and set July 2027 as its anticipated timeframe for final action, replacing an earlier May 2026 target. The current Security Rule, including the "addressable" designation at 45 CFR 164.306(d), remains unchanged and is being enforced today. Separately, a real 2026 compliance date did arrive: every HIPAA covered entity handling substance use disorder records protected by 42 CFR Part 2 owed an updated Notice of Privacy Practices by February 16, 2026.**

<div style="border-left:4px solid #EE4C48;background:#f7f7f8;padding:18px 22px;margin:28px 0;border-radius:4px;">
<strong style="display:block;margin-bottom:10px;font-size:1.05em;">Key Takeaways</strong>
<ul style="margin:0;padding-left:20px;line-height:1.7;">
<li>The Security Rule overhaul is still a <em>proposed</em> rule. HHS/OCR issued the NPRM December 27, 2024 and published it January 6, 2025 at 90 FR 898.</li>
<li>OMB's Unified Agenda now shows a final action target of July 2027 for RIN 0945-AA22, moved from May 2026, and the rulemaking sits on the Long-Term Actions list.</li>
<li>Multi-factor authentication is not named anywhere in the current Security Rule. It appears only in the proposal.</li>
<li>Encryption remains an <em>addressable</em> implementation specification at &sect; 164.312(a)(2)(iv) and &sect; 164.312(e)(2)(ii).</li>
<li>Industry expectation is a 180 to 240 day compliance window after any final rule, which would put real compliance in 2028, not 2026.</li>
<li>The HIPAA deadline that actually bound in 2026 was February 16: Part 2 substance use disorder updates to your Notice of Privacy Practices under &sect; 164.520.</li>
<li>That obligation reaches covered entities that merely receive Part 2 records. It is not limited to substance use disorder treatment programs.</li>
<li>OCR announced its Civil Enforcement Program for Confidentiality of Substance Use Disorder Patient Records on February 13, 2026 and is accepting complaints.</li>
</ul>
</div>

## What is the status of the HIPAA Security Rule update in 2026?

It is a proposal, and it is further away than it was a year ago.

HHS's Office for Civil Rights issued a Notice of Proposed Rulemaking on December 27, 2024, titled *HIPAA Security Rule To Strengthen the Cybersecurity of Electronic Protected Health Information*. It was published in the Federal Register on January 6, 2025 at 90 FR 898, under RIN 0945-AA22. The comment period closed March 7, 2025.

If finalized, it would be the first material overhaul of the Security Rule since the 2013 Omnibus Rule. It proposes to remove the addressable designation and make implementation specifications mandatory, to require multi-factor authentication, to mandate encryption of electronic protected health information at rest and in transit, to require annual technology asset inventories and network maps, to require vulnerability scanning twice a year and annual penetration testing, and to impose a 72-hour restoration requirement for critical systems.

None of that is law.

OCR's regulatory agenda originally pointed at May 2026 for final action. That month came and went without a final rule. In the Fall 2026 Unified Agenda, HHS moved RIN 0945-AA22 to its Long-Term Actions list and identified July 2027 as the anticipated timeframe for final action. Placement on the Long-Term Actions list generally signals that an agency does not expect to finalize within the next twelve months.

The companion HIPAA Privacy Rule modifications were pushed out as well, to a target of August 2027.

![Timeline of the HIPAA Security Rule rulemaking from the December 2024 NPRM through the July 2027 final action target, showing the February 16 2026 Part 2 compliance date that already passed](/blog/images/2-hipaa-security-rule-timeline-2025-2028.png)

Two qualifications matter here, and they cut in opposite directions.

Unified Agenda dates are planning estimates, not binding deadlines. OCR could finalize earlier or delay again. This date has already slipped once, by roughly fourteen months, so treat it as a signal about near-term likelihood rather than a date you can schedule against.

The compliance date would also be later than the rule date. Industry expectation is a compliance window of roughly 180 to 240 days after publication of a final rule. If July 2027 holds exactly, and if the window lands in that range, full compliance realistically arrives in 2028.

More than a hundred hospital systems and provider associations have formally asked HHS to withdraw or narrow the proposal. Whether it is finalized as written, substantially modified, delayed again, or withdrawn is not knowable right now.

## Why do so many sources say MFA and encryption are already mandatory?

Because the proposal is specific, prescriptive, and easy to summarize, and because summarizing a proposal in the present tense produces better headlines than summarizing it accurately.

Run the search yourself and you will find, on the first page, a LinkedIn post asserting that the 2026 Security Rule is finalized text, a vendor blog stating that encryption at rest is now mandatory, and a Reddit thread presenting mandatory MFA as settled fact. Google's own AI Overview for the query repeats the claim, and its citation chips point at that Reddit post and that LinkedIn post as sources.

This is not a harmless drafting error. If you are a fifteen-person practice and you believe the rule changed, you will make three predictable mistakes.

You will spend a capital budget on tooling to satisfy a requirement that does not exist, on a timeline nobody imposed. You will conclude that your documented decisions about addressable specifications are now worthless, and stop maintaining them. And you will assume that because you are working on the "new" rule, you are current on the old one, which is the rule OCR is actually enforcing while you do it.

![Comparison of common claims about HIPAA changes in 2026 against the text of 45 CFR Part 164](/blog/images/3-hipaa-2026-claimed-vs-actual.png)

## What does "addressable" still mean under 45 CFR 164.306(d)?

Exactly what it has meant since 2003, because that provision has not been amended.

Section 164.306(d) sorts every implementation specification in the Security Rule into one of two categories. If a specification is required, the word "Required" appears in parentheses after its title, and you must implement it. If it is addressable, the word "Addressable" appears, and § 164.306(d)(3) tells you what to do: assess whether the specification is a reasonable and appropriate safeguard in your environment, then either implement it, or, if implementing it is not reasonable and appropriate, document why not and implement an equivalent alternative measure if that is reasonable and appropriate.

Addressable has never meant optional. It has always meant documented.

The distinction matters for the two controls most often misreported. Encryption and decryption under the Access Control standard, at § 164.312(a)(2)(iv), is addressable. Encryption of ePHI in transmission, at § 164.312(e)(2)(ii), is addressable. Both would become mandatory under the proposal. Neither is mandatory today.

Multi-factor authentication is a different case entirely: it is not named in the current Security Rule at all. The Access Control standard at § 164.312(a) carries four implementation specifications. Unique user identification and emergency access procedure are Required. Automatic logoff and encryption and decryption are Addressable. MFA appears nowhere among them.

That does not make MFA a bad idea. It makes MFA a risk-based decision you are expected to reach and record through your risk analysis, rather than a line item you can be cited for omitting.

Risk analysis itself is Required, at § 164.308(a)(1)(ii)(A), and remains the single most frequently cited deficiency in OCR investigations. If you want the mechanics of when that analysis has to be revisited, we covered the trigger standard in detail in [when to update your HIPAA risk assessment]({% post_url 2026-07-27-when-to-update-hipaa-risk-assessment %}).

## Which HIPAA deadline actually took effect in 2026?

February 16, 2026, and it had nothing to do with cybersecurity.

In February 2024, HHS, through SAMHSA and OCR, finalized amendments to 42 CFR Part 2, the regulation governing the confidentiality of substance use disorder patient records. The final rule was published February 16, 2024, took effect April 16, 2024, and carried a general compliance date of February 16, 2026. It implements section 3221 of the CARES Act, and it aligns much of Part 2 with HIPAA while preserving heightened protections for SUD records.

The piece that catches almost everyone is the notice requirement. Covered entities had to revise their Notice of Privacy Practices under 45 CFR 164.520 to address uses and disclosures of Part 2 records.

Read the scope carefully, because this is where practices wrongly exclude themselves. The obligation is not limited to Part 2 programs. Any HIPAA covered entity that creates, maintains, receives, or transmits Part 2 records is in scope, precisely because so many providers receive SUD records from Part 2 programs for treatment and care coordination. A primary care group that receives records from an addiction medicine practice is in scope. So is a health plan. So, in many cases, is an employer-sponsored group health plan.

If you are both a covered entity and a Part 2 program, you may keep separate notices or combine them into one.

![Checklist of the Notice of Privacy Practices updates required by the February 16 2026 42 CFR Part 2 compliance date](/blog/images/4-hipaa-npp-part-2-deadline-checklist.png)

This one has teeth already. OCR announced its Civil Enforcement Program for Confidentiality of Substance Use Disorder Patient Records on February 13, 2026, and as of February 16, 2026 it is accepting complaints alleging violations of the Part 2 confidentiality regulations and of the related breach notification requirements.

So the practical position for a small practice on July 30, 2026 is close to the inverse of what the search results suggest. The cybersecurity requirements you have been told are mandatory are not, and will not be for at least a year. The privacy notice requirement nobody told you about was due five months ago and is enforceable now.

## Does the delay change what OCR is enforcing right now?

No, and this is the part worth being blunt about.

The current Security Rule has been in force since 2003. Enforcement of it does not pause while a proposal sits on the Long-Term Actions list. OCR's recent settlement record includes small covered entities, not only hospital systems, and the most common finding in those cases is a missing or inadequate risk analysis under § 164.308(a)(1)(ii)(A). We walked through what that enforcement actually looks like at small-practice scale in [HIPAA fines for small practices]({% post_url 2026-07-16-hipaa-fines-small-practice %}).

There is also a quieter risk in treating July 2027 as breathing room. Most of what the proposal would require, MFA, asset inventories, encryption, vulnerability scanning, incident response planning, is already widely accepted security practice. If a breach happens in 2026 and your risk analysis documented that MFA was reasonable and appropriate for remote access to your EHR and you never implemented it, the absence of a final rule will not help you. You will be answering for your own documented decision, not for a regulation that had not issued.

## What should a small practice do between now and 2027?

1. **Confirm whether the February 16, 2026 notice obligation applied to you.** If you create, receive, maintain, or transmit any Part 2 SUD records, it did. Check the version date on your current Notice of Privacy Practices before you check anything else.
2. **If your notice was not updated, update it now and date the revision.** A late correction with a documented date is a materially better position than an ongoing omission. Keep the superseded version; the six-year retention rule at § 164.316(b)(2)(i) still applies.
3. **Stop budgeting against a 2026 Security Rule deadline.** There isn't one. If a vendor is selling you urgency tied to a 2026 mandate, ask them to name the Federal Register citation for the final rule.
4. **Refresh the risk analysis instead.** It is Required today, it is the most-cited deficiency today, and it is the document that would carry most of the weight if the proposal is finalized. Our walkthrough of the [HIPAA security risk assessment]({% post_url 2026-06-28-hipaa-security-risk-assessment %}) covers the structure.
5. **Record your addressable decisions in writing.** For each addressable specification, note the assessment, the decision, and the alternative measure where one applies. This is the work that survives whatever the final rule says.
6. **Treat the proposal as a planning document, not a compliance obligation.** Read it, map your gaps against it, and sequence the work over eighteen months. Do not restructure your program around requirements that do not exist.
7. **Check the AI tools your staff adopted this year.** New technology triggers a risk analysis at the planning stage, and consumer AI accounts are the most common unreviewed data flow in small practices right now. We covered the specific BAA problem in [is ChatGPT HIPAA compliant]({% post_url 2026-07-23-is-chatgpt-hipaa-compliant %}).

If you want the risk analysis structure already built rather than assembled from scratch, the [HIPAA Security Risk Assessment Tool: Excel + Guide](https://payhip.com/b/vXmYA) is $57 and includes the asset inventory, threat and vulnerability pairing, risk scoring, and a dated revision log.

## The bottom line

The headline changes are not in effect and are now targeted for July 2027, with realistic compliance in 2028. The change that did land in 2026 was a privacy notice requirement with a February 16 compliance date and an active OCR enforcement program behind it.

Getting that distinction right is not pedantry. It is the difference between spending this year on the obligation you actually have and spending it on one somebody invented.

## Sources

- HHS Office for Civil Rights, *HIPAA Security Rule To Strengthen the Cybersecurity of Electronic Protected Health Information*, Notice of Proposed Rulemaking, 90 FR 898, January 6, 2025 (RIN 0945-AA22).
- Office of Information and Regulatory Affairs, Unified Agenda of Regulatory and Deregulatory Actions, RIN 0945-AA22, Final Rule Stage, Final Action 07/2027.
- 45 CFR 164.306, Security standards: General rules. Electronic Code of Federal Regulations.
- 45 CFR 164.308, Administrative safeguards. Electronic Code of Federal Regulations.
- 45 CFR 164.312, Technical safeguards. Electronic Code of Federal Regulations.
- 45 CFR 164.316, Policies and procedures and documentation requirements. Electronic Code of Federal Regulations.
- 45 CFR 164.520, Notice of privacy practices for protected health information. Electronic Code of Federal Regulations.
- HHS SAMHSA and OCR, *Confidentiality of Substance Use Disorder (SUD) Patient Records*, Final Rule, published February 16, 2024, effective April 16, 2024, compliance date February 16, 2026. Implements section 3221 of the CARES Act.
- HHS Office for Civil Rights, Civil Enforcement Program for Confidentiality of Substance Use Disorder Patient Records, announced February 13, 2026.
- HHS Office for Civil Rights, *Guidance on Risk Analysis*.
