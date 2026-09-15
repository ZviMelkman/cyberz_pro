---
layout: post
title: "The Date You Promised in SPRS Has Passed. Your Score Has Not Moved. That Is the Problem."
date: 2026-09-15
description: "Every NIST 800-171 self-assessment under 110 requires a Plan of Action Completion Date in SPRS. Nothing in the system ages that date. What an expired completion date next to an unchanged score says to DCMA, a prime, and a whistleblower, what LOGZONE shows about stale representations, and the ten-day fix."
category: CMMC
tags: [CMMC, SPRS, Plan of Action Completion Date, NIST 800-171, POA&M, DFARS 252.204-7019, DFARS 252.204-7020, False Claims Act, LOGZONE, defense contractors]
image: /blog/images/1-sprs-plan-of-action-completion-date-hero.png
author: CyberZ
---

*Every CMMC guide talks about the score. Almost none talk about the other number you typed into SPRS the same day: the date you said you would reach 110. For a lot of small contractors that date was in 2024 or 2025. It has passed, the score is the same, and nobody has looked at it since.*

**The SPRS Plan of Action Completion Date is the date a contractor enters in the Supplier Performance Risk System stating when it expects all 110 NIST SP 800-171 requirements to be implemented, meaning a score of 110. SPRS requires the field for any self-assessment score below 110, and DFARS 252.204-7019 and 252.204-7020 describe it as the date all requirements are expected to be implemented, based on the contractor's plan of action. It is a representation to the Department of Defense. Once it passes with the same gaps open and the same score posted, the record shows a commitment the contractor made and did not keep.**

<div class="key-takeaways" style="border-left:4px solid #EE4C48;background:#15151a;padding:18px 24px;margin:28px 0;border-radius:6px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;">
<li>Any NIST SP 800-171 Basic Assessment score under 110 requires a Plan of Action Completion Date in SPRS. The clause text calls it the date all requirements are expected to be implemented, drawn from your POA&M. SPRS will not save the record without it.</li>
<li>SPRS ages exactly one thing: the assessment date, which turns red after three years. The score never expires and the completion date is never flagged. A 2024 completion date sits in the record indefinitely, and the only people who will notice it passed are the ones reading your record for a reason.</li>
<li>The exposure is not the missed date by itself. It is the combination: a passed date, an unchanged score, and open POA&M items with no record of what happened. That is a stale representation, and DOJ settled with LOGZONE for $507,144 on June 18, 2026 over a self-assessment score that sat untouched while a DCMA assessment found the real number was minus 170.</li>
<li>The fix is one operation, not three: re-run the assessment against NIST SP 800-171A, then update the score, the assessment date, and the completion date together, with a written basis for the new date. Pushing the date out with nothing else changed is the one thing not to do.</li>
<li>With third-party assessments stripped from contracts by the September 3 class deviation, the SPRS record is the government's primary view of your compliance. Nothing else is checking this for you.</li>
</ul>
</div>

## What the field actually is

When a contractor posts a NIST SP 800-171 Basic Assessment in SPRS, the entry screen asks for a fixed set of things: the assessment date, the summary score, the assessment scope (Enterprise, Enclave, or Contract), the system security plan name, version, and date, the CAGE codes covered, and a Plan of Action Completion Date. The SPRS training transcript for vendors states it plainly: if a score of 110 is not achieved, a Plan of Action Completion Date is required.

The clause language behind that screen is in DFARS 252.204-7019(d) and 252.204-7020(b). Both list the same item at the end of the required information: the date that all requirements are expected to be implemented, meaning a score of 110 is expected to be achieved, based on information gathered from the associated plan of action developed in accordance with NIST SP 800-171.

Two things in that sentence matter. First, "expected to be implemented" is not "hoped for." It is the contractor's forecast, derived from its own POA&M, entered into a government system that contracting officers use to make award decisions. Second, the date is tied explicitly to the plan of action. It is supposed to be the last milestone on the last open item. If the POA&M has moved, the date should have moved with it.

The FAR Overhaul housekeeping did not change any of this. DFARS 252.204-7019 was eliminated as a standalone provision on February 1, 2026 and 252.204-7020 was renumbered into the new Part 240 clause set, which the [7019 deletion walkthrough]({% post_url 2026-06-16-dfars-7019-deleted-sprs-score %}) covers. The reporting fields travelled with the clause, and SPRS enforces them at the entry screen regardless of which clause number a given contract carries.

## Why nobody notices when it passes

SPRS ages one field. The vendor training for viewing NIST SP 800-171 assessments says assessment results turn red when the assessment date goes beyond three years. That matches the clause: DFARS 252.204-7019(b) requires a Basic Assessment that is current, defined as not more than three years old unless the solicitation says otherwise.

Nothing comparable happens to the completion date. There is no color change, no email, no warning at login. The score does not expire either. A contractor that posted a 78 in March 2024 with a completion date of December 2024 has a record today that reads, to anyone who opens it, as a company that missed its own forecast by nine months and then stopped updating.

