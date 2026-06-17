---
layout: post
title: "Which CMMC Gaps You Can POA&M (and the 63 You Can't)"
date: 2026-06-17
description: "CMMC POA&M eligibility under 32 CFR 170.21, explained: which controls you can defer to Conditional status, the 88-point floor, the six controls named out, and the 180-day clock."
category: cmmc
tags: [CMMC, NIST 800-171, POA&M, Conditional Certification]
image: /blog/images/1-cmmc-poam-eligibility-hero.png
author: CyberZ
---

*Most contractors plan their CMMC timeline around a gap they expect to fix later. The rule decides which gaps that is allowed for, and the list is shorter than almost anyone assumes.*

**A Plan of Action and Milestones (POA&M) in CMMC is a documented, time-bound plan to close security requirements that were scored NOT MET during your assessment. Under 32 CFR 170.21 it does one thing and only one thing: it lets you reach a Conditional CMMC Status instead of failing outright. It is not a way to skip controls, and it covers far fewer of them than the old self-attestation habit suggests.**

<div class="callout" markdown="0" style="border:1px solid #EE4C48;border-left:6px solid #EE4C48;background:#161618;padding:18px 22px;border-radius:6px;margin:28px 0;">
  <strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
  <ul style="margin:12px 0 0;padding-left:20px;line-height:1.55;">
    <li>A POA&amp;M in CMMC only earns a Conditional status. Level 1 self-assessments get no POA&amp;M at all.</li>
    <li>Only requirements worth 1 point under the CMMC Scoring Methodology (32 CFR 170.24) are eligible. Every 3-point and 5-point control must be MET at assessment.</li>
    <li>Six specific 1-point controls are excluded by name under 32 CFR 170.21(a)(2)(iii), including your System Security Plan (CA.L2-3.12.4).</li>
    <li>You must score at least 88 of 110 to qualify, which leaves a 22-point cushion and no more.</li>
    <li>Every open item closes within 180 days of the Conditional status date, confirmed by a C3PAO closeout assessment, or the status expires.</li>
  </ul>
</div>

## The POA&M is not what it used to be

For years, defense contractors treated NIST SP 800-171 as a checklist they could partially meet, write a POA&M for the rest, and report a self-assessed score in SPRS. That worked because nobody was checking. The CMMC Final Rule, published at 89 FR 83214 on October 15, 2024 and enforceable as of November 10, 2025, ended that arrangement for contracts that touch Controlled Unclassified Information.

The mechanism that ends it is third-party verification. Starting November 10, 2026, Phase 2 of the CMMC rollout makes a C3PAO certification assessment the default for Level 2 contracts involving CUI. A self-assessed score is no longer the finish line. An assessor will sit down with your System Security Plan and your evidence and score the 110 requirements against the assessment objectives in NIST SP 800-171A.

That changes what a POA&M is for. It is no longer a parking lot for everything you did not get to. It is a narrow, regulated path to a temporary pass, and 32 CFR 170.21 spells out exactly how narrow.

## The three conditions for a Conditional Level 2

Section 170.21 allows a POA&M only for requirements scored NOT MET, and only if all three of the following hold. Miss any one and there is no conditional path. You either pass clean or you fail.

**First, the score floor.** Your assessment score divided by the total number of Level 2 requirements must be at least 0.8. With 110 requirements, that is a minimum score of 88.

**Second, the point-value cap.** Nothing with a point value above 1, as scored under the CMMC Scoring Methodology in 32 CFR 170.24, can sit on a POA&M. The scoring methodology weights controls at 1, 3, or 5 points based on their security impact. The 3-point and 5-point controls are the high-impact ones: access control, multi-factor authentication, audit logging, boundary protection. None of them are deferrable.

**Third, the named exclusions.** Even among 1-point controls, six are excluded by name. More on those below.

![Two-column comparison of what a CMMC POA&M can carry: POA&M-eligible 1-point NOT MET items capped by the 88 of 110 score floor with a 180-day closeout, versus never-deferrable items including every 3 and 5-point control plus six named 1-point controls.](/blog/images/2-cmmc-poam-eligible-vs-cannot-defer.png)

## The 63 you cannot defer

When practitioners count it out against the rule, the deferrable set is small. Recent analyses of the scoring methodology put it at 47 controls that can go on a POA&M and 63 that cannot. The 63 are every 3-point and 5-point control, plus the six 1-point controls that 170.21 names out.

Those six, taken verbatim from 32 CFR 170.21(a)(2)(iii)(A) through (F), are:

- **AC.L2-3.1.20** External Connections
- **AC.L2-3.1.22** Control Public Information
- **CA.L2-3.12.4** System Security Plan
- **PE.L2-3.10.3** Escort Visitors
- **PE.L2-3.10.4** Physical Access Logs
- **PE.L2-3.10.5** Manage Physical Access

There is a logic to the list. These are the requirements that define and protect the CUI boundary itself: what connects to it, what information leaves it, who walks into the rooms where it lives, and the document that describes the whole system. The DoD's position is that if those are not in place, the rest of the assessment is built on sand, regardless of how few points the control is worth.

