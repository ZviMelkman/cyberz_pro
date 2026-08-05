---
layout: post
title: "CMMC Level 1 Requirements: The 15 Controls, the Annual Affirmation, and Who Actually Needs It"
date: 2026-08-05
description: "CMMC Level 1 covers FCI, not CUI. The 15 requirements from FAR 52.204-21, why no POA&M is permitted, what the annual SPRS affirmation obligates, and what the Phase 2 suspension left untouched."
category: CMMC
tags: [CMMC, CMMC Level 1, FAR 52.204-21, FCI, NIST 800-171, SPRS, self-assessment, defense contractors]
image: /blog/images/1-cmmc-level-1-vs-level-2-decision.png
author: CyberZ
---

*Phase 2 is suspended. Level 1 is not, and it never was.*

**CMMC Level 1 applies to contractors whose systems process, store, or transmit Federal Contract Information but not Controlled Unclassified Information. It requires all 15 security requirements in FAR 52.204-21(b)(1) to be assessed as MET, with no Plan of Action and Milestones permitted for any of them. Under 32 CFR 170.15, the self-assessment is annual, the results go into SPRS, and an Affirming Official must submit a separate affirmation of continuing compliance at completion and every year thereafter. Assessment artifacts must be retained for six years from the CMMC Status Date.**

<div class="key-takeaways" style="background:#16161a;border-left:4px solid #EE4C48;padding:20px 24px;margin:24px 0;">
<strong>Key Takeaways</strong>
<ul>
<li>The line between Level 1 and Level 2 is the type of information, not the size of the company. FCI in scope means Level 1. CUI in scope means Level 2.</li>
<li>32 CFR 170.15(a)(1) requires a MET result on all 15 requirements and states plainly that no POA&amp;Ms are permitted for CMMC Level 1. There is no partial pass and no 80 percent threshold at this level.</li>
<li>The self-assessment and the affirmation are two separate submissions, both annual, both in SPRS. 32 CFR 170.15(b) makes contract eligibility depend on having done both.</li>
<li>The July 13, 2026 memoranda suspended CMMC Phase 2 and all pending and future program milestones. Phase 1 self-assessment requirements remained in force, and DoD programs can continue including CMMC self-assessment requirements in contracts.</li>
<li>Level 1 scoping has two carve-outs, at 32 CFR 170.19(b)(2). FAR 52.204-21 has neither, so a contractor handling FCI is usually carrying both sets of obligations at once.</li>
<li>Paragraph (c) of FAR 52.204-21 requires the substance of the clause in subcontracts where the subcontractor may have FCI in or transiting its systems. Level 1 obligations move down the supply chain by contract, not by company size.</li>
<li>Achieving Level 2 (Self) also satisfies Level 1 for the same assessment scope, per 32 CFR 170.16(a). The reverse is never true.</li>
</ul>
</div>

![The 15 basic safeguarding requirements from FAR 52.204-21(b)(1), grouped into access, identity, media, physical, boundary and integrity categories](/blog/images/2-far-52-204-21-fifteen-requirements.png)

## What is CMMC Level 1?

CMMC Level 1 is the lowest of the three assessment levels in the CMMC Program, codified at 32 CFR Part 170. Its content comes from a single Federal Acquisition Regulation clause, FAR 52.204-21, "Basic Safeguarding of Covered Contractor Information Systems," currently in its November 2021 revision.

That clause defines a covered contractor information system as one owned or operated by a contractor that processes, stores, or transmits Federal contract information. It defines FCI as information not intended for public release, provided by or generated for the Government under a contract to develop or deliver a product or service, excluding information the Government makes public and excluding simple transactional information such as what is needed to process payments.

Two things follow from those definitions that contractors routinely get wrong. First, FCI is a wide category. Statements of work, delivery schedules, technical correspondence, and drawings that were never intended for public release all tend to qualify. Second, the trigger is the information, not the contract value. A small subcontract can put FCI on your systems just as effectively as a large one.

## Which contracts require CMMC Level 1 instead of Level 2?

