---
layout: post
title: "CMMC SSP Update Requirements: How Often, What Triggers It, and Who Decides"
date: 2026-09-17
description: "NIST SP 800-171 requirement 3.12.4 says to update the system security plan 'periodically.' 32 CFR 170.24 says an assessment cannot be completed without an up to date SSP. What the rules actually require, the changes that force an update, and a one-page annual review routine for small defense contractors."
category: CMMC
tags: [CMMC, system security plan, SSP, CA.L2-3.12.4, NIST 800-171, 32 CFR 170.24, annual affirmation, significant change, SPRS, defense contractors]
image: /blog/images/1-cmmc-ssp-update-requirements-hero.png
author: CyberZ
---

*Most system security plans are accurate on the day they are finished and wrong a little more every month after that. Nobody decides to let it happen. The network changes, the MSP changes, the person who wrote the thing leaves, and the document keeps describing a company that used to exist. Then an executive signs an affirmation under it.*

**NIST SP 800-171 Rev 2 requirement 3.12.4 requires a contractor to develop, document, and "periodically update" its system security plan (SSP). Neither NIST nor 32 CFR Part 170 sets a number of months. The contractor defines its own update frequency in the SSP, and NIST SP 800-171A objectives 3.12.4[g] and 3.12.4[h] then assess whether that frequency is defined and whether it was met. The DoD CMMC Assessment Guide for Level 2 lists a defined update frequency of at least annually as a minimum SSP element. Separately, 32 CFR 170.24 states that the absence of an up to date SSP means an assessment cannot be completed at all, and 32 CFR 170.21 bars CA.L2-3.12.4 from any POA&M. In practice that means two duties: a scheduled review at least once a year, and an immediate update whenever the environment stops matching the document.**

<div class="key-takeaways" style="border-left:4px solid #EE4C48;background:#15151a;padding:18px 24px;margin:28px 0;border-radius:6px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;">
<li>There is no regulatory number. Requirement 3.12.4 says "periodically." You set the frequency in your own SSP, and NIST SP 800-171A objectives 3.12.4[g] and [h] test whether you defined it and kept to it. DoD's Level 2 Assessment Guide treats at least annually as the floor.</li>
<li>The frequency you wrote down is the standard you are held to. An SSP that promises quarterly review and shows a last-reviewed date from 2024 fails 3.12.4[h] on its own evidence.</li>
<li>32 CFR 170.24(c)(2)(i)(B)(5) requires an "up to date" SSP at the time of assessment. Without one, the finding is that the assessment could not be completed. 32 CFR 170.21(a)(2)(iii) bars CA.L2-3.12.4 from a POA&M, so a stale SSP cannot be deferred.</li>
<li>The CMMC Level 2 Scoping Guide draws the line that matters between reviews: operational changes that follow the existing SSP are covered by the annual affirmation. Architectural or boundary changes require a new assessment. Everything in between requires an SSP revision now, not at the next review.</li>
<li>Several pages ranking for this question still cite DFARS 252.204-7019 for a three-year cycle. That clause was eliminated on February 1, 2026. The three-year self-assessment cycle lives in 32 CFR 170.16 and the annual affirmation in 32 CFR 170.22.</li>
</ul>
</div>

## What the rule says, and what it leaves to you

Requirement 3.12.4 in NIST SP 800-171 Rev 2 is one sentence. Develop, document, and periodically update system security plans that describe system boundaries, system environments of operation, how security requirements are implemented, and the relationships with or connections to other systems.

The word carrying the weight is "periodically," and NIST declines to define it. The definition shows up one document over, in NIST SP 800-171A, which breaks each requirement into the objectives an assessor actually tests. Requirement 3.12.4 has eight. The last two are the ones this article is about:

- **3.12.4[g]:** the frequency to update the system security plan is defined.
- **3.12.4[h]:** the system security plan is updated with the defined frequency.

Read those together and the structure is plain. The government does not tell you how often. It tells you to pick a number, write it down, and then holds you to your own number. An assessor, or you during a self-assessment, checks [g] by finding the sentence in the SSP that states the review cycle. They check [h] by looking for proof the cycle happened: a revision history, a dated approval, a change log.

