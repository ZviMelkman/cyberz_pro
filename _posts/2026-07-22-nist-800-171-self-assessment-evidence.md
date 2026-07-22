---
layout: post
title: "NIST 800-171 Self-Assessment Evidence: What Backs Your Score Now That No Assessor Is Coming"
date: 2026-07-22
description: "The CMMC pause made your self-assessment the only assessment DoD has. What evidence backs each of the 110 requirements, and what a defensible SPRS score requires."
category: cmmc
tags: [NIST 800-171, CMMC, self-assessment, evidence, SPRS, NIST 800-171A]
image: /blog/images/1-nist-800-171-self-assessment-evidence-hero.png
author: CyberZ
---
 
*The July 13 suspension canceled the audit. It did not cancel the attestation. For the foreseeable future, the self-assessment behind your SPRS score is the only assessment the Department of Defense has, and evidence is the only thing that makes it more than a guess.*
 
**NIST 800-171 self-assessment evidence is the set of documents, records, configurations, and system outputs that demonstrate each of the 110 security requirements is actually implemented as your System Security Plan claims. NIST SP 800-171A defines what that evidence looks like: it breaks the 110 requirements into 320 assessment objectives and grades them through three methods, examine, interview, and test. If your SPRS score is not backed by evidence at the objective level, it is an unsupported claim in a federal database.**
 
<div class="key-takeaways" style="background:#16161a;border-left:4px solid #EE4C48;padding:1.2em 1.5em;margin:1.5em 0;">
<strong>Key Takeaways</strong>
<ul>
<li>The July 13, 2026 suspension paused third-party CMMC assessments, not the requirement to protect CUI or the self-assessment behind your SPRS score. DFARS 252.204-7012, -7019, and -7020 remain fully in force.</li>
<li>NIST SP 800-171A is the evidence standard for self-assessments, not just C3PAO audits. It defines 320 assessment objectives and three assessment methods: examine, interview, and test.</li>
<li>A self-assessment scored from memory, without artifacts behind it, produced the exact gap that cost MORSECORP $4.6 million in a 2025 False Claims Act settlement.</li>
<li>The evidence file you build for your self-assessment is the same file a C3PAO will request if Phase 2 returns after the 60-day review. Nothing you collect now is wasted.</li>
</ul>
</div>
 
## Your self-assessment just became the only assessment
 
On July 13, 2026, the Department of War suspended CMMC Phase 2, the milestone that would have made third-party C3PAO assessments a condition of award for CUI contracts starting November 10. All later phase milestones are on hold while a Reform Task Force conducts a 60-day review, with a public Request for Information due August 14. The arithmetic behind the decision: over 100,000 companies were expected to need third-party assessments, against roughly 100 authorized C3PAOs.
 
What the suspension did not touch is the part most of the relieved commentary skips. During the pause, contracting officers may still include CMMC Level 1 (Self) and Level 2 (Self) requirements in solicitations. The Phase 1 self-assessment obligations that took effect in November 2025 continue. And underneath all of it, DFARS 252.204-7012 still requires safeguarding covered defense information, while DFARS 252.204-7019 still requires a current NIST 800-171 Basic Assessment score posted to the Supplier Performance Risk System (SPRS) before award. We covered the full paused-versus-in-force breakdown in [Is CMMC Still Required? What the Phase 2 Suspension Did and Did Not Change](/blog/2026/07/19/is-cmmc-still-required/).
 
Here is the practical shift: before July 13, your self-assessment was a waypoint on the road to an external audit. Now it is the entire assessment regime. There is no assessor coming to catch your mistakes before the government relies on your number. That makes the evidence behind your self-assessment more important, not less.
 
## The evidence standard already exists, and it applies to you
 
Contractors sometimes assume NIST SP 800-171A, the assessment companion document, is a C3PAO concern. It is not. The DoD Assessment Methodology that governs your Basic (self) Assessment tells you to assess implementation of NIST 800-171, and 800-171A is NIST's own answer to what "assessed" means. The CMMC Level 2 self-assessment requirement points at the same objectives. If you scored yourself without reference to it, your score measures optimism, not implementation.
 
800-171A does two things that matter for a self-assessor:
 
