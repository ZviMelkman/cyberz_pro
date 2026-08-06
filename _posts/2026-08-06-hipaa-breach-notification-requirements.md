---
layout: post
title: "HIPAA Breach Notification Requirements: The 60-Day Limit Is a Ceiling, Not a Deadline"
date: 2026-08-06
description: "OCR settled with a health system for $552,250 on July 29, 2026, and two of the four cited violations were timing failures. What 45 CFR 164.400 through 164.414 actually requires, including the two different 500 thresholds."
category: HIPAA
tags: [HIPAA, breach notification, 45 CFR 164.404, 45 CFR 164.408, OCR, business associate, small practice, compliance]
image: /blog/images/1-hipaa-breach-notification-requirements-hero.png
author: CyberZ
---

*Search "HIPAA breach notification requirements" and page one will give you four facts: 60 days, 500 records, tell the patients, tell HHS. All four are roughly true. None of them is the fact that gets practices penalized.*

**The HIPAA Breach Notification Rule is 45 CFR 164.400 through 164.414. It requires a covered entity to notify each affected individual following discovery of a breach of unsecured protected health information without unreasonable delay and in no case later than 60 calendar days after discovery, under 164.404(b). Breaches involving 500 or more individuals must be reported to the HHS Secretary contemporaneously with the individual notice under 164.408(b), while breaches involving fewer than 500 individuals go into a log filed no later than 60 days after the end of the calendar year under 164.408(c). Media notice under 164.406 is owed only when a breach involves more than 500 residents of a single state or jurisdiction. Business associates must notify the covered entity within the same 60-day outer limit under 164.410(b). Under 164.414(b), the burden of proving that notifications were made, or that the incident was not a breach at all, sits with the regulated entity.**

<div style="border-left:4px solid #EE4C48;background:#f7f7f8;padding:18px 22px;margin:28px 0;border-radius:4px;">
<strong style="display:block;margin-bottom:10px;font-size:1.05em;">Key Takeaways</strong>
<ul style="margin:0;padding-left:20px;line-height:1.7;">
<li>Subpart D has not changed since January 3, 2017. Title 45 is current as of August 4, 2026 and the breach rule text is untouched, including through the pending Security Rule proposal.</li>
<li>60 calendar days is an outer limit, not a target. The operative phrase in &sect; 164.404(b) is "without unreasonable delay," and OCR has treated sitting on a notice as its own violation.</li>
<li>Discovery is not the day your IT vendor finishes the forensic report. Under &sect; 164.404(a)(2) it is the first day the breach was known, or would have been known with reasonable diligence, to any workforce member or agent other than the person who caused it.</li>
<li>There are two different 500 thresholds. Media notice needs <em>more than</em> 500 residents of one state. HHS notice needs 500 <em>or more</em> individuals in total.</li>
<li>For 500 or more individuals, the HHS report is contemporaneous with the individual notice. It is not a separate 60-day allowance.</li>
<li>Every impermissible use or disclosure is <em>presumed</em> to be a breach under &sect; 164.402(2) unless you document a low probability of compromise across four specified factors.</li>
<li>Encryption and destruction per the HHS guidance at 74 FR 19006 take information outside the definition of "unsecured," which is the only true safe harbor in the rule.</li>
<li>On July 29, 2026 OCR settled with OSF Healthcare System for $552,250. Two of the four cited violations were failures to notify on time, not failures to secure.</li>
</ul>
</div>

## What are the HIPAA breach notification requirements?

Five separate obligations, all triggered by the same event.

Following discovery of a breach of unsecured protected health information, a covered entity owes notice to each affected individual (164.404), to prominent media outlets in certain cases (164.406), and to the Secretary of HHS (164.408). A business associate owes notice to the covered entity (164.410). Law enforcement can pause all of it (164.412). And under 164.414(b) the entity carries the burden of proving it did what the rule required.

The subpart applies to breaches occurring on or after September 23, 2009. It has not been amended since January 3, 2017. That matters because a great deal of 2026 HIPAA content is written as though a rewrite is imminent. The [proposed Security Rule overhaul]({% post_url 2026-07-30-hipaa-security-rule-changes-2026 %}) is real, still a proposal, and now targeted for July 2027. It would not change Subpart D. The breach rule you are reading about here is the breach rule you are subject to today.

