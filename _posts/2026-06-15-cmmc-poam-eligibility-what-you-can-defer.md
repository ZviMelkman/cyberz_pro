---
layout: post
title: "What Can Actually Go on a CMMC POA&M (and What Can't)"
date: 2026-06-15
description: "Under 32 CFR 170.21, only 1-point controls can sit on a CMMC Level 2 POA&M, and six of those are barred by name. Here is exactly what you can defer, what you can't, and the 180-day clock that starts the day you get conditional status."
category: CMMC
tags: [CMMC, NIST 800-171, POA&M, conditional certification, 32 CFR 170.21]
image: /blog/images/1-cmmc-poam-what-cant-be-deferred-hero.png
author: CyberZ
---

*Most contractors treat the POA&M as a safety net: get close, defer the rest, finish later. The CMMC Final Rule does not work that way. The list of what you can defer is short, specific, and easy to misjudge by exactly the controls that sink an assessment.*

**A CMMC Level 2 Plan of Action and Milestones (POA&M) is a formal, time-bound plan to close requirements scored NOT MET during your assessment. Under 32 CFR 170.21, it can hold only requirements worth 1 point in the CMMC Scoring Methodology, with one narrow encryption exception, and six specific 1-point controls are excluded by name. Everything worth 3 or 5 points must be fully MET before the assessor scores it. By the scoring methodology in 32 CFR 170.24, that puts 63 of the 110 controls permanently off the POA&M.**

<div class="callout" style="border-left:4px solid #EE4C48;background:#16161a;padding:18px 22px;margin:26px 0;border-radius:4px;">
<strong style="color:#EE4C48;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0 0;padding-left:20px;line-height:1.55;">
<li>A POA&M is not a grace period for hard controls. Under 32 CFR 170.21, only 1-point requirements are eligible to be deferred.</li>
<li>63 of the 110 NIST SP 800-171 Rev 2 controls can never sit on a POA&M: every 3-point and 5-point control, plus six named 1-point controls.</li>
<li>Conditional status requires a score of at least 88 of 110 (0.80). Below that, there is no conditional path at all.</li>
<li>The one carve-out is SC.L2-3.13.11 CUI Encryption, deferrable at 3 points if encryption is used but is not FIPS-validated.</li>
<li>The 180-day closeout clock starts on your Conditional CMMC Status Date, not when you feel ready. Miss it and the status expires.</li>
</ul>
</div>

## The POA&M is not what it used to be

For years, "we'll POA&M it" was a reasonable answer in the Defense Industrial Base. Under the older self-attestation regime, a contractor could submit a Supplier Performance Risk System (SPRS) score below 110, keep an open plan of action, and continue working while remediating. The plan was broad and the enforcement was light.

The CMMC Final Rule ended that. The program rule at 32 CFR Part 170 took effect December 16, 2024, and the contract clause that pulls it into solicitations, DFARS 252.204-7021, became effective November 10, 2025. Since then, CMMC requirements have been appearing in live DoD solicitations, and the POA&M rules that come with them are far narrower than most contractors expect.

The governing section is 32 CFR 170.21. It is short, and it is strict. If you are preparing for a Level 2 assessment, whether a self-assessment under 170.16 or a C3PAO certification under 170.17, these are the rules that decide whether a gap is survivable or disqualifying.

## Level 1: no POA&M, ever

Start with the simplest case. Under 32 CFR 170.21(a)(1), a POA&M is not permitted at any time for a Level 1 self-assessment. Level 1 covers the 15 basic safeguarding requirements in FAR 52.204-21 for Federal Contract Information. You meet all of them, or you are not compliant. There is no partial credit and no deferral.

If your only obligation is Level 1, the POA&M conversation does not apply to you. Everything below is Level 2.

## The three gates to conditional Level 2 status

At Level 2, a POA&M is allowed, but only as the price of admission to a temporary status called Conditional Level 2. To earn it, 32 CFR 170.21(a)(2) sets three conditions, and all three must be met.

![The three 32 CFR 170.21 gates to Conditional Level 2 status](/blog/images/2-cmmc-poam-three-gates-170-21.png)

### Gate 1: a score of at least 88 of 110

