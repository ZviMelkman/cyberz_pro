---
layout: post
title: "The CMMC POA&M Closeout Self-Assessment: Your Conditional Level 2 (Self) Status Expires on Day 181"
date: 2026-09-22
description: "A Conditional Level 2 (Self) posted in SPRS on March 26, 2026 expires today. 32 CFR 170.16 gives a contractor 180 days to remediate every POA&M item, run a POA&M closeout self-assessment, post the result, and affirm again. What the closeout actually involves, what expiry does to contract eligibility, and a 30-day plan for a small shop that has not scheduled it."
category: CMMC
tags: [CMMC, POA&M, POA&M closeout, Conditional Level 2, Level 2 self-assessment, 32 CFR 170.16, 32 CFR 170.21, SPRS, affirmation, defense contractors]
image: /blog/images/1-cmmc-poam-closeout-self-assessment-hero.png
author: CyberZ
---

*Phase 1 of CMMC opened on November 10, 2025. A contractor that posted a Conditional Level 2 (Self) in SPRS that first week had until May 9, 2026 to close its POA&M. One that posted on March 26, 2026 has until today. Most of them built a remediation list. Fewer put the closeout self-assessment on a calendar, and the rule treats those as two different things.*

**Under 32 CFR 170.16(a)(1)(ii)(B), a contractor with a Conditional Level 2 (Self) CMMC Status must remediate every NOT MET requirement on its POA&M, perform a POA&M closeout self-assessment, and post the compliance results to SPRS within 180 days of the Conditional CMMC Status Date. 32 CFR 170.21(b) defines the closeout as a CMMC assessment of only the POA&M items, performed "in the same manner as the initial self-assessment," and 32 CFR 170.22(a) requires a fresh affirmation from the Affirming Official when it is done. If the closeout is not completed and posted inside the window, the Conditional status expires, the contractor becomes ineligible for further awards that require Level 2 (Self) or higher for that system, and if the expiry lands inside a contract's period of performance, standard contractual remedies apply. The July 13 suspension of Phase 2 and the September 3 class deviation changed which assessment type contracts require. They did not touch this clock.**

<div class="key-takeaways" style="border-left:4px solid #EE4C48;background:#15151a;padding:18px 24px;margin:28px 0;border-radius:6px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;">
<li>The 180 days run from the Conditional CMMC Status Date in SPRS, not from the day you started fixing things. SPRS itself labels a Conditional Level 2 (Self) as valid for 180 days. A Final Level 2 (Self) is valid for three years.</li>
<li>The closeout is an assessment, not a status update. 32 CFR 170.21(b)(1) requires it to be performed the same way as the initial self-assessment: NIST SP 800-171A objectives, evidence in final form, scored under 32 CFR 170.24.</li>
<li>Three things have to happen inside the window: remediate, assess, post. Then 32 CFR 170.22(b)(2) requires the Affirming Official to submit a new affirmation for the closeout.</li>
<li>Expiry is not a warning. 32 CFR 170.16(a)(1)(ii)(B) makes the contractor ineligible for additional awards requiring Level 2 (Self) or higher for that system until a new CMMC Status is achieved, and applies standard contractual remedies if it happens mid-contract.</li>
<li>The three-year re-assessment cycle also runs from the Conditional date, not the Final date. Closing out late does not reset it.</li>
<li>Nothing in the Phase 2 suspension, the September 3 class deviation, or the Task Force review reaches 32 CFR 170.16. Every Phase 1 conditional posted since November 10, 2025 is on this clock.</li>
</ul>
</div>

## What a conditional status bought you, and for how long

The [POA&M eligibility rules]({% post_url 2026-06-15-cmmc-poam-eligibility-what-you-can-defer %}) covered what can go on the list in the first place: a score of at least 88 of 110, only one-point requirements (plus non-FIPS encryption at three points), and six requirements barred by name. Clear those gates during a Level 2 self-assessment and 32 CFR 170.16(a)(1)(ii) gives you a CMMC Status of Conditional Level 2 (Self).

That status is a real thing. Under 32 CFR 170.16(b), a Conditional Level 2 (Self) plus an affirmation in SPRS is enough to be eligible for award on a contract that requires Level 2 (Self). Since the [September 3 class deviation]({% post_url 2026-09-10-cmmc-phase-2-class-deviation %}) directed contracting officers to strip third-party assessment requirements out of solicitations, Level 2 (Self) is what most CUI contracts now ask for. So a conditional status is, right now, a contract-winning status.