The DoD CMMC Assessment Guide for Level 2 (version 2.13) narrows the choice. Its list of minimum SSP contents ends with a defined frequency of updates of at least annually, and its worked example for this requirement describes an organization that sets a policy requiring a formal review and update of the SSP each year to satisfy objectives [g] and [h]. The guide is not regulation and says so on its notices page. It is, however, what every C3PAO and DIBCAC assessor reads before they read you.

So the honest answer to "how often" has two parts. The regulation says as often as you said. DoD's guidance says that had better be at least once a year.

### The trap in your own document

Many SSPs were written from templates that promise more than the company delivers. "This plan is reviewed quarterly and upon any change to the system." It sounds diligent. If the revision table underneath shows one entry from the month the consultant delivered it, that sentence is now evidence against you. Objective [h] is assessed against the frequency you defined, so an ambitious cycle you did not keep is worse than a modest one you did.

Pick a cycle you will actually run. Annual, tied to a fixed month, with event-driven updates in between, is defensible and achievable for a 25-person shop. Then keep the log.

## Why "stale" is treated the same as "missing"

The [SSP template guide]({% post_url 2026-06-09-cmmc-ssp-template %}) from June covers why the SSP is the first thing an assessor opens. The scoring rule explains what happens when it does not match what they find.

32 CFR 170.24(c)(2)(i)(B)(5) requires an SSP "in place at the time of assessment to describe each information system within the CMMC Assessment Scope," and says the absence of an up to date SSP results in a finding that the assessment could not be completed due to incomplete information and noncompliance with DFARS 252.204-7012. The phrase is "up to date," not merely "existing." A plan that describes last year's network is, for scoring purposes, the absence of a plan for this year's.

Two more provisions close the exits:

- **No POA&M.** 32 CFR 170.21(a)(2)(iii) names CA.L2-3.12.4 among the six requirements that can never sit on a Level 2 POA&M. The [POA&M eligibility breakdown]({% post_url 2026-06-15-cmmc-poam-eligibility-what-you-can-defer %}) lists all six. You cannot score the SSP as NOT MET and promise to fix it in 180 days.
- **No drafts.** 32 CFR 170.24(b)(1) says all evidence must be in final form, and lists working papers, drafts, and unapproved policies as unacceptable. An SSP marked "v3 DRAFT, pending review" is not an SSP.

This applies to self-assessment exactly as it applies to a C3PAO. The [Level 2 self-assessment requirements]({% post_url 2026-07-07-cmmc-level-2-self-assessment-requirements %}) use the same 170.24 methodology, and since the [September 3 class deviation]({% post_url 2026-09-10-cmmc-phase-2-class-deviation %}) made self-assessment the codified default for CUI work, the person applying that rule to your SSP is you.

![Three tiers of change under the CMMC Level 2 Scoping Guide: operational changes that follow the SSP are covered by the annual affirmation, changes the SSP does not describe need a revision now, and boundary changes need a new assessment](/blog/images/2-cmmc-ssp-update-triggers-significant-change.png)

## What forces an update between reviews

The annual review is the floor. The harder question is what happens in month four, when something changes. DoD's CMMC Level 2 Scoping Guide gives the most useful line in the whole program on this point. A new assessment is required if there are significant architectural or boundary changes to the previous CMMC Assessment Scope, with network expansions and mergers and acquisitions given as examples. Operational changes within the scope, such as adding or subtracting resources inside the existing boundary that follow the existing SSP, do not require a new assessment and are covered by the annual affirmation.

The phrase to notice is "that follow the existing SSP." It sorts every change into one of three tiers.

**Tier 1: the change follows the SSP.** You add four laptops built from the same baseline, enrolled in the same MDM, on the same network segment the SSP already describes. Update the asset inventory. The SSP narrative is still true.

**Tier 2: the change is not described in the SSP.** This is where most small contractors drift, because none of these feel like compliance events when they happen:

- **A new or replaced MSP, MSSP, or other external service provider.** 32 CFR 170.16(c)(3)(i) requires that the use of the ESP, its relationship to you, and the services provided are documented in your SSP. Switch providers and the old SSP names a company that no longer has your admin credentials. The [ESP requirements guide]({% post_url 2026-07-12-cmmc-external-service-provider-requirements %}) covers the rest.
- **A new cloud service touching CUI.** 32 CFR 170.16(c)(2)(iii) requires the customer responsibility matrix requirements to be documented or referenced in the SSP.
- **A new tool in a security function.** New EDR, new SIEM, new MFA vendor, new backup product. Each one changes how at least one requirement is implemented, which is the core content 3.12.4 asks the SSP to describe.
- **A new way CUI enters, moves, or leaves.** A new prime portal, a new file transfer method, a new site, a newly remote engineer.
- **Roles.** The system owner, the ISSO, or the affirming official named in the plan has left or changed jobs.
- **A closed POA&M item.** The control moved from planned to implemented. The SSP should now describe the implementation, and the score in SPRS should change with it. The [SPRS completion date piece]({% post_url 2026-09-15-sprs-plan-of-action-completion-date %}) covers that half.
- **A newly categorized asset.** 32 CFR 170.19 requires Contractor Risk Managed Assets and Specialized Assets to be documented in the SSP. A new CNC controller or test stand on the CUI floor belongs there.

Tier 2 changes require an SSP revision when they happen. Waiting for the annual review means every day in between, the document an executive affirmed no longer describes the system.

**Tier 3: the boundary itself moved.** Migrating from on-premises to a cloud enclave, absorbing an acquired company's network, collapsing an enclave into the corporate LAN. Per the Scoping Guide, this is new-assessment territory. For a Level 2 (Self) contractor that means re-running the self-assessment against the new scope and posting the new result, not editing a paragraph. The [scoping decision guide]({% post_url 2026-07-19-cmmc-scoping-decision-not-controls %}) covers why the boundary drives everything downstream.

One provision makes the point sharper than any commentary could. Under 32 CFR 170.24(c)(2)(i)(B)(8), a requirement that the DoD CIO has adjudicated as met by an alternative measure is assessed as MET only "if there have been no changes in the environment." Even a formal government ruling in your favor expires when the environment it described stops existing.

## Who decides whether a change is significant

The DoD CIO's CMMC FAQ takes this up directly at question C-Q12. It explains that the three-year assessment cycle and the annual affirmation are designed to accommodate normal change, and it places the judgment about whether a particular change is significant on the affirming official, who carries the contractual and legal risk of the continuing-compliance statement.

That allocation is worth sitting with. The person who decides whether your cloud migration needed a new assessment is the same person who signs the affirmation in SPRS under 32 CFR 170.22, and the same person a False Claims Act complaint will name. The [affirmation liability breakdown]({% post_url 2026-08-23-cmmc-affirmation-false-claims-act %}) covers that exposure in full. The practical consequence for SSP maintenance is simple: every Tier 2 or Tier 3 call should be written down, dated, and signed off by the affirming official at the time, with the reasoning. "We assessed this change on March 3 and concluded it follows the existing SSP because..." is a defensible record. Silence is not.

## Why this matters more after the suspension

A year ago the plan for most CUI contractors was that a C3PAO would eventually read the SSP against the environment and catch the drift. Under the class deviation that reader is gone for new awards. The only scheduled event left in which anyone senior attests that the documented system matches the real one is the annual affirmation.

The Justice Department has been explicit about what it does with documents that do not match reality. On May 1, 2025, Raytheon, RTX, and Nightwing agreed to pay $8.4 million to resolve allegations that, among other things, Raytheon failed to develop and implement a system security plan for an internal development system used on DoD contracts between 2015 and 2021. In June 2026, LOGZONE paid $507,144 over a self-assessment score a DoD audit found inaccurate. Neither case involved a breach. Both were about the gap between what was represented and what existed.

The SSP is where that gap is either closed or recorded. The SPRS score is calculated from it. The affirmation is signed over it. If a whistleblower or a DIBCAC team ever compares the three, the SSP is the exhibit. The [self-disclosure piece]({% post_url 2026-09-14-sprs-score-wrong-self-disclosure %}) covers what to do when the comparison has already gone wrong. This piece is about not getting there.

![A one-page annual SSP review: walk the boundary, read each implementation statement against the live environment, reconcile the POA&M and SPRS score, then sign and date the revision](/blog/images/3-ssp-annual-review-cmmc-checklist.png)

## The annual review, in one sitting

Searches for this topic end in the words "sample" and "example," so here is one. This is a half-day exercise for a small contractor, scheduled 30 to 45 days before the affirmation date so there is time to fix what it finds.