## When does the 60-day clock actually start?

Not when you finish investigating. This is the single most expensive misunderstanding in the rule.

Section 164.404(a)(2) defines discovery as the first day on which the breach is known to the covered entity, or by exercising reasonable diligence would have been known. It then imputes that knowledge broadly: the entity is deemed to know about a breach if it is known, or would have been known with reasonable diligence, to any person who is a workforce member or agent of the entity, other than the person who committed the breach.

Read that carefully. A front desk employee who notices a missing folder on a Tuesday starts the clock on that Tuesday. It does not start when the practice manager hears about it on Friday, and it does not start when the incident response vendor issues findings six weeks later. The exclusion for the person who caused the breach exists so that a bad actor cannot start and run out your clock in secret, and it does not shelter anyone else.

The same imputed-knowledge standard applies to business associates under 164.410(a)(2), using the federal common law of agency.

![Five notification clocks under the HIPAA Breach Notification Rule, all triggered by the date of discovery](/blog/images/3-hipaa-breach-notification-60-day-clocks.png)

## Is every impermissible disclosure a breach?

It is presumed to be one, which is the reverse of how most practices behave.

Section 164.402 defines a breach as an acquisition, access, use, or disclosure of protected health information not permitted under the Privacy Rule that compromises its security or privacy. Then paragraph (2) sets the default: any impermissible use or disclosure is presumed to be a breach unless the covered entity or business associate demonstrates a low probability that the information has been compromised, based on a risk assessment of at least four factors.

The four factors are the nature and extent of the information involved, including the types of identifiers and the likelihood of re-identification; the unauthorized person who used it or to whom it was disclosed; whether the information was actually acquired or viewed; and the extent to which the risk has been mitigated.

Three narrow exclusions sit ahead of that test at 164.402(1). Good-faith, in-scope access by a workforce member that is not further disclosed. Inadvertent disclosure between two people who are both authorized to access protected health information at the same entity, again not further disclosed. And a disclosure where the entity has a good-faith belief the unauthorized recipient could not reasonably have retained the information.

Before any of that, ask whether the information was "unsecured" at all. Section 164.402 defines unsecured protected health information by reference to guidance the Secretary issued under section 13402(h)(2) of Public Law 111-5. That guidance was issued April 17, 2009 and published at 74 FR 19006, and it specifies exactly two methodologies: encryption and destruction. Information encrypted to that standard, with the key uncompromised, is not unsecured, so no breach notification obligation arises. HHS calls this the breach safe harbor in its own cloud computing guidance. It is the only genuine safe harbor the rule contains.

![The 45 CFR 164.402 breach determination: exclusions, the presumption, and the four-factor risk assessment](/blog/images/2-hipaa-breach-notification-four-factor-test.png)

The practical failure here is not getting the four-factor analysis wrong. It is never documenting that you ran it. Section 164.414(b) puts the burden of proof on you, and 164.414(a) pulls in the Privacy Rule documentation requirements at 164.530(j), which means retaining the documentation for six years. An undocumented determination that an incident was not a breach is, to a regulator, indistinguishable from an unreported breach.

## Why is the 60-day limit a ceiling rather than a deadline?

Because the sentence has two halves and most summaries quote only one.

Section 164.404(b) requires notification "without unreasonable delay and in no case later than 60 calendar days after discovery." The 60 days is the absolute outer boundary. The operative standard is the first clause. If you identified every affected patient on day nine and mailed notices on day 58, you complied with the second half of the sentence and arguably violated the first.

This is not a theoretical reading. OCR has been enforcing the timing requirement as a standalone violation since 2017, and it did so again eight days ago.

## Which 500 threshold applies to which notice?

Two thresholds, two different populations, and they are commonly conflated.

Media notice under 164.406 is owed for a breach involving **more than 500 residents of a State or jurisdiction**. That is 501 people in one state, counted state by state.

