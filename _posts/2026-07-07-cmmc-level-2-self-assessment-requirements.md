---
layout: post
title: "CMMC Level 2 Self-Assessment: Requirements, Who Qualifies, and What Changes on November 10"
date: 2026-07-07
description: "CMMC Level 2 (Self) is appearing in live DoD solicitations right now, but you do not get to choose it. What 32 CFR 170.16 actually requires, how DFARS 252.204-7025 assigns your path, and why the window narrows after November 10, 2026."
category: CMMC
tags: [CMMC, NIST 800-171, SPRS, self-assessment, DFARS 252.204-7025, Level 2]
image: /blog/images/1-cmmc-level-2-self-assessment-requirements-hero.png
author: CyberZ
---

*Open a June 2026 sam.gov solicitation and you will find language like this: "A minimum of CMMC Level 2 (Self-Assessment) is required. Please complete a CMMC Level 2 Self-Assessment in Supplier Performance Risk System (SPRS) prior to award." The self-assessment path is real, it is in contracts right now, and most of the content written about it describes a process that no longer exists.*

**A CMMC Level 2 self-assessment is an internal evaluation, defined in 32 CFR 170.16, in which a contractor scores its own implementation of all 110 NIST SP 800-171 Revision 2 security requirements using the assessment objectives in NIST SP 800-171A, uploads the results to the Supplier Performance Risk System (SPRS), and affirms compliance annually. It produces a CMMC Status of Conditional or Final Level 2 (Self), which is a condition of contract award when a solicitation names it in DFARS provision 252.204-7025.**

<div style="border-left:4px solid #EE4C48;background:#18181c;padding:20px 24px;margin:28px 0;border-radius:4px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;line-height:1.65;color:#e6e6e6;">
<li>You do not choose the self-assessment path. The DoD program office or requiring activity assigns it, and the solicitation names it in DFARS 252.204-7025 before award.</li>
<li>Level 2 (Self) scores the exact same 110 NIST SP 800-171 R2 requirements as a C3PAO certification assessment, using the same 32 CFR 170.24 scoring methodology. What changes is who checks, not what is checked.</li>
<li>Conditional Level 2 (Self) requires a minimum score of 88 out of 110, a POA&M limited to 1-point requirements (with one narrow encryption exception), and a closeout self-assessment within 180 days or the status expires.</li>
<li>The status runs on two clocks: a full self-assessment every three years and an affirmation by a senior official every year in SPRS. Miss either and you are ineligible for award.</li>
<li>DoD's own estimates in the CMMC Program final rule put Level 2 (Self) at roughly 2% of contractors versus roughly 35% for Level 2 (C3PAO). After Phase 2 begins on November 10, 2026, C3PAO becomes the default condition of award for applicable CUI contracts.</li>
</ul>
</div>

## You Do Not Choose Self-Assessment. The Solicitation Does.

The most common misunderstanding in this niche is the idea that a contractor can look at the cost of a C3PAO assessment, decide it is too much, and elect to self-assess instead. The regulation is built the other way around.

Under DFARS 204.7503, the DoD program office or requiring activity, not the contractor and not even the contracting officer, determines the CMMC level and assessment type for each procurement based on the sensitivity of the information involved. That determination lands in your solicitation through DFARS provision 252.204-7025, Notice of Cybersecurity Maturity Model Certification Level Requirements, prescribed at DFARS 204.7504(b) for any solicitation that includes the 252.204-7021 clause.

The provision contains a single blank the contracting officer fills in with one of four values: CMMC Level 1 (Self), CMMC Level 2 (Self), CMMC Level 2 (C3PAO), or CMMC Level 3 (DIBCAC). That entry, or a higher status, is required prior to award for every contractor information system that will process, store, or transmit FCI or CUI during performance.

![The four possible CMMC level inserts in DFARS 252.204-7025](/blog/images/2-dfars-252-204-7025-cmmc-level-inserts.png)

Eligibility under 252.204-7025 comes down to two items, both of which must be current at the time of award: a CMMC Status in SPRS at the required level, and an affirmation of continuous compliance in SPRS. If either has lapsed, you are not eligible, no matter how strong your actual security posture is. We covered the mechanics of what primes and contracting officers actually verify in [what your prime is actually accepting]({% post_url 2026-06-08-what-your-prime-is-actually-accepting-cmmc %}).