1. **Walk the boundary.** Put the network diagram and asset inventory next to what is actually plugged in, enrolled, and licensed. New sites, new segments, new cloud tenants, new specialized assets. If the diagram is wrong, stop and decide which tier the change belongs to before going further.
2. **Reconcile the people and the providers.** Every named role and every ESP in the SSP: still here, still doing that job, still under the same contract and responsibility matrix.
3. **Read every implementation statement against the live environment.** All 110. The test for each is whether the sentence is true today using the tool named in it. Strike anything aspirational. "Will implement" language in the body of an SSP is a POA&M item hiding in the wrong document.
4. **Reconcile the POA&M and the score.** Closed items move into the SSP as implemented. Open items get real dates. Recompute the SPRS score from the corrected SSP using the 170.24 point values, and if the number moved, update SPRS. The [SPRS score guide]({% post_url 2026-09-06-how-to-improve-sprs-score %}) covers the arithmetic.
5. **Record it.** New version number, review date, a change log with date, description, and responsible party for each edit, and an approval signature. Remove "draft" from every header. This log is your evidence for 3.12.4[h].
6. **Brief the affirming official before they sign.** Show them the change log and the tier decisions made during the year. The [annual affirmation walkthrough]({% post_url 2026-07-05-cmmc-annual-affirmation-requirements %}) covers the SPRS mechanics. The briefing is what makes the signature informed.

Then set two calendar entries: the same review next year, and a standing item on whatever meeting approves IT purchases, asking one question of each change. Does this follow the SSP?

## The bottom line

The update requirement for a CMMC SSP is lighter on its face than most contractors assume and heavier in effect. The regulation sets no interval. It asks you to choose one, and DoD's guidance expects at least annual. Then it treats an SSP that has fallen behind the environment as no SSP at all under 32 CFR 170.24, refuses to let you defer it under 170.21, and leaves the judgment about significant change with the executive who signs the affirmation. With third-party assessments out of new contracts, that yearly signature is the only scheduled accounting left, and the SSP is the book it is taken from. It should say what is true on the day it is signed.

If your SSP started life as a consultant's deliverable or a free template and has not been opened since, the [CMMC Level 2 System Security Plan (SSP) Template](https://payhip.com/b/gB6oD) ($77) is structured around all 110 requirements and their 800-171A objectives, with the revision history and review-frequency sections that objectives [g] and [h] are assessed against. If the review above is going to change your score, your POA&M, and your evidence at the same time, which it usually does before an affirmation deadline, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) keeps the SSP, the SPRS workbook, the POA&M, the scoping worksheet, and the evidence tracker consistent with each other so the affirming official signs over one set of facts.

## Sources

- NIST SP 800-171 Rev 2, requirement 3.12.4; NIST SP 800-171A, assessment objectives 3.12.4[a] through [h]
- 32 CFR 170.24, CMMC Scoring Methodology, paragraphs (b)(1), (c)(2)(i)(B)(5), and (c)(2)(i)(B)(8)
- 32 CFR 170.21(a)(2)(iii), POA&M exclusions; 32 CFR 170.16(c)(2)(iii) and (c)(3)(i), CSP and ESP documentation in the SSP; 32 CFR 170.19, CMMC scoping; 32 CFR 170.22, affirmation
- U.S. Department of War CIO, CMMC Assessment Guide, Level 2, version 2.13, CA.L2-3.12.4 (minimum SSP contents and example)
- U.S. Department of War CIO, CMMC Scoping Guide, Level 2, version 2.13 (new assessment for significant architectural or boundary changes; operational changes covered by annual affirmation)
- U.S. Department of War CIO, CMMC Frequently Asked Questions, question C-Q12 (significant change and the affirming official)
- U.S. Department of War, DARS class deviation 2026-O0025, Revision 3, signed September 3, 2026
- U.S. Department of Justice, "Raytheon Companies and Nightwing Group to Pay $8.4M to Resolve False Claims Act Allegations Relating to Non-Compliance with Cybersecurity Requirements in Federal Contracts," May 1, 2025
- U.S. Department of Justice, LOGZONE Inc. False Claims Act settlement ($507,144), June 2026
- DFARS 252.204-7012; DFARS 252.204-7021; elimination of DFARS 252.204-7019 effective February 1, 2026
