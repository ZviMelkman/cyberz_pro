---
layout: post
title: "CMMC Annual Affirmation Requirements: How Often, How to Submit, and What Happens If You Skip It"
date: 2026-07-05
description: "CMMC affirmations are due after every assessment, at POA&M closeout, and annually in SPRS. The full cycle under 32 CFR 170.22, the submission mechanics, and the award consequences under DFARS 252.204-7021."
category: CMMC
tags: [CMMC, NIST 800-171, SPRS, annual affirmation, affirming official, DFARS]
image: /blog/images/1-cmmc-annual-affirmation-requirements-hero.png
author: CyberZ
---

*A CMMC Level 2 certification is valid for three years. The affirmation behind it is not. It expires every year, and the contracting officer checks for it before every award, option exercise, and extension. This is the part of CMMC that keeps running after the assessment ends.*

**A CMMC annual affirmation is an attestation, submitted electronically in the Supplier Performance Risk System (SPRS), that your organization has implemented and will maintain implementation of all applicable CMMC security requirements for every information system inside your CMMC Assessment Scope. Under 32 CFR 170.22, it is required after every assessment, at POA&M closeout, and annually thereafter, and the Department of Defense verifies its submission in SPRS.**

<div style="border-left:4px solid #EE4C48;background:#18181c;padding:20px 24px;margin:28px 0;border-radius:4px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;line-height:1.65;color:#e6e6e6;">
<li>The affirmation is not a one-time step. 32 CFR 170.22 requires it after every assessment, at POA&M closeout, and annually after the Final CMMC Status Date.</li>
<li>Every affirmation names a senior official (the Affirming Official) with their title and contact information, and attests to implemented and maintained compliance across the full assessment scope.</li>
<li>All affirmations go into SPRS, and DoD verifies submission against solicitation and contract requirements.</li>
<li>Without a current affirmation, DFARS 252.204-7021 blocks new awards, option exercises, and extensions for contracts that carry a CMMC requirement.</li>
<li>The three-year assessment cycle and the one-year affirmation cycle run on different clocks. Most compliance drift happens between the two.</li>
</ul>
</div>

## What 32 CFR 170.22 actually requires

The affirmation rule is short, and it is worth reading in its own words. Under 32 CFR 170.22(a), the organization must affirm continuing compliance with its self-assessment or certification assessment, and the Affirming Official "must affirm the continuing compliance of their respective organizations with the specified security requirement after every assessment, including POA&M closeout, and annually thereafter."

Three details in that sentence do the real work.

First, it applies to primes and subcontractors alike. The regulation says the Affirming Official from each organization, "whether a prime or subcontractor," submits the affirmation. There is no tier where this becomes someone else's problem.

Second, the affirmation has defined content under 170.22(a)(2). It includes the name, title, and contact information of the Affirming Official, plus a statement attesting that the organization "has implemented and will maintain implementation of all applicable CMMC security requirements" for all information systems within the relevant CMMC Assessment Scope. Note the two verbs. You are not just certifying past implementation. You are committing to maintain it going forward.

Third, everything goes into SPRS. Under 170.22(b), all affirmations are completed in SPRS, and "the Department will verify submission of the affirmation in SPRS to ensure compliance with CMMC solicitation or contract requirements." Verification is not theoretical. It is written into the rule.

Who the Affirming Official is, and why that signature carries personal False Claims Act exposure, is a separate topic we covered in depth in [Who Signs Your CMMC Affirmation Is Personally on the Hook]({% post_url 2026-06-18-cmmc-affirming-official-personal-liability %}). This article is about the machine itself: the schedule, the submission, and the consequence.

## How often must CMMC compliance be affirmed

The honest answer is: more often than most contractors have planned for. 32 CFR 170.22(b) breaks the schedule out by level.

![The CMMC Level 2 affirmation cycle under 32 CFR 170.16 and 170.22, from assessment through annual affirmations to reassessment](/blog/images/2-cmmc-affirmation-cycle-level-2.png)
*The Level 2 cycle: one assessment, then a new attestation every year until you reassess.*

**Level 1 (Self).** The affirmation is due at the completion of the Level 1 self-assessment and annually thereafter (32 CFR 170.22(b)(1)). Since the Level 1 self-assessment itself is an annual exercise under 32 CFR 170.15, Level 1 contractors are effectively re-assessing and re-affirming every year.

**Level 2 (Self).** The affirmation is due at the completion of the Level 2 self-assessment and annually following the Final CMMC Status Date (32 CFR 170.22(b)(2)). If your self-assessment produced a POA&M and a Conditional status, an additional affirmation is due at the completion of the POA&M closeout self-assessment. The status itself is valid for three years, which means a typical cycle looks like: assess and affirm in year zero, affirm again at POA&M closeout if applicable, affirm in year one, affirm in year two, then reassess and start over.