The deciding question is whether CUI is in your assessment scope.

If your systems handle FCI and no CUI, Level 1 is the applicable status. If CUI is in scope, you are in Level 2 territory, which draws on the 110 requirements of NIST SP 800-171 rather than the 15 of FAR 52.204-21, and which may require a third-party assessment depending on the contract.

The two levels are not rungs on a difficulty ladder that you climb over time. They are separate obligations with separate triggers. One useful asymmetry is worth committing to memory: under 32 CFR 170.16(a), achieving a CMMC Status of Level 2 (Self) also satisfies the Level 1 requirements for the same assessment scope. Nothing works in the opposite direction.

![Side-by-side comparison of CMMC Level 1 and Level 2 showing trigger, requirement source, count, assessor, POA&M treatment, affirmation and governing section](/blog/images/3-cmmc-level-1-vs-level-2-comparison.png)

If you are not certain which side of that line you are on, the scoping determination is the work that has to happen first, and it is a documentation exercise rather than a technical one. The [scoping decision comes before any control work]({% post_url 2026-07-19-cmmc-scoping-decision-not-controls %}), and getting it backwards is the most expensive sequencing error in CMMC preparation.

## What are the 15 CMMC Level 1 requirements?

FAR 52.204-21(b)(1) lists them as (i) through (xv). In plain terms:

1. Limit information system access to authorized users, processes acting on behalf of authorized users, and devices.
2. Limit access to the types of transactions and functions that authorized users are permitted to execute.
3. Verify and control or limit connections to and use of external information systems.
4. Control information posted or processed on publicly accessible information systems.
5. Identify information system users, processes acting on behalf of users, and devices.
6. Authenticate or verify the identities of those users, processes, or devices before allowing access.
7. Sanitize or destroy information system media containing FCI before disposal or release for reuse.
8. Limit physical access to organizational systems, equipment, and their operating environments to authorized individuals.
9. Escort visitors and monitor visitor activity, maintain audit logs of physical access, and control and manage physical access devices.
10. Monitor, control, and protect organizational communications at the external boundaries and key internal boundaries of the systems.
11. Implement subnetworks for publicly accessible system components, physically or logically separated from internal networks.
12. Identify, report, and correct information and information system flaws in a timely manner.
13. Provide protection from malicious code at appropriate locations within organizational systems.
14. Update malicious code protection mechanisms when new releases are available.
15. Perform periodic scans of the system, and real-time scans of files from external sources as they are downloaded, opened, or executed.

Requirement 9 deserves a flag, because it is the one that most often fails a self-assessment honestly performed. It is not satisfied by a locked front door. It asks for visitor escorting, visitor activity monitoring, audit logs of physical access, and management of physical access devices such as keys and badges. Most small contractors have the locked door and none of the logs.

Requirement 11 is the other frequent gap. A publicly accessible component sitting on the same flat network as everything else does not meet it, and a great many small offices run flat networks.

## Did the July 2026 CMMC suspension change Level 1 obligations?

No.

On July 13, 2026, DoD issued two memoranda under publication case 26-P-1023, a policy memorandum from the DoD Chief Information Officer and an implementation memorandum from the Under Secretary of Defense for Acquisition and Sustainment. They suspended CMMC Phase 2, which would have made third-party Level 2 assessments the default for CUI contracts starting November 10, 2026, and they suspended all pending and future CMMC milestones until further notice. A CMMC Reform Task Force was stood up to review the program and report within 60 days.

What the memoranda did not do is remove the Phase 1 requirements that took effect in November 2025. DoD programs can continue to include CMMC self-assessment requirements in contracts, and self-assessment plus government-led assessment is the enforcement posture during the interim period.

The distinction that matters here is legal, not rhetorical. A memorandum changes departmental discretion. It does not amend 32 CFR Part 170 or the DFARS. Level 1 obligations sit in a regulation that was not touched, and in a FAR clause that was not touched either. If your contract carries FAR 52.204-21 today, it carries it tomorrow. For the fuller version of that argument, see [whether CMMC is still required after the suspension]({% post_url 2026-07-19-is-cmmc-still-required %}), and note that the reform process is still open: [the RFI closes at noon Eastern on August 14]({% post_url 2026-08-02-cmmc-reform-task-force-rfi-response %}).