**It decomposes 110 requirements into 320 assessment objectives.** Requirement 3.1.1, limiting system access to authorized users, is not one yes-or-no question. It breaks into separate objectives: authorized users are identified, processes acting on behalf of users are identified, devices are identified, and access is actually limited to each. You can satisfy three objectives and fail the fourth, and the requirement is NOT MET. Scoring at the requirement level without looking at the objectives is how companies post a 110 and hold a much lower reality.
 
**It defines three assessment methods, and each method implies evidence.**
 
![The three NIST 800-171A assessment methods and the evidence each one needs](/blog/images/2-nist-800-171a-examine-interview-test-evidence-types.png)
 
- **Examine** looks at specifications and mechanisms: policies, plans, procedures, architecture diagrams, and system configurations. The evidence is the document or the config export itself.
- **Interview** asks the people who operate the controls. For a self-assessment, this translates to knowing exactly who answers for each control family and having the training and role records that prove they can.
- **Test** exercises the mechanism. The evidence is the output: the screenshot of the MFA challenge, the audit log sample, the backup restore report with a date on it.
 
A defensible self-assessment keeps at least one artifact per objective, mapped so you can retrieve it. Not a binder of policies. Policies only cover the examine method, and only partially; a written access control policy proves nothing about whether MFA was actually enforced on the VPN last Tuesday.
 
## The SPRS number is a federal claim, not an IT metric
 
Your Basic Assessment score, from +110 down to the floor of -203 under the DoD Assessment Methodology's 1, 3, and 5 point weightings, gets posted to SPRS under DFARS 252.204-7019. A senior company official affirms it. Where the CMMC clause applies, that affirmation renews annually. Every layer of that stack is a representation to the federal government.
 
![What your SPRS score stands on: affirmation, score, self-assessment, evidence](/blog/images/3-sprs-attestation-evidence-stack.png)
 
The Department of Justice has already shown what happens when the layers do not hold. In March 2025, MORSECORP agreed to pay $4.6 million to resolve False Claims Act allegations that included submitting SPRS scores that did not reflect its actual NIST 800-171 implementation. No breach was required. The gap between the claimed score and the defensible score was the violation. DOJ's Civil Cyber-Fraud Initiative has been explicit that these cases turn on misrepresentation, not on whether an attacker ever showed up.
 
That is why the suspension cuts the opposite way from how many contractors read it. With third-party validation paused, the government is relying entirely on self-reported numbers, and the False Claims Act is the enforcement mechanism that polices self-reporting. A whistleblower does not need an audit to notice that the company posted a 110 while half the controls live on a to-do list. How the scoring math works, weight by weight, is in [How Your NIST 800-171 SPRS Score Is Calculated (and What It Legally Commits You To)](/blog/2026/06/19/how-nist-800-171-sprs-score-calculated/).
 
## What the evidence file looks like for a 20-person shop
 
Take a machining subcontractor with 20 employees, a flow-down clause from a prime, and CUI living in a small enclave. A defensible evidence file for that company is not enterprise GRC software. It is a disciplined set of folders and a tracker:
 
| Control family (examples) | Evidence a self-assessor keeps |
|---|---|
| Access Control (3.1.x) | User list export with authorization records, MFA configuration screenshots, quarterly access review notes |
| Awareness & Training (3.2.x) | Training completion log with dates and names, the actual training material used |
| Audit & Accountability (3.3.x) | Retention settings export, a dated sample of reviewed logs, the review procedure |
| Configuration Management (3.4.x) | Baseline documents, change tickets or an equivalent change log |
| Identification & Authentication (3.5.x) | Password/MFA policy settings export, service account inventory |
| Incident Response (3.6.x) | The IR plan, the report of the last tabletop exercise with a date |
| System & Comms Protection (3.13.x) | Firewall ruleset export, encryption settings, network diagram matching the SSP |
 
Three habits make the file audit-grade rather than decorative. Date everything, because undated evidence proves nothing about the period your score covers. Map every artifact to the objective it supports, not just the control. And when evidence exposes a gap, move the item to your POA&M and adjust the score instead of rounding up; an honest 85 with a remediation plan is defensible, an aspirational 110 is a liability.
 
One more reason not to shortcut this: the file you build for the self-assessment is the same file a C3PAO requests if the Reform Task Force brings third-party assessments back in some form after mid-September. What assessors examine, interview, and test in that scenario is covered in [What a C3PAO Actually Examines, Interviews, and Tests in a CMMC Level 2 Assessment](/blog/2026/06/14/cmmc-evidence-what-c3pao-examines/). Nothing collected now is wasted under any outcome of the review.
 
