---
layout: post
title: "DFARS 7019 Is Gone. Do You Still Need an SPRS Score?"
date: 2026-06-16
description: "DFARS 252.204-7019 was eliminated and 7020 renumbered on Feb 1, 2026. Here is what changed for your SPRS score and what every CUI contractor still has to do."
category: CMMC
tags: [CMMC, NIST 800-171, SPRS, DFARS, Defense Contractors]
image: /blog/images/1-dfars-7019-deleted-sprs-score-hero.png
author: CyberZ
---

*On February 1, 2026, the clause that told defense contractors to self-assess against NIST SP 800-171 and upload a score to SPRS quietly stopped existing. Here is what actually changed, and what did not.*

**As of February 1, 2026, DFARS 252.204-7019 has been eliminated and DFARS 252.204-7020 has been renumbered to DFARS 252.240-7997 as part of the Revolutionary FAR Overhaul. The standalone "Basic" NIST SP 800-171 self-assessment and its SPRS upload requirement no longer exist as a separate clause. If your company handles Controlled Unclassified Information (CUI), you still self-assess against NIST SP 800-171 and report your SPRS score. That obligation now sits under the CMMC clause, DFARS 252.204-7021.**

<div style="border-left: 4px solid #EE4C48; background: #16161a; padding: 18px 22px; margin: 28px 0; border-radius: 4px;">
<strong style="color:#EE4C48; letter-spacing:0.5px;">KEY TAKEAWAYS</strong>
<ul style="margin: 12px 0 0 0; padding-left: 20px; line-height: 1.6;">
<li>DFARS 252.204-7019 was eliminated and 252.204-7020 was renumbered to DFARS 252.240-7997, effective February 1, 2026.</li>
<li>FAR 52.204-21 was renumbered to FAR 52.240-93. The 15 basic safeguarding requirements for FCI are unchanged.</li>
<li>The standalone "Basic" self-assessment, and the requirement to upload that score to SPRS, no longer exist as a separate clause.</li>
<li>DFARS 252.204-7012 and the CMMC clause DFARS 252.204-7021 are unchanged.</li>
<li>Contractors that handle CUI still self-assess to NIST SP 800-171 and report an SPRS score, now under the CMMC framework.</li>
<li>This happened through DoD class deviations, not new rulemaking, so old and new clause numbers will both circulate until rulemaking catches up.</li>
</ul>
</div>

If you spend any time in CMMC circles, you have spent years learning to cite three numbers from memory: 7012, 7019, 7020. Two of them just changed underneath you. The reaction in some corners of the defense industrial base has been relief, as if a compliance burden was lifted. It was not. What happened on February 1 was consolidation, and reading it as relief is the kind of mistake that loses a contract.

## What changed on February 1, 2026

The Revolutionary FAR Overhaul is a federal effort to strip redundancy out of the acquisition regulations. To move faster than formal rulemaking allows, the Department of Defense implemented a batch of DFARS class deviations that took effect February 1, 2026. Three clauses that defense contractors track most closely were affected.

DFARS 252.204-7019, the "Notice of NIST SP 800-171 DoD Assessment Requirements," was eliminated. This was the provision that told you to perform a Basic self-assessment and have a current score on file before award. As a standalone clause, it is gone.

DFARS 252.204-7020 was renumbered to DFARS 252.240-7997 under the new DFARS Part 240. The revised clause removes its references to "Basic" assessments. It now defines only Medium and High assessments, both of which are performed by the government, not by you.

FAR 52.204-21, the "Basic Safeguarding of Covered Contractor Information Systems," was renumbered to FAR 52.240-93 under the new FAR Part 40. The title, the text, and the 15 safeguarding requirements are unchanged. Note that CMMC Level 1 still references the old number, 52.204-21, so for now both numbers point at the same set of requirements.

![Before-and-after of the FAR Overhaul: DFARS 7019 deleted, 7020 renumbered to 252.240-7997, FAR 52.204-21 renumbered to 52.240-93, with 7012 and the CMMC clause 7021 unchanged.](/blog/images/2-dfars-clause-changes-before-after.png)
*The clause map after February 1, 2026. Two numbers changed; the obligations behind them did not disappear.*

## What did not change

It is worth being precise about what survived, because this is the part the "relief" reading skips.

DFARS 252.204-7012 is unchanged. It still requires you to provide adequate security for Covered Defense Information by implementing NIST SP 800-171 Rev 2, to report cyber incidents within 72 hours, and to flow the requirement down to subcontractors that handle covered information.

DFARS 252.204-7021, the CMMC clause, is unchanged. This is the clause that, in Phase 2, makes a third-party assessment a condition of award for contracts involving CUI.

NIST SP 800-171 Rev 2 is unchanged. The 110 security requirements and the DoD Assessment Methodology that turns them into an SPRS score are exactly where they were.