The System Security Plan exclusion deserves its own line. CA.L2-3.12.4 is not only ineligible for a POA&M, the SSP is a prerequisite for the assessment to proceed at all. An assessor cannot evaluate a system that has no documented description. If your SSP is incomplete, you do not get a low score on that control, you get an assessment that cannot start. It is the single most common blocker we see, and it is the reason the SSP is the first artifact worth getting right. The full walkthrough of what an assessor actually reads in an SSP is in our piece on {% raw %}{% post_url 2026-06-08-what-your-prime-is-actually-accepting-cmmc %}{% endraw %}.

## The one exception worth knowing

There is a single carve-out in the point-value cap. SC.L2-3.13.11, CUI Encryption, normally a higher-weighted control, may be placed on a POA&M if encryption is in use but is not yet FIPS-validated. In that specific situation it is treated as a 3-point item that the rule permits on the plan.

This is the only place where something above 1 point can be deferred, and it is conditional on encryption already being deployed. It is not a loophole for skipping encryption. It is an accommodation for the real-world gap between using cryptography and using cryptography that has cleared the FIPS 140 validation process.

## Your real margin is smaller than 88 of 110 sounds

The 88-point threshold sounds generous until you do the subtraction. A perfect score is 110. To stay at or above 88, your total point deductions cannot exceed 22. Because every deferrable item is worth exactly 1 point, that means you can carry at most 22 one-point gaps into the assessment and still qualify for a conditional status.

If you use the encryption exception, that 3-point deferral eats into the same budget, leaving room for roughly 19 one-point gaps. Cross the line and there is no negotiation. The assessor is not weighing your effort. The arithmetic either clears 88 or it does not.

![Graphic showing the two numbers that decide a Conditional CMMC cert: a score floor where MET must reach 88 of 110 leaving a 22-point cushion, and a 180-day closeout clock confirmed by a C3PAO after which conditional status expires.](/blog/images/3-cmmc-poam-180-day-margin-timeline.png)

This is also where an accurate SPRS score matters. The number you self-report is a representation to the government, and the gap between a generous self-score and a real one is exactly the kind of misstatement the Department of Justice has pursued under the False Claims Act. We covered how a SPRS score functions as a legal statement, not an IT metric, in {% raw %}{% post_url 2026-06-10-nist-800-171-sprs-score %}{% endraw %}.

## The 180-day clock

A conditional status is not a pass you keep. Under 32 CFR 170.21(b), every requirement on your POA&M must be closed within 180 days of the Conditional CMMC Status Date, and the closure has to be confirmed by a POA&M closeout assessment. For a Level 2 certification assessment, that closeout has to be performed by an authorized or accredited C3PAO, not self-attested.

Miss the 180-day window and the conditional status for that information system expires. You do not get an extension, and you do not quietly keep operating. You lose the status, which means you lose eligibility for the contracts that required it. Given that C3PAO scheduling already runs weeks to months, a closeout assessment is something you book early, not something you scramble for on day 170.

## What to do before you schedule

The contractors who get blindsided are the ones who walk into an assessment assuming they can clean up afterward. The work is to know your position before the assessor does.

- **Confirm your SSP is complete first.** CA.L2-3.12.4 is non-deferrable and gates the whole assessment. A documented system description, current and matching reality, is the prerequisite, not the cleanup item.
- **Score yourself honestly against 170.24.** Map each NOT MET requirement to its point value. The 3-point and 5-point gaps are your real problem because none of them can wait.
- **Separate the non-deferrable gaps from the rest.** Pull the six named controls and every 3 and 5-point control into one list. Those must be MET at assessment. Everything left is your POA&M candidate pool.
- **Count your cushion.** Add up the 1-point gaps you would carry. If the total exceeds 22 points (or about 19 if you are using the encryption exception), you will not clear 88, and no POA&M will save you. That tells you what to remediate now versus what can ride.
- **Book the closeout, not just the assessment.** The 180-day clock starts at conditional status. Treat the closeout assessment as a scheduled event from day one.

The five tools we use to run this exact process, an asset scoping worksheet, an SSP template, an SPRS scoring workbook, a POA&M tracker, and an evidence tracker, are bundled in the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147). If your blocker right now is the SSP, the [CMMC Level 2 System Security Plan (SSP) Template](https://payhip.com/b/gB6oD) ($77) is the document an assessor expects to read, and the [NIST 800-171 SPRS Score Workbook for CMMC Level 2](https://payhip.com/b/R5g4Y) ($87) is how you get the score that decides whether a POA&M is even on the table.

## The bottom line

A POA&M is a narrow exception, not a safety net. It earns a conditional status, never a clean one, and only for 1-point gaps that are not on the named-exclusion list, only if you are already at 88 of 110, and only for 180 days. Treating it as room to defer the hard controls is how contractors discover at the assessment that two-thirds of their gaps were never deferrable in the first place. Score yourself against the rule before you book the date, and the POA&M becomes what it was meant to be: a managed plan for a handful of low-impact items, not a bet on finishing later.

## Sources

- 32 CFR 170.21, Plan of Action and Milestones requirements (eCFR, current as of June 2026)
- 32 CFR 170.24, CMMC Scoring Methodology
- CMMC Program Final Rule, 89 FR 83214, October 15, 2024
- NIST SP 800-171 Rev. 2 and NIST SP 800-171A (assessment objectives)
- DoD CIO, CMMC phased rollout schedule (Phase 2 begins November 10, 2026)