![Three SPRS fields. Only the assessment date turns red after three years; the score never expires and the completion date is never flagged](/blog/images/2-sprs-three-fields-only-one-turns-red.png)

The last fourteen months made this worse in a specific way. When the Department suspended CMMC Phase 2 on July 13, a lot of shops froze their "CMMC project," and because the CMMC project and the NIST 800-171 remediation were the same spreadsheet with one name, the remediation froze too. The POA&M items did not close. The completion dates written in 2024 and early 2025, which assumed a November 2026 third-party assessment was coming, quietly expired during the pause. The [class deviation of September 3]({% post_url 2026-09-10-cmmc-phase-2-class-deviation %}) then stripped the third-party checkpoint out of the contracts entirely. The verification layer that might have caught a stale record before the government relied on it is gone. The record is what the government sees.

## Who reads an expired date, and what they see

Three audiences open your SPRS record, and none of them read the completion date as a formality.

**DCMA.** The Defense Contract Management Agency's DIBCAC conducts Medium and High assessments under 252.204-7020, and it selects targets. A record where the self-assessed score has not changed since 2023, the completion date passed in 2024, and the SSP date is older still is exactly the profile that draws a look. That is the pattern in LOGZONE, below.

**Your prime.** Under 252.204-7020(g), a prime cannot award a subcontract subject to NIST SP 800-171 unless the sub has a current Basic Assessment posted. Primes read the whole record when they run supplier risk reviews. An expired completion date is the first thing a diligent supply-chain analyst asks about.

**A relator.** DFARS 252.204-7019(b) says the score is used to determine whether the offeror is eligible for award. That single sentence is the materiality argument in a False Claims Act complaint. A former IT lead or FSO who knows the POA&M never moved has a clean story: the company told the government it would be at 110 by a date, it was not, and it kept the old score posted while it billed. The [Honeywell settlement]({% post_url 2026-09-02-honeywell-fca-cybersecurity-settlement %}) and MORSECORP both started with an insider.

## LOGZONE: the anatomy of a stale representation

The June settlement is worth reading for the timeline rather than the dollar figure.

![LOGZONE timeline: self-scored 110 in October 2021, billed the Navy from 2021 to 2025, DCMA assessment scored minus 170, $507,144 settlement in June 2026](/blog/images/3-logzone-sprs-score-110-to-minus-170-timeline.png)

According to the Department of Justice press release of June 18, 2026, LOGZONE Inc. of Huntsville, Alabama agreed to pay $507,144 to resolve False Claims Act liability for knowingly failing to comply with cybersecurity requirements on two Navy contracts. From May 2021 to March 2025, the company allegedly failed to implement NIST SP 800-171 controls that, if unimplemented, could lead to significant exploitation of the system or exfiltration of sensitive defense information. The deficiencies surfaced when DCMA assessed LOGZONE's implementation and scored it at minus 170, near the bottom of the minus 203 to 110 range. Of the total, $253,572 is restitution, which is the standard double-damages structure.

The settlement agreement, as reported by the FCA bar, adds the detail that matters here: LOGZONE's own October 2021 self-assessment reported a perfect 110. A 110 does not require a completion date, so LOGZONE never had one to miss. What it had was a number that nobody revisited for three and a half years while claims were submitted against it.

That is the mechanism. Not a breach. Not a missed deadline in isolation. A representation in SPRS that stopped matching reality and stayed posted. A contractor with an 82 and a completion date of June 2025 is in a structurally similar position on September 15, 2026 if the 82 and the June 2025 date are still what the record shows. The number is smaller and the story is more sympathetic, but the shape is the same: the government relied on a forecast, the forecast was wrong, and the contractor let it stand.

One distinction is worth stating precisely, because the [self-disclosure piece]({% post_url 2026-09-14-sprs-score-wrong-self-disclosure %}) turned on it. Under 31 U.S.C. § 3729(b)(1), "knowingly" includes reckless disregard. Posting a completion date in good faith and then missing it is not fraud. Knowing it passed, knowing the items are still open, and leaving the record as it is for another year while certifying compliance on invoices is where the knowledge standard starts to bite.

## What to do when your date has passed

The instinct is to log in and push the date out. Do not do that first. A completion date that moves with no change to the score, the assessment date, or the SSP is a worse record than an expired one, because it documents that someone looked and chose to change only the forecast.

![If your SPRS completion date has passed: all POA&M items closed means re-assess and post 110; some closed means a new score and a new date; none closed means an honest date with a written reason](/blog/images/4-sprs-completion-date-passed-three-cases.png)

Start with the POA&M, not the portal. Pull the plan of action that generated the original completion date and sort the open items into what actually happened.