**Level 2 (C3PAO).** Same rhythm. The affirmation is due at the completion of the certification assessment and annually following the Final CMMC Status Date, plus at POA&M closeout if the assessment produced a Conditional status (32 CFR 170.22(b)(3)). The three-year validity of the certification does not stretch the affirmation. A C3PAO certificate from November 2026 still needs a fresh affirmation in November 2027 and November 2028.

**Level 3 (DIBCAC).** Also annual following the Final CMMC Status Date, and organizations holding Level 3 must separately affirm their underlying Level 2 (C3PAO) status each year as well, because the two assessments verify different requirement sets.

One nuance worth flagging because it trips people up: the annual clock runs from the CMMC Status Date, not from the calendar year and not from the contract award date. If your assessment closed in March, your affirmation is a March obligation every year after.

## How the affirmation is submitted in SPRS

Mechanically, this is the least documented part of the program, and it is the part contractors ask about most on r/CMMC. The authoritative walkthrough is DISA's Affirming Official tutorial published on the SPRS site (sprs.csd.disa.mil).

The short version. The Affirming Official needs their own access: a Procurement Integrated Enterprise Environment (PIEE) account with the SPRS Cyber Vendor User role. Affirmation is a distinct action inside SPRS, separate from entering the assessment score. In the CMMC module, an assessment that is pending affirmation or ready for its initial affirmation shows in the status column, and the Affirming Official completes the attestation from there. The affirmation record carries its own expiration date, which is what the annual cycle counts against.

Two operational consequences follow from that design.

The score and the affirmation are separate submissions, and a score without an affirmation does not make you eligible. The Department has been reminding contractors of exactly this distinction, and Reddit threads in r/CMMC are full of contractors who entered a score, assumed they were done, and never completed the attestation step.

And because the Affirming Official personally holds the PIEE access and clicks the button, the affirmation cannot quietly live with your MSP or IT consultant. The regulation defines the Affirming Official as the senior level representative responsible for ensuring compliance (32 CFR 170.22(a)(1)). The workflow enforces what the rule intends: a named executive, in the system, on the record.

## What happens if you do not affirm

The consequence is not a fine and it is not a letter. It is eligibility.

![Three things a contracting officer cannot do without a current CMMC affirmation in SPRS, per DFARS 252.204-7021](/blog/images/3-cmmc-affirmation-missed-consequences.png)
*An expired affirmation and a failed assessment have the same contractual effect.*

DFARS clause 252.204-7021, effective November 10, 2025, makes a current CMMC status and a current affirmation of continuous compliance in SPRS a condition of contract action. When a solicitation carries a CMMC requirement, the contracting officer will not make award, exercise an option, or extend the period of performance if the contractor does not have both the passing assessment results and the affirmation on file. The clause also flows the obligation down to subcontractors that handle FCI or CUI.

Run that against the annual cycle and the failure mode becomes obvious. A contractor certifies in early 2027, wins a three-year contract, and treats the certificate as done. Twelve months later the affirmation expires. Nothing dramatic happens that day. The problem surfaces months later, when the option year comes up for exercise and the contracting officer's SPRS check shows no current affirmation. At that point the contractor is not partially compliant. They are ineligible, on a contract they already hold, over an attestation that takes minutes to submit.

