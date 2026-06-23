---
layout: post
title: "The CMMC Affirming Official: Who Signs, and What Their Name Is Actually On"
date: 2026-06-23
description: "Who is the affirming official for CMMC, what the annual affirmation under 32 CFR 170.22 attests to, and why that one signature carries personal False Claims Act liability every year."
category: cmmc
tags: [CMMC, NIST 800-171, Affirming Official, SPRS, False Claims Act]
image: /blog/images/1-cmmc-affirming-official-hero.png
author: CyberZ
---

*A contractor can pass an assessment, record a clean SPRS score, win the contract, and still have a senior executive personally exposed under federal fraud law. The exposure does not come from the assessment. It comes from the signature that follows it.*

**The CMMC affirming official is the senior company representative who personally attests, inside the Supplier Performance Risk System (SPRS), that the organization has implemented and will keep implementing all applicable CMMC security requirements. Under 32 CFR 170.22 that person is defined as the senior-level representative with the authority to affirm continuing compliance, and they must affirm after every assessment, after any POA&M closeout, and again every year. It is a separate, legally distinct step from entering a score, and it is the step that attaches a name to the claim.**

<div class="callout" markdown="0" style="border:1px solid #EE4C48;border-left:6px solid #EE4C48;background:#161618;padding:18px 22px;border-radius:6px;margin:28px 0;">
  <strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
  <ul style="margin:12px 0 0;padding-left:20px;line-height:1.55;">
    <li>The affirming official is a single senior official, not a committee and not your IT vendor. 32 CFR 170.22 requires someone with the authority to bind the company.</li>
    <li>The affirmation is a separate action from the SPRS score. You can submit a score and still be out of compliance for failing to affirm.</li>
    <li>It repeats. The affirmation is required at assessment, at POA&amp;M closeout, and annually thereafter, so the exposure is recurring, not one-time.</li>
    <li>Under the False Claims Act, "knowingly" includes reckless disregard. The official does not need intent to defraud to create liability.</li>
    <li>In FY2025 the DOJ recovered over $52 million across nine cybersecurity fraud settlements, and several turned on misrepresented compliance, not on any breach.</li>
  </ul>
</div>

## Who the affirming official actually is

Defense contractors tend to treat CMMC as an IT project. Scope the systems, fix the controls, run the assessment, enter the number. The affirmation gets handled as one more checkbox, often by whoever happens to have the SPRS login.

The regulation does not see it that way. Under 32 CFR 170.22, the affirming official is the senior-level representative from within the organization who is responsible for ensuring the company's compliance with CMMC and who has the authority to affirm that compliance on the company's behalf. That is a deliberate choice of words. The Department of Defense wanted the attestation tied to someone who can be held to it, not to a technician executing a task.

In a small defense subcontractor, that is usually the owner, the president, or the CFO. It is the person whose name carries weight on a contract and whose signature a court will treat as the company speaking. When that official affirms, they are not confirming that the IT team did some work. They are stating, on the federal record, that the organization meets the requirements and will continue to.

## Your SPRS score and your affirmation are two different things

This is the part that catches people. Entering a score in SPRS and affirming compliance in SPRS are separate steps, and doing the first does not satisfy the second.

![Comparison graphic showing the SPRS score as a number you enter, contrasted with the affirmation as a senior official personally attesting under the False Claims Act, with a footer noting the affirmation is a separate step.](/blog/images/2-cmmc-affirming-official-score-vs-affirmation.png)

A score records where you say you stand against the 110 requirements in NIST SP 800-171 Revision 2. The affirmation is a named official going on record that the picture the score paints is true and that the company will maintain it. DFARS clause 252.204-7021 makes the point explicit: the contractor must complete, on an annual basis and maintain as current, an affirmation of continuous compliance by the affirming official in SPRS, for each system that processes, stores, or transmits FCI or CUI.