**Case one: everything closed.** Some shops finished the work during the run-up to November 2026 and never went back to update SPRS. This is the best position and the easiest fix. Re-run the assessment against NIST SP 800-171A, confirm each previously open objective now has evidence, and post the new score with today's assessment date. At 110 the completion date field falls away. The [90-day improvement walkthrough]({% post_url 2026-09-06-how-to-improve-sprs-score %}) covers how to document the jump so the jump is not the story.

**Case two: some closed, some open.** Re-score. Every closed item moves the score by its weight under the DoD Assessment Methodology (5, 3, or 1 point), so the new number will be higher than the posted one. Update the score, the assessment date, and the SSP date together, then set a new completion date derived from the remaining items' realistic milestones. Write one paragraph, kept with the POA&M, explaining what closed, what did not, and why the new date is credible.

**Case three: nothing moved.** This is more common than anyone admits, especially in shops that paused in July. The honest entry is a new assessment date confirming the score still holds, a new completion date that reflects a plan you actually intend to execute, and a memo to the file explaining the gap. If the true answer is that some items will never close because they are not funded, say so in the POA&M and set the date accordingly. Under 32 CFR 170.21, the CMMC rule limited what can sit on a POA&M and how long, and the [POA&M eligibility walkthrough]({% post_url 2026-06-17-cmmc-poam-eligibility %}) covers which items cannot be deferred at all. A 5-point control that has been on the plan since 2023 is not a plan; it is a decision, and the record should read like one.

In all three cases, keep the prior record. SPRS lets you edit the entry, but the history of what you posted and when is what will let you show a reviewer, or DOJ, that the correction was prompt once you found it.

### The next ten days

A small contractor can close this out in ten working days without outside help.

Days one and two: pull the current SPRS record, the POA&M it was based on, and the SSP. Put the three dates side by side.

Days three to six: walk the open POA&M items against NIST SP 800-171A objectives with whoever owns each control. Mark closed, partially closed, or open, and attach the evidence for anything you are marking closed. Do not mark anything closed on memory.

Days seven and eight: compute the new score, draft the new completion date from the remaining milestones, and write the one-page basis memo.

Days nine and ten: brief the person who signs the annual affirmation, post the updated record, and file the memo and evidence index with the SSP.

The [NIST 800-171 SPRS Score Workbook for CMMC Level 2](https://payhip.com/b/R5g4Y) ($87) is built for days seven and eight: it scores each objective on the real 5/3/1 weights, tracks which items are POA&M-eligible, and produces the number and the date from the same sheet so they cannot drift apart. If the POA&M review on days three to six turns up an SSP that no longer describes the environment, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) has the SSP template, evidence tracker, and asset scoping worksheet to rebuild the record from the environment up rather than from the old spreadsheet down.

## The bottom line

The Plan of Action Completion Date is the only forward-looking promise in your SPRS record, and it is the one nobody monitors. The system will not tell you it passed. Your prime, DCMA, and a relator will all notice that it did, and each will read the unchanged score next to it the same way. The fix is not to move the date. It is to go back to the plan the date came from, find out what is actually true, and post all three fields together so the record describes the company as it stands today. That is a ten-day job. The alternative is a record that describes a company you said you would become and did not.

## Sources

- Supplier Performance Risk System, "NIST SP 800-171 Assessments" module description, sprs.csd.disa.mil/nistsp.htm (lists assessment date, score, scope, plan of action completion date, CAGE codes, SSP name, version, and date)
- Supplier Performance Risk System, "NIST SP 800-171 Entry Vendor Tutorial" transcript ("If a score of 110 is not achieved, a Plan of Action Completion Date is required")
- Supplier Performance Risk System, "Viewing NIST SP 800-171 Assessments" transcript (assessment results turn red when the assessment date exceeds three years)
- DFARS 252.204-7019, Notice of NIST SP 800-171 DoD Assessment Requirements, paragraphs (b) and (d)(1)(i)(F), acquisition.gov and eCFR
- DFARS 252.204-7020, NIST SP 800-171 DoD Assessment Requirements, paragraphs (b)(1)(i)(F) and (g), acquisition.gov
- DoD, NIST SP 800-171 DoD Assessment Methodology, Version 1.2.1, June 24, 2020
- 32 CFR 170.21, Plan of Action and Milestones requirements, eCFR
- U.S. Department of Justice, Office of Public Affairs, "Alabama Defense Contractor Agrees to Pay $507,144 to Resolve False Claims Act Liability Relating to Cybersecurity Violations," June 18, 2026
- Sidley Austin LLP, False Claims Act Blog, analysis of the LOGZONE settlement agreement (October 2021 self-assessment score of 110), June 23, 2026
- DefenseScoop, "Defense contractor settles cybersecurity False Claims Act allegations," June 18, 2026 ($253,572 restitution figure)
- 31 U.S.C. § 3729(b)(1), definition of "knowingly"
- Washington Technology, "CMMC's Phase 2 suspension locked in with binding regulation," September 9, 2026