It is also a short one. DoD's own SPRS Quick Entry Guide for Level 2 self-assessments states the two validity periods side by side: a Conditional Level 2 (Self) is valid for 180 days, a Final Level 2 (Self) with annual affirmations is valid for three years. The regulation puts it in one sentence at 32 CFR 170.16(a)(1)(ii)(B):

> The OSA must remediate any NOT MET requirements, must perform a POA&M closeout self-assessment, and must post compliance results to SPRS within 180 days of the CMMC Status Date associated with the Conditional Level 2 (Self).

Three verbs. Remediate, perform, post. The window closes on all three at once.

One more detail from the same section that contractors routinely miss: the three-year re-assessment cycle in 32 CFR 170.16(a)(1) runs "within three years of the CMMC Status Date associated with the Conditional Level 2 (Self)." Not the Final date. A shop that posts a conditional in March and closes out in September owes its next full self-assessment by March three years later, not September. The conditional date is the anchor for everything that follows.

![Timeline of a Conditional Level 2 (Self) under 32 CFR 170.16: day 0 the conditional status is posted in SPRS, day 180 is the last day to post the POA&M closeout, and on day 181 the status has expired to No CMMC Status](/blog/images/2-cmmc-conditional-level-2-self-180-day-expiry-timeline.png)

## Day 181

The consequence is written into the same paragraph, and it is worth reading slowly because it has three parts.

> If the POA&M is not successfully closed out within the 180-day timeframe, the Conditional Level 2 (Self) CMMC Status for the information system will expire. If Conditional Level 2 (Self) CMMC Status expires within the period of performance of a contract, standard contractual remedies will apply, and the OSA will be ineligible for additional awards with a requirement for the CMMC Status of Level 2 (Self), or higher requirement, for the information system within the CMMC Assessment Scope until such time as a new CMMC Status is achieved.

**Part one: the status expires.** Not "is flagged." Not "moves to a grace period." In SPRS terms, the system goes back to No CMMC Status. The DoD Quick Entry Guide notes that the same No CMMC Status result applies when a NOT MET requirement is not POA&M-eligible, regardless of score. An expired conditional and a failed initial assessment land in the same place.

**Part two: standard contractual remedies if it expires mid-contract.** The rule does not spell out which remedies. It does not have to. A contract that required Level 2 (Self) at award now has a contractor that no longer holds it. What the contracting officer does with that is a contracting question, and a small subcontractor's prime will usually answer it first. The [prime flow-down piece]({% post_url 2026-06-08-what-your-prime-is-actually-accepting-cmmc %}) covered how primes are already policing CMMC status in their supplier portals. An expired conditional is exactly the kind of change a prime's compliance team is watching for.

**Part three: ineligible for additional awards until a new status is achieved.** The rule does not bar a new self-assessment. It does say the old conditional is gone, and a new CMMC Status has to be earned from scratch. The contractor is back at the starting line with the same 110 requirements, the same 88-point floor, and the same eligibility gates, plus a SPRS history that now shows a conditional that ran out.

None of this touches DFARS 252.204-7012. The obligation to implement NIST SP 800-171 Rev 2 for any system handling covered defense information has been in force since 2017 and does not depend on CMMC status at all. Expiry removes eligibility. It does not remove the duty.

## The closeout is an assessment, not a checkbox

This is the part that separates a contractor who scheduled the closeout from one who only scheduled the remediation.

32 CFR 170.21(b) defines the POA&M closeout assessment as "a CMMC assessment that assesses only the NOT MET requirements that were identified with POA&M in the initial assessment." Then 170.21(b)(1) sets the standard for the self-assessment version: it "shall be performed by the OSA in the same manner as the initial self-assessment."

Same manner means the same procedure 32 CFR 170.16(c)(1) required the first time:

- **Assessed against NIST SP 800-171A objectives**, not against the requirement statement. A POA&M item for AC.L2-3.1.9 (privacy and security notices) is not MET until both of its assessment objectives, identifying the required notices and displaying them, are satisfied.
- **Scored under 32 CFR 170.24.** And 170.24(b)(1) is unambiguous about evidence: MET means every applicable objective is satisfied "based on evidence," all evidence "must be in final form and not draft," and working papers, drafts, and unapproved policies are named as unacceptable. A policy that was approved in principle but not signed is still a NOT MET at closeout.
- **Documented like an assessment.** The [self-assessment evidence guide]({% post_url 2026-07-22-nist-800-171-self-assessment-evidence %}) covered what "examine, interview, test" looks like when there is no assessor in the room. The closeout uses the same three methods on the items that were open. Artifact retention under 32 CFR 170.16(c)(4) is six years from the CMMC Status Date, and that covers the closeout artifacts too.