Two practical consequences follow. A contractor who submits a score but never completes the affirmation is not compliant, regardless of how high the number is. And a contractor whose conditions change after a clean affirmation, a new system added to scope, a control that quietly lapsed, has affirmed something that is no longer accurate. The affirmation is a continuing statement, not a snapshot. If you want the mechanics of the number itself, the [SPRS scoring walkthrough]({% post_url 2026-06-10-nist-800-171-sprs-score %}) covers how the weighting actually works.

## Why one signature now carries personal, recurring liability

For years the entire NIST 800-171 regime ran on self-attestation that nobody verified. A contractor could claim a score, attach a long Plan of Action and Milestones, and move on. The risk of being wrong was theoretical.

Two changes ended that. First, third-party verification. Starting November 10, 2026, Phase 2 of the CMMC rollout under 32 CFR Part 170 makes a C3PAO certification assessment the default for Level 2 contracts involving CUI, so an outside assessor now checks the claim against your System Security Plan and your evidence. Second, the affirmation itself became an enforcement hook for the False Claims Act.

Here is the mechanism. When a company certifies compliance with a cybersecurity requirement as a condition of contract eligibility or payment, and that certification is false, it can be a false claim or a false statement material to a false claim under 31 U.S.C. 3729. The affirmation is exactly that kind of certification, and it is signed by a named person. The standard for liability is lower than most owners assume. Under the statute, "knowingly" means actual knowledge, deliberate ignorance of the truth, or reckless disregard for it. There is no requirement to prove intent to defraud. An official who signs a compliant status while real gaps sit in plain view can satisfy the standard without ever meaning to deceive anyone.

The enforcement is not hypothetical, and it is accelerating.

![Statistic graphic reading 52 million dollars recovered across 9 cybersecurity settlements in fiscal year 2025, with notes that cyber recoveries tripled two years running, averaged about 5.77 million dollars, and that a record 1,297 whistleblower suits were filed. Source: U.S. Department of Justice, January 2026.](/blog/images/3-cmmc-affirming-official-fca-enforcement.png)

In its FY2025 report, released January 16, 2026, the DOJ recorded over $52 million recovered across nine cybersecurity fraud settlements, part of a record $6.8 billion in total False Claims Act recoveries. Cyber recoveries have more than tripled in each of the past two years. A record 1,297 whistleblower suits were filed that year, and relators typically collect between 15 and 30 percent of a recovery, which means the person most likely to report a false affirmation is often an employee who knows the compliance posture firsthand.

The named settlements show the pattern clearly:

<table style="width:100%;border-collapse:collapse;margin:22px 0;font-size:0.95em;">
  <thead>
    <tr style="border-bottom:2px solid #EE4C48;text-align:left;">
      <th style="padding:8px 10px;">Contractor</th>
      <th style="padding:8px 10px;">Amount</th>
      <th style="padding:8px 10px;">Core allegation</th>
    </tr>
  </thead>
  <tbody>
    <tr style="border-bottom:1px solid #333;">
      <td style="padding:8px 10px;">Health Net Federal Services / Centene</td>
      <td style="padding:8px 10px;">$11.2M</td>
      <td style="padding:8px 10px;">Falsely certified cybersecurity compliance on a TRICARE military health contract</td>
    </tr>
    <tr style="border-bottom:1px solid #333;">
      <td style="padding:8px 10px;">Illumina</td>
      <td style="padding:8px 10px;">$9.8M</td>
      <td style="padding:8px 10px;">Sold systems with known security vulnerabilities and misrepresented compliance</td>
    </tr>
    <tr style="border-bottom:1px solid #333;">
      <td style="padding:8px 10px;">MORSECORP</td>
      <td style="padding:8px 10px;">$4.6M</td>
      <td style="padding:8px 10px;">Submitted an inaccurate SPRS score, lacked an SSP, and did not promptly correct the score after a consultant flagged it</td>
    </tr>
    <tr>
      <td style="padding:8px 10px;">Penn State</td>
      <td style="padding:8px 10px;">$1.25M</td>
      <td style="padding:8px 10px;">Missing baseline NIST 800-171 controls on federal research contracts</td>
    </tr>
  </tbody>
</table>