## What is in scope for a CMMC Level 1 self-assessment?

Under 32 CFR 170.19(b)(1), the systems in scope are those that process, store, or transmit FCI. The scope must be specified before the assessment, not reconstructed afterward.

Two categories sit outside that scope. Out-of-Scope Assets, at 170.19(b)(2)(i), are systems that do not process, store, or transmit FCI, plus an endpoint hosting a VDI client configured to pass nothing beyond keyboard, video, and mouse. There are no documentation requirements for out-of-scope assets at Level 1. Specialized Assets, at 170.19(b)(2)(ii), are assets that can handle FCI but cannot be fully secured: IoT and IIoT devices, operational technology, Government Furnished Equipment, restricted information systems, and test equipment. At Level 1 these are not part of the assessment scope and are not assessed against CMMC requirements.

![Three scoping buckets for CMMC Level 1: in scope, out of scope, and specialized assets, with the governing subsections](/blog/images/4-cmmc-level-1-scoping-in-out-specialized.png)

Before leaning on either carve-out, read the FAR clause again. It contains no equivalent exceptions. Its safeguarding requirements apply to any covered contractor information system that processes, stores, or transmits FCI, full stop. A contractor with FCI on its network is typically subject to both the clause and the CMMC status requirement, which means the Level 1 scoping exceptions narrow what gets assessed without narrowing what the contract obligates.

Note also that Level 1 scoping is genuinely simpler than Level 2 scoping. Level 2 defines four in-scope asset categories, and specialized assets there must be documented in the asset inventory and addressed in the SSP under 170.19(c)(1) Table 3. If you are trying to work out which regime you are in, that difference in documentation burden is a useful tell.