Secretary notice under 164.408(b) is owed for a breach involving **500 or more individuals**, counted in total across every state.

So a breach affecting 2,000 patients spread evenly across five states owes HHS a report at the same time as the individual notices, and owes the media nothing at all, because no single state crosses 500. A breach affecting 501 patients who all live in one state owes both.

The timing differs too. For 500 or more individuals, 164.408(b) requires the report to the Secretary contemporaneously with the individual notice, in the manner specified on the HHS website, which in practice means the HHS breach portal. It is not a second, independent 60-day window, and a fair amount of published guidance describes it as one.

For breaches involving fewer than 500 individuals, 164.408(c) requires maintaining a log and submitting the notification no later than 60 days after the end of the calendar year in which the breach was discovered. For breaches discovered during 2026, that filing is due by March 1, 2027. The individual notice for those small breaches is still owed on the ordinary 60-day clock. Only the HHS report waits.

![The two different 500 thresholds in the HIPAA Breach Notification Rule and what each one triggers](/blog/images/4-hipaa-breach-notification-500-record-thresholds.png)

## What does a business associate owe, and when?

Notice to the covered entity, without unreasonable delay and no later than 60 calendar days after the business associate discovers the breach, under 164.410(b).

The content requirement at 164.410(c) is more demanding than most business associate agreements suggest. The business associate must identify, to the extent possible, each individual whose information was involved, and must provide the covered entity with any other information the covered entity needs for its own individual notice under 164.404(c), either at the time of notification or promptly as it becomes available.

The structural risk is obvious once stated. Your clock as a covered entity depends on a vendor telling you something. If the vendor stays silent, your patients go unnotified and you are the one on the HHS breach portal. That is worth checking your business associate agreements for, because 60 days is the regulatory floor for the vendor and nothing stops you from contracting for less.

## What has OCR actually penalized?

Timing, by itself, repeatedly.

On **July 29, 2026**, OCR announced a settlement with **OSF Healthcare System** and its affiliated covered entities for **$552,250**, its 21st ransomware enforcement action. OSF discovered in April 2021 that its files had been infected with the Nephilim ransomware variant, and 53,907 individuals' information was exfiltrated. OSF filed its breach report in October 2021. Of the four potential violations OCR cited, two were timing: failing to provide timely breach notification to affected individuals, and failing to provide timely breach notification to the Secretary. The other two were the absent risk analysis and the impermissible disclosure itself.

On **March 5, 2026**, OCR settled with **MMG Fusion, LLC**, a Maryland software company acting as a business associate, over an intrusion in December 2020 that reached the protected health information of approximately 15 million individuals. Among the cited violations: failing to notify the covered entities affected by the incident. The settlement was **$10,000**, and OCR stated it considered MMG's financial condition. The corrective action plan requires MMG to go back and conduct a breach risk assessment of the 2020 attack and, to the extent possible, give the affected covered entities accurate notice. OCR Director Paula M. Stannard used the announcement to restate the business associate obligation directly, noting that timeliness is what allows a covered entity to meet its own notification duties.

The pattern is not new. On **January 9, 2017**, OCR settled with **Presence Health** for **$475,000** in what it described as the first HIPAA enforcement action based on untimely breach notification. Paper operating room schedules containing the information of 836 individuals went missing, discovered October 22, 2013. OCR received the breach report on January 31, 2014. OCR found Presence Health had failed to notify the affected individuals, prominent media outlets, and OCR itself within 60 days.

![Three verified HHS OCR settlements citing untimely HIPAA breach notification](/blog/images/5-hipaa-breach-notification-ocr-enforcement.png)

Note what is absent from all three. No allegation that anyone was demonstrably harmed by the delay. The late notice was the violation.

## What should a small practice do this week?

1. **Write down who can start your clock.** List the roles whose knowledge is imputed to the practice under 164.404(a)(2). It is broader than your privacy officer. Then make sure those people know that noticing something is the trigger for escalating it the same day.

2. **Build a breach determination log.** One page per incident: what happened, discovery date and how you learned, which exclusion you considered, the four factors from 164.402(2) with your reasoning on each, the conclusion, and the date. Retain it six years per 164.530(j). This is the document that turns "we decided it wasn't reportable" into a defensible position.