The MORSECORP case is the one every affirming official should read twice. The company submitted a score that was wrong, was told by an outside consultant that it was wrong, and left it standing. That gap, between what was claimed and what was true, is the entire theory of the case. No breach was required. The affirmation turns that gap from an operational shortfall into a signed statement that a court can call false.

## What a defensible affirmation actually rests on

An affirming official is not expected to personally run the assessment. They are expected to have a reasonable basis for the statement they sign. In practice that basis is a small set of documents that, taken together, let a senior person say "I have looked, and this is true" without it being a guess.

There are four pieces:

- **A scoped boundary.** You cannot affirm compliance for systems you have not defined. The asset categories under 32 CFR 170.19 tell you what is in scope before any control is scored.
- **A score you can reconstruct.** The number in SPRS should trace back to the specific requirements you assessed, not a figure someone remembers entering. MORSECORP is what happens when it does not.
- **A System Security Plan that matches reality.** The SSP is the document a C3PAO reads first, and the thing your affirmation implicitly stands behind. If it describes a system you no longer run, you are affirming fiction. Our [breakdown of what an SSP must actually contain]({% post_url 2026-06-09-cmmc-ssp-template %}) covers the gap most plans have.
- **Evidence that the controls operate.** "Implemented" under NIST 800-171A means the assessor can examine, interview, and test it. A policy with no artifact behind it is not a defensible basis for a signature.

If any of those is missing, the official is signing on faith. That is precisely the posture the False Claims Act punishes.

This is the work the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) was built to do, and it is the reason it exists as a bundle rather than five separate downloads. An affirming official's signature stands or falls on whether the scope, the score, the SSP, and the evidence agree with each other. The Kit ($147) is the documented basis that lets a senior person review four artifacts in an afternoon and sign with a reasonable basis instead of a hope. If the immediate gap is the number itself, the [NIST 800-171 SPRS Score Workbook for CMMC Level 2](https://payhip.com/b/R5g4Y) ($87) rebuilds the score line by line so what you affirm matches what you assessed.

## What to do before you sign

Five concrete moves, none of which require a consultant:

1. **Name the official in writing.** Decide who holds the affirming-official role and confirm they have the authority 32 CFR 170.22 requires. Do not let it default to whoever has the SPRS login.
2. **Confirm the affirmation was actually submitted,** not just the score. Log into SPRS and verify the affirmation step is complete and current for every applicable system.
3. **Reconstruct the score before affirming it.** If the official cannot see how the number was reached, it is not yet a basis for a signature.
4. **Read the SSP as the assessor will.** If it describes systems or controls that no longer match the environment, fix the document before the affirmation, not after.
5. **Calendar the next one.** The affirmation is annual, and it is also due at any POA&M closeout. If you are carrying open items, the [POA&M eligibility rules]({% post_url 2026-06-17-cmmc-poam-eligibility %}) and the 180-day clock change when your next affirmation comes due.

## The bottom line

CMMC moved cybersecurity from a back-office task to a personal attestation by a named executive, repeated every year, enforceable under federal fraud law. The affirming official is not certifying that work was done. They are putting their name on a continuing claim that it was done correctly and will stay that way. The defense against the downside is not optimism. It is a scoped boundary, a reconstructable score, an honest SSP, and evidence the controls run, so that when a senior person signs, the statement is simply true.

## Sources

- 32 CFR 170.22, Affirmation, and 32 CFR 170.19, Asset categories. Electronic Code of Federal Regulations, eCFR.
- DFARS 252.204-7021, Contractor Compliance With the Cybersecurity Maturity Model Certification Level Requirements. Acquisition.gov.
- 31 U.S.C. 3729, False Claims Act, including the definition of "knowingly."
- "False Claims Act Settlements and Judgments Exceed $6.8B in Fiscal Year 2025." U.S. Department of Justice, Office of Public Affairs, January 16, 2026.
- 32 CFR Part 170, CMMC Program, Phase 2 implementation timeline.
- NIST SP 800-171 Revision 2 and NIST SP 800-171A. National Institute of Standards and Technology.