The scope is narrow, which is the good news. A closeout does not re-run the other 100-odd requirements. But a narrow assessment done to a lower standard is not a closeout under the rule; it is a remediation log with a date on it. If a DCMA DIBCAC assessment under 32 CFR 170.16(a)(1)(iv) later finds that a closed-out item was never actually implemented, those results take precedence over the self-assessed status, and the contractor is back to No CMMC Status with an affirmation on file that said otherwise.

![The four steps of a CMMC POA&M closeout self-assessment under 32 CFR 170.21(b): remediate every POA&M item, re-assess only those items against NIST SP 800-171A objectives with final evidence, post the closeout results to SPRS, and have the Affirming Official submit a new affirmation](/blog/images/3-cmmc-poam-closeout-self-assessment-four-steps.png)

## The second signature

The closeout ends with the same person it started with. 32 CFR 170.22(a) requires the Affirming Official to affirm continuing compliance "after every assessment, including POA&M closeout, and annually thereafter." Section 170.22(a)(3) lists four triggers for a submission, and "following a POA&M closeout assessment" is one of them. Section 170.22(b)(2) repeats it for Level 2 self-assessments specifically: an affirmation "shall also be submitted at the completion of a POA&M closeout self-assessment."

So the Affirming Official signs twice on a conditional path. Once at the conditional status, attesting to an 88-plus score with a compliant POA&M. Again at closeout, attesting that every item on that POA&M is now implemented and the score is 110. The [affirming official liability piece]({% post_url 2026-08-23-cmmc-affirmation-false-claims-act %}) covered what that signature is worth under the False Claims Act. The closeout affirmation is the stronger of the two statements, because it says the gaps are gone.

DOJ's June 18, 2026 settlement with LOGZONE Inc. is the reference point for what happens when the government checks. The Huntsville contractor paid $507,144 after a DCMA assessment scored its NIST SP 800-171 implementation at negative 170, against contracts on which it had represented compliance from May 2021 to March 2025. The settlement press release does not mention a POA&M, and there is no need to invent one. The point is simpler: the affirmation says the controls are in, and a government assessor can come and count.

## Two lists that look alike and are not

There is a trap in 32 CFR 170.24 that matters at closeout, and the [SSP update piece]({% post_url 2026-09-17-cmmc-ssp-update-requirements %}) only touched it in passing.

32 CFR 170.24(b)(1)(ii) says that "temporary deficiencies that are appropriately addressed in operational plans of action," meaning ones that include deficiency reviews and show progress toward correction, "shall be assessed as MET." Two paragraphs later, 170.24(c)(2)(i)(B)(6) says that for each NOT MET requirement the contractor must have a POA&M, that a POA&M "is not a substitute for a completed requirement," and that a requirement not implemented "whether described in a POA&M or not, is assessed as NOT MET."

Read together: a control that is implemented and operating, with a known temporary gap that is being tracked and closed under an operational plan of action (a patch cycle running late, a configuration exception with a review date), is MET. A control that is not implemented, with a plan to implement it, is NOT MET and belongs on the 170.21 POA&M with the 180-day clock attached.

The trap is at closeout, when an item that was on the POA&M is still not finished on day 170 and someone proposes moving it to the "operational" list to get to 110. That is not what 170.24(b)(1)(ii) describes. The temporary-deficiency language applies to a requirement that has been implemented and has a transient gap in its operation. It does not convert an unimplemented requirement into an implemented one. Reclassifying an open POA&M item that way, and then affirming a score of 110 on the strength of it, produces the exact gap between what was said and what is true that the [self-disclosure piece]({% post_url 2026-09-14-sprs-score-wrong-self-disclosure %}) covered from the other end.

The honest version is less comfortable and much safer: the item is still NOT MET, the closeout cannot be completed, and the conditional expires. That is a bad outcome. It is a recoverable one.

## What the suspension changed, and what it did not

The July 13 memorandum suspended Phase 2 and the requirement for C3PAO certification assessments. The September 3 class deviation put that suspension into contract regulation. The CMMC Reform Task Force sent its report to the Department of War CIO on or about September 11, and as of this week the report has not been made public.

None of those instruments amend 32 CFR Part 170. The eCFR text of sections 170.16, 170.21, and 170.22, current as of September 18, 2026, contains every sentence quoted in this article. The [Task Force piece]({% post_url 2026-09-03-cmmc-task-force-report-what-changes %}) covered why a memo cannot change a regulation. The practical consequence for this article is narrow: every contractor that posted a Conditional Level 2 (Self) at any point since Phase 1 opened on November 10, 2025 is on a 180-day clock that no announcement has paused.