The asset inventory is the deliverable that makes all of this defensible. The [CMMC Level 2 Asset Scoping Worksheet for NIST 800-171](https://payhip.com/b/2nzjO) sorts each asset into the CMMC categories and flags what is missing from your inventory, and the categorization logic is the same exercise a Level 1 contractor runs to draw the FCI boundary. It is $47.

## Can you use a POA&M at CMMC Level 1?

No. 32 CFR 170.15(a)(1) states that no POA&Ms are permitted for CMMC Level 1, and requires a MET result on every one of the 15 requirements to achieve a CMMC Status of Final Level 1 (Self).

This is where Level 1 is structurally stricter than Level 2, which surprises people. At Level 2, 32 CFR 170.21 allows certain gaps to be deferred on a POA&M under defined conditions, with a closeout clock. At Level 1 there is no such mechanism. Fourteen of fifteen is not a Level 1 status. It is nothing.

There is also no scoring cushion to hide in. The Level 1 self-assessment is scored under the methodology at 32 CFR 170.24, and it is performed using the assessment objectives in NIST SP 800-171A June 2018 for the requirement that maps to each Level 1 requirement, substituting FCI for CUI wherever an objective addresses CUI. Those objectives are granular. A requirement is MET when every objective under it is satisfied, which is a higher bar than reading the FAR sentence and nodding.

## Who signs the CMMC Level 1 affirmation, and how often?

An Affirming Official does, and annually.

32 CFR 170.22(a) requires an Affirming Official from each organization, whether prime or subcontractor, to affirm continuing compliance after every assessment and annually thereafter, entered electronically in SPRS. Paragraph (b)(1) applies that specifically to Level 1: at completion of the self-assessment and annually after, the Affirming Official submits a CMMC affirmation attesting to continuing compliance with all requirements of the CMMC Status Level 1 (Self).

Two operational consequences follow. First, the self-assessment and the affirmation are separate submissions, and 32 CFR 170.15(b) conditions contract eligibility on both being complete for all information systems within the assessment scope. Doing the assessment and forgetting the affirmation leaves you ineligible. Second, an affirmation is an attestation by a named individual, which is the mechanism that connects compliance representations to False Claims Act exposure. That exposure does not scale down because the level is 1. If anything, the absence of a POA&M safety valve makes an inaccurate Level 1 affirmation harder to explain.

Retention closes the loop. Under 32 CFR 170.15(c)(2), the artifacts used as evidence must be retained for six years from the CMMC Status Date. An affirmation you cannot substantiate three years later is a problem you have created for yourself, which is why [the evidence question is the one worth solving early]({% post_url 2026-07-22-nist-800-171-self-assessment-evidence %}).

![The five-step annual CMMC Level 1 cycle: define scope, self-assess to MET, submit in SPRS, file the affirmation, retain artifacts six years](/blog/images/5-cmmc-level-1-annual-cycle.png)

## Does FAR 52.204-21 flow down to subcontractors?

Yes, and this is worth stating clearly because published guidance on the point is not uniformly correct.

Paragraph (c) of the clause requires the contractor to include the substance of the clause, including paragraph (c) itself, in subcontracts under the contract, including subcontracts for commercial products or commercial services other than commercially available off-the-shelf items, in which the subcontractor may have FCI residing in or transiting through its information system.

The trigger for flow-down is therefore whether the subcontractor may hold or pass FCI. It is not the subcontract value and not the subcontractor's headcount. A two-person shop receiving a drawing package that was never intended for public release is inside this clause.

## What does a contractor do this week?

Five things, in order.

**Read your contracts for the clause.** Search executed contracts and active solicitations for FAR 52.204-21 and for any CMMC status requirement. The clause tells you whether the 15 requirements are contractual obligations for you right now.

**Determine whether any CUI is in scope.** If it is, you are answering a Level 2 question and the rest of this changes. If it is not, Level 1 is your target.

**Draw the FCI boundary and write it down.** Identify every system that processes, stores, or transmits FCI, and record the out-of-scope and specialized determinations you are relying on. The scope has to exist before the assessment.

**Self-assess against the 800-171A objectives, not the FAR sentences.** Work requirement by requirement, objective by objective, substituting FCI for CUI. Expect requirement 9 and requirement 11 to be the two that fail honestly.

**Close every gap before you submit, then affirm.** With no POA&M available, remediation precedes submission. Then have the Affirming Official file the affirmation in SPRS, and file the artifacts where you can find them in year six.

If the self-assessment turns up CUI you did not know you were holding, the target moves to Level 2 and the work expands from 15 requirements to 110. The [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) is the bundle for that situation: it covers the SSP, the SPRS scoring workbook, the evidence tracker, the POA&M structure, and the asset scoping worksheet in one set, which is the difference between starting a Level 2 program from a blank page and starting from a structure. It is $147.

---

### Sources

- 48 CFR 52.204-21, Basic Safeguarding of Covered Contractor Information Systems (NOV 2021), via eCFR. [ecfr.gov](https://www.ecfr.gov/current/title-48/chapter-1/subchapter-H/part-52/subpart-52.2/section-52.204-21)
- 32 CFR 170.15, CMMC Level 1 self-assessment and affirmation requirements, via eCFR. [ecfr.gov](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.15)
- 32 CFR 170.16, CMMC Level 2 self-assessment and affirmation requirements, via eCFR. [ecfr.gov](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.16)
- 32 CFR 170.19, CMMC scoping, via eCFR. [ecfr.gov](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.19)
- 32 CFR 170.22, Affirmation, via eCFR. [ecfr.gov](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.22)
- DoD CIO policy memorandum and USD(A&S) implementation memorandum suspending CMMC Phase 2, July 13, 2026, publication case 26-P-1023.
- CMMC Assessment Scope Level 1 guidance, DoD CIO. [dodcio.defense.gov](https://dodcio.defense.gov/Portals/0/Documents/CMMC/ScopingGuideL1.pdf)

*Verified August 5, 2026. CMMC is in an active reform process and the Task Force report is expected in mid-September 2026. Re-check 32 CFR Part 170 and any class deviation before relying on this for a submission.*