3. **Fix the two 500 thresholds in your policy.** If your written procedure says media notice at 500, it is wrong. It is more than 500 residents of one state.

4. **Correct the HHS timing language.** If your procedure gives you 60 days to file with HHS on a large breach, it is wrong. That report is contemporaneous with the individual notice.

5. **Diary the annual log filing.** Breaches discovered in 2026 that affected fewer than 500 individuals are due to HHS by March 1, 2027. Practices miss this one because nothing prompts them.

6. **Read your business associate agreements for the notification clause.** Sixty days from the vendor's discovery consumes your entire window. Shorter contractual notice is negotiable and worth asking for.

7. **Check whether your notice template contains all five elements.** Section 164.404(c)(1) requires a description of what happened with dates, the types of information involved, steps individuals should take, what you are doing about it, and contact procedures including a toll-free number, email address, website, or postal address. In plain language.

8. **Confirm your encryption posture.** Encryption to the 74 FR 19006 standard is the difference between an incident and a reportable breach. Whether your practice has actually [documented that in a current risk analysis]({% post_url 2026-07-27-when-to-update-hipaa-risk-assessment %}) is a separate question, and it is the one OCR asks first.

If you want the underlying risk analysis structure already built rather than assembled from scratch, the [HIPAA Security Risk Assessment Tool: Excel + Guide](https://payhip.com/b/vXmYA) is $57 and includes the asset inventory, threat and vulnerability pairing, risk scoring, and a dated revision log. It is a security risk analysis under 164.308(a)(1)(ii)(A), not a breach determination under 164.402, and the two are different documents. It is the one OCR cited as missing in all three settlements above.

## The bottom line

The Breach Notification Rule punishes the calendar as readily as it punishes the incident. In every settlement above, the underlying event was ordinary: missing paper, ransomware, an intrusion. What OCR wrote down was that the notice came late.

Sixty days is where the rule stops tolerating you, not where it expects you to act. If you learn what happened on day twelve, the question a regulator will ask is what you were doing on day thirteen. Whether your [exposure as a small practice]({% post_url 2026-07-16-hipaa-fines-small-practice %}) is $10,000 or $552,250 has more to do with your documentation than your size.

## Sources

- 45 CFR Part 164 Subpart D, *Notification in the Case of Breach of Unsecured Protected Health Information*, sections 164.400 through 164.414. Electronic Code of Federal Regulations, Title 45 current as of August 4, 2026. Subpart D last amended January 3, 2017.
- 45 CFR 164.402, Definitions (breach, exclusions, four-factor risk assessment, unsecured protected health information).
- 45 CFR 164.404, Notification to individuals (discovery, timeliness, content, methods, substitute notice).
- 45 CFR 164.406, Notification to the media.
- 45 CFR 164.408, Notification to the Secretary.
- 45 CFR 164.410, Notification by a business associate.
- 45 CFR 164.412, Law enforcement delay.
- 45 CFR 164.414, Administrative requirements and burden of proof.
- 45 CFR 164.530(j), Documentation retention, incorporated by 164.414(a).
- HHS, *Guidance Specifying the Technologies and Methodologies That Render Protected Health Information Unusable, Unreadable, or Indecipherable to Unauthorized Individuals*, issued April 17, 2009, published at 74 FR 19006, April 27, 2009.
- HHS Office for Civil Rights, *Guidance on HIPAA and Cloud Computing* (breach safe harbor for encrypted electronic protected health information).
- HHS Office for Civil Rights, "HHS' Office for Civil Rights Settles Ransomware Investigation with Healthcare System," press release, July 29, 2026 (OSF Healthcare System, $552,250).
- HHS Office for Civil Rights, "HHS' Office for Civil Rights Settles HIPAA Investigation of MMG Fusion, LLC Breach Affecting 15 Million Individuals," press release, March 5, 2026 ($10,000).
- HHS Office for Civil Rights, "First HIPAA enforcement action for lack of timely breach notification settles for $475,000," press release, January 9, 2017 (Presence Health).