And the underlying duty to protect Federal Contract Information (FCI) and CUI is unchanged. Renumbering a clause does not change what the government expects you to do with its data.

## Why "7019 is gone" does not mean self-assessment is gone

Here is the trap. Under the old structure, a CUI contractor lived under two parallel scoring regimes. One was the 7019/7020 path: do a Basic self-assessment, post the score in SPRS. The other was the CMMC program itself. Those two tracks asked for substantially the same thing, which is exactly the redundancy the FAR Overhaul set out to remove.

So the deviation collapsed the duplicate. It did not cancel the obligation. The self-assessment-and-report duty moved under the CMMC framework, governed by DFARS 252.204-7021, rather than living as a separate provision. One framework instead of two. The score still matters. The methodology still applies. The government still looks you up in SPRS.

Walk it through by data type, because that is what determines your obligation:

If your contracts involve only FCI, you meet the 15 safeguarding requirements, now cited as FAR 52.240-93. That is the Level 1 self-assessment population.

If your contracts involve CUI, you implement all 110 NIST SP 800-171 requirements, you assess against them (self-assessment now, third-party assessment under Phase 2), and your SPRS score remains the number DoD uses to gauge your posture. Nothing in the February deviation lets a CUI contractor stop self-assessing or stop caring about that score.

![Decision graphic: contractors that handle CUI still self-assess and upload an SPRS score under DFARS 7021; FCI-only firms meet FAR 52.240-93; deleting 7019 did not delete the obligation.](/blog/images/3-do-you-still-need-sprs-score.png)
*The obligation did not vanish. It changed addresses.*

## Your SPRS score is still the same instrument

For contractors that handle CUI, the SPRS score has not gotten any softer. It is still derived from the DoD Assessment Methodology: you start at 110, subtract a weighted value for each requirement you have not fully met (most are worth 1 point, some 3, a few 5), and the scale bottoms out at a floor of -203. A score that low means you have implemented almost nothing.

More to the point, the score you post is a representation to the federal government about the state of your security. That has not changed because the clause number did. A score that overstates your real posture is the same exposure it always was. If you self-reported a number a year ago and your environment has drifted since, the deletion of 7019 does nothing to protect you. The number still has to be true.

If you are rebuilding your score the right way, control by control, the [NIST 800-171 SPRS Score Workbook for CMMC Level 2](https://payhip.com/b/R5g4Y) ($87) walks the 110 requirements with the 1/3/5 weighting and produces a defensible score you can stand behind.

## What this means before November 10, 2026

Phase 2 of the CMMC program begins November 10, 2026, under 32 CFR Part 170. From that point, a C3PAO Level 2 assessment becomes the default condition of award for contracts involving CUI. The February clause renumbering does not touch that date. If anything, it sharpens the picture: there is now one framework to prepare against instead of two overlapping ones, and one fewer clause to hide behind.

Concretely, before the deadline:

Confirm whether your contracts involve FCI, CUI, or both. That single fact decides which level you owe and which clause set applies to you.

If you touch CUI, get your System Security Plan current, run a real self-assessment against all 110 requirements, and make sure your SPRS score reflects what is actually deployed, not what you intended to deploy.

For now, track both the old and the new clause numbers in your solicitations and contracts. Until rulemaking codifies these deviations, you will see 7019, 7020, 52.204-21 in older documents and 252.240-7997, 52.240-93 in newer ones, often referring to the same requirements.

A 12-person shop with a single CUI contract and a 200-person sub with a dozen of them are in the same position here: the clause that used to organize the self-assessment moved, and the work it pointed at did not.

If you are staring at the full path from scoping to a scheduled assessment, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) bundles the scoping worksheet, SSP template, SPRS workbook, evidence tracker, and a start-here guide, so a small team can run the whole sequence without assembling it piecemeal under deadline pressure.

## The bottom line

The elimination of DFARS 252.204-7019 is housekeeping, not a reprieve. The basic self-assessment and SPRS reporting obligations for CUI contractors did not disappear on February 1, 2026. They were consolidated under the CMMC framework and DFARS 252.204-7021. If you handle CUI, you still implement 110 controls, you still self-assess, and you still report a score that has to be accurate. The smartest thing a contractor can do with the news is treat it as a prompt to verify that score is right before Phase 2 makes it count.

## Sources

- DFARS 252.204-7012; 252.204-7019 (eliminated); 252.204-7020 renumbered to 252.240-7997; DFARS 252.204-7021 (CMMC) — DoD class deviations effective February 1, 2026, acquisition.gov
- FAR 52.204-21 renumbered to FAR 52.240-93 — acquisition.gov
- NIST SP 800-171 Revision 2, "Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations" — csrc.nist.gov
- CMMC Program Final Rule, 32 CFR Part 170 — ecfr.gov
- DoD Assessment Methodology, NIST SP 800-171 (SPRS scoring, 1/3/5 weighting, -203 floor) — U.S. Department of Defense