## What a Level 2 Self-Assessment Actually Requires

Here is the part that surprises contractors who assumed "self" meant "lighter." Under 32 CFR 170.16, a Level 2 self-assessment evaluates the identical requirement set as a C3PAO certification assessment: all 110 security requirements of NIST SP 800-171 Revision 2, assessed against the objectives in NIST SP 800-171A, scored with the same CMMC Scoring Methodology in 32 CFR 170.24. Each requirement carries a weight of 1, 3, or 5 points, and every NOT MET requirement subtracts its full weight from the maximum score of 110. The floor is negative.

Two structural requirements sit underneath the scoring:

- **A System Security Plan must exist at the time of assessment.** 32 CFR 170.24 is explicit: the absence of an up-to-date SSP (requirement CA.L2-3.12.4) means the assessment cannot be completed at all. There is no score without an SSP, self-assessed or otherwise.
- **The results go into SPRS, with specifics.** 32 CFR 170.16 requires the SPRS entry to include, among other items, all CAGE codes associated with the information systems inside the CMMC Assessment Scope. The scope you declare is the scope DoD holds you to.

One more constraint that catches small contractors using cloud tools: if CUI touches a cloud environment under a Level 2 (Self) requirement, 32 CFR 170.16(a)(2) requires the cloud service offering to be FedRAMP Authorized at the Moderate baseline or higher, or to meet the equivalency conditions. Your Microsoft 365 or Google Workspace tier is a compliance question, not an IT preference.

![Level 2 Self lifecycle: assess, upload to SPRS, affirm annually, repeat every three years](/blog/images/3-cmmc-level-2-self-assessment-lifecycle-sprs.png)

## Conditional Status: The 88-Point Floor and the 180-Day Clock

A perfect 110 on the first pass earns Final Level 2 (Self). Anything less puts you into conditional territory, and conditional status has hard edges.

To achieve Conditional Level 2 (Self), your score must be at least 88 of 110, and every open item must sit on a POA&M that satisfies 32 CFR 170.21(a)(2). The POA&M rules are strict: only requirements worth 1 point are eligible, with a single exception for SC.L2-3.13.11 (CUI encryption), which may go on a POA&M at a 3-point deduction if encryption is employed but not FIPS-validated. Five-point requirements like multifactor authentication or FIPS-validated cryptography used incorrectly cannot be deferred at all. The full eligibility table is in our [POA&M eligibility breakdown]({% post_url 2026-06-17-cmmc-poam-eligibility %}).

Then the clock starts. A POA&M closeout self-assessment, covering every NOT MET item, must be performed and posted to SPRS within 180 days of the Conditional CMMC Status Date. Under 32 CFR 170.16(a)(1)(ii)(B), if the POA&M is not closed out in that window, the Conditional Level 2 (Self) status expires. If that happens during a contract's period of performance, standard contractual remedies apply and you are ineligible for further awards carrying the requirement until you achieve a new status. DFARS 252.204-7021 adds a currency rule on top: a conditional status older than 180 days no longer counts as current for award purposes.

## Two Clocks: Three Years and One Year

A Final Level 2 (Self) status is not a one-time event. It runs on two separate cycles, and most compliance failures happen in the gap between them.

The long clock: under 32 CFR 170.16, you must conduct a fresh Level 2 self-assessment and submit results in SPRS every three years to maintain the status.

The short clock: under 32 CFR 170.22, a named senior official, the Affirming Official, must affirm continuing compliance with all 110 requirements annually in SPRS, plus after every assessment and at POA&M closeout. That affirmation is a legal statement with False Claims Act exposure attached, which is exactly the pattern DOJ has been settling on since the Civil Cyber-Fraud Initiative began. We walked through the personal liability side in [the affirming official piece]({% post_url 2026-06-18-cmmc-affirming-official-personal-liability %}) and the full affirmation cycle in [the annual affirmation breakdown]({% post_url 2026-07-05-cmmc-annual-affirmation-requirements %}).

And self-assessed does not mean unwatched. 32 CFR 170.16(a)(1)(iv) reserves DoD's right to run a DCMA DIBCAC assessment of any self-assessed contractor. If DIBCAC's results contradict your SPRS entry, DIBCAC wins, your status is superseded, and you are ineligible for further Level 2 (Self) awards on that system until you earn a new status.