The same logic applies to the POA&M path. Under 32 CFR 170.16 and 170.17, a Conditional Level 2 status expires if the POA&M is not closed out within 180 days, and the closeout itself triggers its own affirmation. Miss either half and the status is gone, with standard contractual remedies available to the government. We walked through which gaps can legally sit on a POA&M in [Which CMMC Gaps You Can POA&M (and the 63 You Can't)]({% post_url 2026-06-17-cmmc-poam-eligibility %}).

## The two-clock problem

Here is the structural issue underneath all of this. The assessment runs on a three-year clock. The affirmation runs on a one-year clock. Your environment runs on no clock at all.

Between year zero and year one, systems get migrated, employees with security responsibilities leave, a new SaaS tool gets adopted, a firewall rule gets loosened for a project and never tightened. None of that shows up in SPRS. But the affirmation you sign in year one does not attest to your posture at assessment time. It attests, in the regulation's words, that you have implemented "and will maintain" implementation of every applicable requirement, right now, across the whole scope.

That is why the annual affirmation is not an administrative renewal. It is a fresh statement of fact about a posture that has had a year to drift. The signature is only as good as the evidence behind it on the day it is signed, and the evidence that matters is the same evidence the original assessment ran on: the SPRS score and the documentation trail underneath it.

## What to have in place before each annual signature

Treat the affirmation date as an internal audit date. The practical checklist before the Affirming Official signs:

**Re-run the score.** Recalculate your NIST SP 800-171 assessment against the DoD scoring methodology and compare it to what SPRS currently shows. If the number in SPRS no longer reflects reality, fix the posture or fix the score before anyone attests to it. The [NIST 800-171 SPRS Score Workbook for CMMC Level 2](https://payhip.com/b/R5g4Y) ($87) walks the full 110-control calculation with the 1, 3, and 5 point weights so the number you affirm is a number you can defend.

**Reconcile the SSP.** The affirmation covers all information systems in scope. If the environment changed, the System Security Plan has to say so before the signature does.

**Check POA&M status against the calendar.** Anything sitting on a POA&M is running against the 180-day clock, and closeout carries its own affirmation.

**Document the review itself.** A dated internal review memo is the difference between a signature made with a reasonable basis and one made on assumption.

If you are building that annual basis from scratch, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) bundles the SPRS workbook with the SSP template, asset scoping worksheet, POA&M tracker, and evidence tracker. It exists for exactly this moment: an affirmation date approaching and no organized record to sign against.

## FAQ

**How often must CMMC compliance be affirmed?**
After every assessment, at POA&M closeout, and annually thereafter, per 32 CFR 170.22. Level 1 affirms with each annual self-assessment. Level 2 and Level 3 affirm at assessment and then every year following the Final CMMC Status Date, even though the assessment itself is only repeated every three years.

**Who submits the affirmation in SPRS?**
The Affirming Official: the senior level representative within the organization who is responsible for CMMC compliance and has the authority to affirm continuing compliance (32 CFR 170.22(a)(1)). They need a PIEE account with the SPRS Cyber Vendor User role to complete it.

**What happens if you don't affirm in SPRS?**
Your CMMC status is no longer current, and under DFARS 252.204-7021 the contracting officer cannot make an award, exercise an option, or extend the period of performance on contracts that carry a CMMC requirement.

**How long is a CMMC certification good for?**
A Level 2 status, self-assessed or C3PAO-certified, is valid for three years. The affirmation behind it must be renewed annually within that window.

**Is the CMMC affirmation legally binding?**
Yes. It is a certification to the federal government, and a false one carries False Claims Act exposure for the company and the individual who signed. The full liability picture is in our breakdown of [who signs and what they're personally on the hook for]({% post_url 2026-06-18-cmmc-affirming-official-personal-liability %}).

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {"@type": "Question","name": "How often must CMMC compliance be affirmed?","acceptedAnswer": {"@type": "Answer","text": "After every assessment, at POA&M closeout, and annually thereafter, per 32 CFR 170.22. Level 1 affirms with each annual self-assessment. Level 2 and Level 3 affirm at assessment and then every year following the Final CMMC Status Date, even though the assessment itself is only repeated every three years."}},
    {"@type": "Question","name": "Who submits the affirmation in SPRS?","acceptedAnswer": {"@type": "Answer","text": "The Affirming Official: the senior level representative within the organization who is responsible for CMMC compliance and has the authority to affirm continuing compliance under 32 CFR 170.22(a)(1). They need a PIEE account with the SPRS Cyber Vendor User role to complete it."}},
    {"@type": "Question","name": "What happens if you don't affirm in SPRS?","acceptedAnswer": {"@type": "Answer","text": "Your CMMC status is no longer current, and under DFARS 252.204-7021 the contracting officer cannot make an award, exercise an option, or extend the period of performance on contracts that carry a CMMC requirement."}},
    {"@type": "Question","name": "How long is a CMMC certification good for?","acceptedAnswer": {"@type": "Answer","text": "A Level 2 CMMC status, self-assessed or C3PAO-certified, is valid for three years. The affirmation behind it must be renewed annually within that window."}},
    {"@type": "Question","name": "Is the CMMC affirmation legally binding?","acceptedAnswer": {"@type": "Answer","text": "Yes. It is a certification submitted to the federal government, and a false affirmation carries False Claims Act exposure for both the company and the individual Affirming Official who signed it."}}
  ]
}
</script>

## Sources

- [32 CFR 170.22, Affirmation](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.22) (eCFR)
- [32 CFR 170.15, CMMC Level 1 self-assessment and affirmation requirements](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.15) (eCFR)
- [32 CFR 170.16, CMMC Level 2 self-assessment and affirmation requirements](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.16) (eCFR)
- [32 CFR 170.17, CMMC Level 2 certification assessment and affirmation requirements](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.17) (eCFR)
- DFARS 252.204-7021, Contractor Compliance with the Cybersecurity Maturity Model Certification Level Requirements (effective November 10, 2025)
- Affirming Official Tutorial for CMMC, Supplier Performance Risk System, DISA (sprs.csd.disa.mil)