## What to do this week
 
1. Pull your current SPRS score and the date it was posted. If your environment has changed since, the score is stale regardless of what it says.
2. Pick your three worst control families and check whether one artifact per objective exists. Most companies find the gap is retrieval, not implementation: the control works, but nobody can prove it in under an hour.
3. Assign an owner per control family. The interview method assumes someone can speak to each control; in a 20-person shop that is usually four or five names.
4. Re-score honestly against the objectives, move real gaps to the POA&M, and update SPRS if the number changes. The refresh requirements and who qualifies are in our [CMMC Level 2 self-assessment requirements guide](/blog/2026/07/07/cmmc-level-2-self-assessment-requirements/).
 
Tracking 320 objectives against evidence in your head does not survive contact with reality, which is what the [CMMC Level 2 Evidence Tracker for NIST 800-171 Audit](https://payhip.com/b/LN2UB) ($67) is built for: every objective, its method, and the artifact that answers it, in one workbook. If the score itself is the part you cannot defend yet, the [NIST 800-171 SPRS Score Workbook for CMMC Level 2](https://payhip.com/b/R5g4Y) ($87) walks the scoring control by control.
 
## Frequently asked questions
 
**Which document is the primary evidence artifact for a self-assessment?**
The System Security Plan. Requirement 3.12.4 makes it mandatory, and every other artifact either supports what the SSP claims or contradicts it. An SSP that describes a network you no longer run is itself adverse evidence.
 
**Is NIST 800-171 a self-assessment?**
Under DFARS 252.204-7019/-7020, the Basic Assessment is a self-assessment, and during the CMMC suspension, self-assessment is the only assessment type contracting officers may require for Level 1 and Level 2. DoD retains the right to conduct Medium and High assessments through DIBCAC.
 
**Can you self-certify for CMMC Level 2 right now?**
During the pause, yes: Level 2 (Self) is the highest CMMC requirement that may appear in new solicitations, and it covers all 110 requirements assessed against the 800-171A objectives, with a senior official's annual affirmation.
 
**How many assessment objectives are in NIST 800-171A?**
320, under the current Rev 2 baseline. You may see 422 cited; that figure belongs to the Rev 3 edition of 800-171A, which is not the assessment baseline for CMMC or the DoD Assessment Methodology today.
 
## The bottom line
 
The suspension removed the deadline, not the liability. Your SPRS score is now the load-bearing representation in the relationship with DoD, and evidence is the only thing holding it up. Build the file while nobody is asking for it, because the moment someone does ask, whether that is a prime, DIBCAC, or a DOJ attorney, is the wrong time to start.
 
## Sources
 
- Department of War press release, "Forging the Arsenal of Freedom: Department of War Suspends CMMC Phase II Requirements" (July 13, 2026): [war.gov](https://www.war.gov/News/Releases/)
- DoD CIO, About CMMC (suspension status and continuing Phase 1 requirements): [dodcio.defense.gov/cmmc](https://dodcio.defense.gov/cmmc/About/)
- SBA news release 26-73 commending the Phase II suspension (July 13, 2026): [sba.gov](https://www.sba.gov/article/2026/07/13/sba-commends-us-department-wars-suspension-cmmc-phase-ii-small-defense-contractors)
- NIST SP 800-171 Rev 2: [csrc.nist.gov](https://csrc.nist.gov/pubs/sp/800/171/r2/upd1/final)
- NIST SP 800-171A, Assessing Security Requirements for Controlled Unclassified Information: [csrc.nist.gov](https://csrc.nist.gov/pubs/sp/800/171/a/final)
- NIST SP 800-171 DoD Assessment Methodology, Version 1.2.1: [acq.osd.mil](https://www.acq.osd.mil/asda/dpc/cp/cyber/safeguarding.html)
- DFARS 252.204-7012, -7019, -7020: [acquisition.gov](https://www.acquisition.gov/dfars/part-252-solicitation-provisions-and-contract-clauses)
- 32 CFR Part 170, CMMC Program: [ecfr.gov](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170)
- DOJ press release, MORSECORP Inc. $4.6M False Claims Act settlement (March 26, 2025): [justice.gov](https://www.justice.gov/usao-ma/pr)