## Why Self-Assessment Is the Exception, Not the Rule

Here is the tension in the market right now. Solicitations posted in June 2026 are explicitly requiring Level 2 (Self) prior to award. At the same time, DoD's own regulatory analysis in the CMMC Program final rule (89 FR 83214) estimates that only about 2% of defense contractors will carry Level 2 self-assessment requirements, against roughly 35% needing a Level 2 C3PAO certification. Both facts are true, and the timeline explains them.

We are in Phase 1 of the rollout, which began November 10, 2025 under 32 CFR 170.3(e). During Phase 1, DoD includes Level 1 (Self) and Level 2 (Self) as conditions of award, with discretion to require C3PAO certification on specific procurements. Phase 2 begins November 10, 2026. From that date, DoD intends to include Level 2 (C3PAO) as a condition of award for applicable CUI contracts, with discretion to delay it to an option period.

Practically: the Level 2 (Self) lane exists, it is narrow, and it narrows further in four months. If your contracts involve CUI on anything DoD considers prioritized, plan for C3PAO and treat a self-assessment requirement as a head start, not a destination. The 110 requirements, the SSP, the SPRS score, and the evidence you build for a self-assessment are the same artifacts a C3PAO will examine later. Nothing is wasted. Skipping the DFARS 7019/7020 history is deliberate here; that framework was retired in early 2026, and we covered what replaced it in [the 7019 deletion piece]({% post_url 2026-06-16-dfars-7019-deleted-sprs-score %}).

## What to Do This Week

1. **Pull your active solicitations and check the 252.204-7025 entry.** The four words in that blank are your requirement. Do not plan around what you hope it says.
2. **Score yourself against all 110 requirements using the 800-171A objectives.** Not a gut check. The actual 320 assessment objectives, requirement by requirement, with the 1/3/5 weighting applied.
3. **Confirm your SSP is current before you score.** No SSP, no completable assessment, at any level.
4. **Map every NOT MET item against POA&M eligibility.** If a 3-point or 5-point requirement is open, you cannot reach even conditional status until it is fixed. Sequence remediation accordingly.
5. **Put both clocks on the calendar now.** The annual affirmation date and the three-year reassessment date, with owners attached.

If you want the scoring done in a structured way instead of a blank spreadsheet, the [NIST 800-171 SPRS Score Workbook for CMMC Level 2](https://payhip.com/b/R5g4Y) ($87) walks all 110 requirements with the official weighting and produces the score you enter in SPRS. If you are starting from further back, with scoping, SSP, and evidence still open ahead of a November deadline, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) bundles the scoping worksheet, SSP template, SPRS workbook, POA&M tracker, and evidence tracker into one working set.

## Sources

- [32 CFR 170.16, CMMC Level 2 self-assessment and affirmation requirements (eCFR)](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.16)
- [32 CFR 170.21, Plan of Action and Milestones requirements (eCFR)](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.21)
- [32 CFR 170.24, CMMC Scoring Methodology (eCFR)](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.24)
- [32 CFR Part 170, CMMC Program, including 170.3(e) phased implementation (eCFR)](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170)
- [DFARS 252.204-7025, Notice of Cybersecurity Maturity Model Certification Level Requirements (acquisition.gov)](https://www.acquisition.gov/dfars/252.204-7025-notice-cybersecurity-maturity-model-certification-level-requirements.)
- [DFARS 252.204-7021, Contractor Compliance With the CMMC Level Requirements (acquisition.gov)](https://www.acquisition.gov/dfars/252.204-7021-contractor-compliance-cybersecurity-maturity-model-certification-level-requirements.)
- [DFARS Subpart 204.75, Cybersecurity Maturity Model Certification (acquisition.gov)](https://www.acquisition.gov/dfars/subpart-204.75-cybersecurity-maturity-model-certification)
- [Cybersecurity Maturity Model Certification (CMMC) Program final rule, 89 FR 83214 (Federal Register, Oct 15, 2024)](https://www.federalregister.gov/documents/2024/10/15/2024-22905/cybersecurity-maturity-model-certification-cmmc-program)
- [CMMC Assessment Guide, Level 2 (DoD CIO)](https://dodcio.defense.gov/Portals/0/Documents/CMMC/AssessmentGuideL2.pdf)