Per 170.21(a)(2)(i), your assessment score divided by the total number of Level 2 requirements must be greater than or equal to 0.80. With 110 requirements, that is a score of at least 88.

The CMMC Scoring Methodology in 32 CFR 170.24 starts you at 110 points and subtracts the weight of each NOT MET requirement. Controls are weighted 1, 3, or 5 points by importance, with the 5-point controls reserved for the most consequential protections such as multifactor authentication. That weighting matters enormously for the math below.

### Gate 2: only 1-point items may be deferred

Per 170.21(a)(2)(ii), no requirement on your POA&M may have a point value greater than 1. Every 3-point and 5-point control must be fully implemented and scored MET before the assessment, with no exceptions in your favor.

There is exactly one carve-out, and it runs the other direction. SC.L2-3.13.11 (CUI Encryption) is normally a higher-weight control, but if you are employing encryption that simply is not FIPS-validated, it may be placed on a POA&M at a value of 3 points. This is the only place the rule lets a control above 1 point be deferred, and it applies only to that specific FIPS-validation gap.

### Gate 3: six 1-point controls are barred by name

This is the gate most contractors miss. Per 170.21(a)(2)(iii), six requirements are excluded from the POA&M even though each is worth only 1 point. They must be fully MET before assessment regardless of your score.

![The six 1-point controls barred from a CMMC POA&M under 32 CFR 170.21(a)(2)(iii)](/blog/images/3-cmmc-poam-six-barred-controls.png)

The six are:

- **AC.L2-3.1.20** External Connections (CUI Data)
- **AC.L2-3.1.22** Control Public Information (CUI Data)
- **CA.L2-3.12.4** System Security Plan
- **PE.L2-3.10.3** Escort Visitors (CUI Data)
- **PE.L2-3.10.4** Physical Access Logs (CUI Data)
- **PE.L2-3.10.5** Manage Physical Access (CUI Data)

Read that list against how teams actually scope their prep. The three physical-protection controls, escorting visitors, keeping physical access logs, and managing physical access to the facility, are the ones a software-focused team most often leaves as "we'll write the procedure later." Later is not an option for these. They are 1-point controls that behave like blockers.

## The control that is a prerequisite and a blocker at the same time

CA.L2-3.12.4, the System Security Plan, deserves its own paragraph. It appears on the barred list, so it cannot be deferred. It is also, in practice, a precondition for the assessment running at all: the C3PAO evaluates evidence against each of the 320 assessment objectives in NIST SP 800-171A, and the SSP is the document that describes how each control is implemented. No complete SSP means there is nothing for the assessor to assess.

So the SSP sits in a double bind. You cannot POA&M it, and you cannot proceed without it. It is the single most common reason a contractor is turned away before the real work of the assessment begins. If you do one thing before scheduling, make it a complete, current SSP.

## The 63 controls you can never defer

Put the three gates together and the deferrable set is small. Off the table entirely:

- Every 5-point control
- Every 3-point control
- The six named 1-point controls in 170.21(a)(2)(iii)

By the weighting in 32 CFR 170.24, that comes to 63 of the 110 requirements that can never appear on a Level 2 POA&M under any score. The only requirements eligible for deferral are the remaining 1-point controls, plus the single SC.L2-3.13.11 encryption exception.

That reframes the whole exercise. Conditional certification is not "finish most of it and clean up the rest." It is "fully implement the entire high-value core and the six named blockers, then defer a thin layer of low-weight items, briefly."

## Do the margin math before the assessor does

Here is the arithmetic that decides whether conditional status is even available to you.

You start at 110. You need 88. That is a budget of 22 points you can be missing on assessment day. Because only 1-point controls are deferrable, each eligible gap costs you exactly 1 point. So if every remaining gap is a POA&M-eligible 1-point control, you can carry at most 22 of them and still clear the 0.80 threshold. The 23rd drops you below 88, and at that point there is no conditional status to grant.

If you are also relying on the SC.L2-3.13.11 encryption exception, that single deferral consumes 3 of your 22 points, leaving room for roughly 19 one-point gaps. Any unmet 3-point or 5-point control is not a deduction you can absorb on a POA&M at all; it is a hard stop, because that control was never eligible to be deferred in the first place.