If anything, the suspension made the conditional path more common. With C3PAO assessments off the table, the [Level 2 self-assessment]({% post_url 2026-07-07-cmmc-level-2-self-assessment-requirements %}) is the only route to a Level 2 status on new awards, and a self-assessment that scores 88 with a compliant POA&M is a faster way to become eligible than waiting for 110. More conditionals means more closeouts due, most of them in shops that have never run one.

## The 30-day closeout run for a small shop

A 20-person subcontractor with six items on its POA&M and eight weeks left can do this in a month if it treats the closeout as a project with a due date and not as the natural end of the remediation work.

1. **Pull the Conditional CMMC Status Date from SPRS and write down day 180.** Not "roughly six months." The date. If the status was posted on March 26, day 180 is September 22. If you are reading this after the date has passed, skip to step seven.
2. **Freeze the POA&M item list.** The closeout assesses "only the NOT MET requirements that were identified with POA&M in the initial assessment." Items that were POA&M'd are in. Nothing else is. If a new gap has surfaced since the initial assessment, it is an SSP and score problem, not a closeout item, and the [SPRS completion-date piece]({% post_url 2026-09-15-sprs-plan-of-action-completion-date %}) covers that separately.
3. **For each item, finish the implementation, then write the SSP statement.** The SSP has to describe how the requirement is now met, in the present tense, before the assessment step. An SSP that still says "planned Q3 2026" for an item you are about to close is a 3.12.4 problem on top of a closeout problem.
4. **Assess each item against its 800-171A objectives, one line per objective, with the evidence named.** This is the closeout. Examine the artifact. Interview the person who operates the control. Test it where testing applies. Record the result the way the initial self-assessment recorded it. If any objective is not satisfied on evidence in final form, the item stays NOT MET and step six does not happen.
5. **Recompute the score under 170.24.** With every POA&M item MET, it is 110. If it is not 110, one of the items is not closed.
6. **Post the closeout results to SPRS and route the record to the Affirming Official.** The regulation requires the compliance results posted within the window; the SPRS Quick Entry Guide walks through entry and transfer to the AO. The AO then submits the closeout affirmation required by 32 CFR 170.22(b)(2). Brief them first. They are attesting that six specific gaps are gone, and they should be able to name them.
7. **If day 180 is going to pass with an item open, do not paper it.** Let the conditional expire, finish the implementation properly, and post a new Level 2 self-assessment when it is true. The rule bars nothing here except a false affirmation. Tell your prime before SPRS tells them.

## The bottom line

A conditional status is a contract-eligible status with a fixed expiry, and the thing that prevents the expiry is a second assessment, posted and affirmed, not a finished to-do list. The rule that governs it has not moved since December 2024, and no suspension or task force report has reached it. Every Phase 1 conditional is on the clock, and the first ones ran out in May.

If your POA&M lives in a spreadsheet that tracks the fix but not the clock, the [CMMC Level 2 POA&M Tracker for NIST 800-171](https://payhip.com/b/HTzXf) ($57) flags eligibility per control under 32 CFR 170.21 and runs the 180-day closeout countdown from your status date. If the closeout is going to touch your SSP implementation statements, your evidence index, and your SPRS score in the same month, which it will, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) keeps the POA&M, the SSP, the evidence tracker, and the score workbook pointed at one set of facts so the Affirming Official is signing over the same numbers you assessed.

## Sources

- 32 CFR § 170.16, CMMC Level 2 self-assessment and affirmation requirements (eCFR, current as of September 18, 2026)
- 32 CFR § 170.21, Plan of Action and Milestones requirements (eCFR)
- 32 CFR § 170.22, Affirmation (eCFR)
- 32 CFR § 170.24, CMMC Scoring Methodology (eCFR)
- U.S. Department of Defense, SPRS, "CMMC Level 2 Self-Assessment Quick Entry Guide," Version 4.0, February 2025
- U.S. Department of Justice, press release, "Alabama Defense Contractor Agrees to Pay $507,144 to Resolve False Claims Act Liability Relating to Cybersecurity Violations," June 18, 2026
- Class Deviation 2026-O0025, Revision 3, September 3, 2026 (as covered in the September 10 CyberZ post)
- Covington & Burling, Inside Government Contracts, "CMMC Reform Task Force Updates September 2026," September 21, 2026
- NIST SP 800-171 Rev 2 and NIST SP 800-171A