The practical takeaway: a contractor with a handful of 1-point gaps is a strong conditional candidate. A contractor missing a 5-point control is not a conditional candidate at any score. Knowing which bucket you are in, before you spend money on an assessment, is the entire point of an honest gap analysis.

## The 180-day clock is shorter than it sounds

Earning Conditional Level 2 status does not close the loop. Under 32 CFR 170.21(b), every item on the POA&M must be closed and confirmed by a POA&M closeout assessment within 180 days of your Conditional CMMC Status Date. For a Level 2 certification assessment, that closeout must be performed by an authorized or accredited C3PAO. For a Level 2 self-assessment, the closeout is performed by your organization in the same manner as the initial self-assessment. If the POA&M is not successfully closed out in that window, the conditional status for the information system expires.

Two things make 180 days tighter than it reads. First, the clock starts on the status date, not on the day you decide to start remediating. Second, a C3PAO closeout has to be scheduled, and assessor calendars are not open-ended. Treat the 180 days as a deadline that includes finding and booking a closeout slot, not just doing the technical work.

## Why this is a False Claims Act issue, not just a checklist

There is a reason to get the score and the POA&M exactly right beyond passing the assessment. The SPRS score you report is a representation to the government. Department of Justice settlements under the Civil Cyber-Fraud Initiative have repeatedly turned on inaccurate cybersecurity representations rather than on any breach. The $4.6M MORSECORP settlement (March 2025) and the $8.4M Raytheon/Nightwing settlement (May 2025) both resolved allegations of failing to implement NIST SP 800-171 and misrepresenting compliance, with no requirement that data was ever lost.

A conditional status does not paper over a score that was reported wrong. If your SPRS number does not reflect what your SSP and your systems can actually show, the gap between claim and reality is the exposure, and the POA&M rules do not change that. This is why the score and the supporting evidence have to be built from the controls up, not reverse-engineered to clear 88.

## What to do this week

- **Score yourself honestly against 110.** Use the 1/3/5 weights from 32 CFR 170.24, not a gut feel. You are looking for your real number and, more importantly, where the deductions sit.
- **Sort every gap by point value.** Any 3-point or 5-point gap is a hard stop that must be fully implemented. There is no deferring it.
- **Check the six named controls specifically.** AC.L2-3.1.20, AC.L2-3.1.22, CA.L2-3.12.4, PE.L2-3.10.3, PE.L2-3.10.4, PE.L2-3.10.5. These pass the point-value test but are barred anyway.
- **Confirm your SSP is complete and current.** CA.L2-3.12.4 is both a prerequisite and non-deferrable.
- **Map your 180 days backward from a closeout slot,** not forward from today.

## The bottom line

The POA&M is real, but it is a narrow instrument, not a cushion. Conditional Level 2 status is reserved for contractors who have already implemented the hard parts and need a short, monitored window to finish a thin layer of low-weight items. If you are counting on deferring anything that matters, the rule has already decided otherwise. Know your score, know which gaps are deferrable, and know your closeout date before you ever contact an assessor.

The full set of tools we use to get a contractor scored, scoped, and ready to schedule, including the SSP template and the SPRS scoring workbook, lives in the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147). If your immediate problem is the number, the [NIST 800-171 SPRS Score Workbook for CMMC Level 2](https://payhip.com/b/R5g4Y) ($87) walks the 1/3/5 weighting control by control so you know your real margin before assessment day.

## Sources

- 32 CFR 170.21, Plan of Action and Milestones requirements (eCFR, Title 32, current edition)
- 32 CFR 170.17, CMMC Level 2 certification assessment and affirmation requirements (eCFR)
- 32 CFR 170.24, CMMC Scoring Methodology (eCFR)
- NIST SP 800-171 Rev 2 and NIST SP 800-171A (assessment objectives and methods)
- DoD CMMC Assessment Guide, Level 2 (dodcio.defense.gov)
- DFARS 252.204-7021 (CMMC requirement clause, effective November 10, 2025)
- U.S. Department of Justice press releases, Civil Cyber-Fraud Initiative settlements (MORSECORP, March 2025; Raytheon/Nightwing, May 2025)
