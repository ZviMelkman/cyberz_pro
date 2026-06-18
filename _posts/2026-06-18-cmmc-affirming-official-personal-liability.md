---
layout: post
title: "Who Signs Your CMMC Affirmation Is Personally on the Hook"
date: 2026-06-18
description: "The CMMC affirmation in SPRS is a legal certification a named senior official signs, not an IT task. What 32 CFR 170.22 requires and the False Claims Act exposure it creates for small defense contractors."
category: CMMC
tags: [CMMC, NIST 800-171, SPRS, affirming official, False Claims Act, DFARS]
image: /blog/images/1-cmmc-affirming-official-liability-hero.png
author: CyberZ
---

*Most of the CMMC conversation in a small shop happens between IT and a consultant. The score gets calculated, the System Security Plan gets written, the results get loaded into SPRS. Then one person signs. That person, by name, is the one the government holds responsible.*

**A CMMC affirmation is a statement, submitted in the Supplier Performance Risk System (SPRS), in which a named senior official from your company attests that the organization meets and will continue to meet every applicable security requirement for its CMMC level. Under 32 CFR 170.22 that person is the Affirming Official, and the affirmation is a legal certification tied to your eligibility for the contract, not an internal IT record.**

<div style="border-left:4px solid #EE4C48;background:#18181c;padding:20px 24px;margin:28px 0;border-radius:4px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;line-height:1.65;color:#e6e6e6;">
<li>The affirmation is signed by a single named senior official inside SPRS, who is personally responsible for its accuracy (32 CFR 170.22).</li>
<li>It is not a one-time event. It is required after every assessment, at POA&amp;M closeout, and annually after that.</li>
<li>The signature converts your compliance posture into a certification the government can act on under the False Claims Act. Reckless disregard for the truth is enough; intent to defraud is not required (31 U.S.C. 3729(b)(1)).</li>
<li>DOJ recovered over $52 million across nine cyber-fraud settlements in FY2025, and in December 2025 settled its first case against a defense subcontractor.</li>
<li>The affirmation is only as defensible as the SSP and SPRS score behind it. Build that basis before anyone signs.</li>
</ul>
</div>

## What the affirmation actually is

For years, the cybersecurity requirements in DFARS 252.204-7012 ran on an honor system. Contractors were expected to implement NIST SP 800-171, but the Department of Defense had no formal mechanism to verify it before awarding a contract. The 48 CFR rule that took effect on November 10, 2025 closed that gap. CMMC status is now a condition of award, and the affirmation is the piece that ties a human being to that status.

The Affirming Official is defined in 32 CFR 170.22 as the senior level representative within your organization who is responsible for ensuring CMMC compliance and has the authority to affirm continuing compliance. In a 15-person machine shop, that is usually the owner. In a 60-person firm, it might be the president, a VP, or whoever holds signature authority over contracts. It is not a junior IT administrator, and it should not be a name picked at random because someone needed to click the button in SPRS.

What that official attests to is broad. The affirmation states that the information systems within the assessment scope are compliant with the applicable security requirements, and that the organization will maintain that compliance. For a Level 2 self-assessment, that means all 110 NIST SP 800-171 controls, with the documented basis recorded in your System Security Plan and your SPRS score.

## When you have to sign it

The single most common misread is treating the affirmation as a one-time formality that goes away once the score is in SPRS. It does not. 32 CFR 170.22 sets three separate triggers, and each one is a fresh attestation.

![Three points when the CMMC affirming official must sign in SPRS per 32 CFR 170.22](/blog/images/2-cmmc-affirmation-triggers-timeline.png)
*When the affirming official has to sign, per 32 CFR 170.22.*

The first affirmation goes in at the completion of the assessment, whether that is a self-assessment or a C3PAO certification assessment, and it rides alongside the score you enter in SPRS. If your assessment results in a Plan of Action and Milestones, a second affirmation is required when you close that POA&M out, attesting that the open items are now implemented. After that, the requirement repeats annually. DFARS 252.204-7021 reinforces this on the contract side: the clause requires the affirming official to complete and maintain a current affirmation of continuous compliance, not older than one year, and it flows that obligation down to subcontractors that handle FCI or CUI.

The practical effect is that the affirmation is not a hurdle you clear once. It is a recurring certification. Every annual cycle is a new statement of fact, made by a named person, about a security posture that may have drifted since the last time anyone looked at it closely.

## Why the signature carries personal risk

A compliance document that sits in a binder is a low-stakes object. A certification submitted to the government as a condition of payment or award is not. That is the shift the affirmation represents, and it is why the person who signs needs to understand what they are signing.

When a contractor certifies compliance with DFARS 252.204-7012 or CMMC requirements and that certification is false, the government can treat it as a false claim or a false statement material to a false claim under 31 U.S.C. 3729. The part that surprises owners is the standard for what counts as knowing.

![The three knowingly standards under the False Claims Act, 31 U.S.C. 3729(b)(1)](/blog/images/3-cmmc-fca-knowingly-standard.png)
*Under the FCA, any one of these three standards is enough. No breach required.*

Under 31 U.S.C. 3729(b)(1), "knowingly" includes actual knowledge that a statement is false, deliberate ignorance of whether it is true, and reckless disregard for its truth or falsity. There is no requirement to prove intent to defraud. An affirming official who signs without a reasonable basis for the claim, who has not read the SSP, or who has not verified that the SPRS score reflects what is actually implemented, can meet the reckless-disregard standard. The signature, not the breach, is the exposure.

This framing came directly from the enforcement side. In January 2026, a senior Department of Justice official described these cyber-fraud cases as "not about data breaches," but instead premised on misrepresentations. The government is not trying to punish firms that get attacked while compliant. It is pursuing firms that said they were compliant when they were not, and the affirmation is the cleanest record of that claim.

## The enforcement has already reached small subs

It is reasonable to assume this is a problem for primes and large contractors, not a 12-person subcontractor. That assumption stopped being safe in December 2025.

That month, the DOJ announced its first False Claims Act settlement targeting a defense subcontractor. A precision machining supplier agreed to resolve allegations that it failed to provide adequate cybersecurity, as required by DFARS 252.204-7012, for the technical drawings of parts it supplied to contractors. The settlement was roughly $421,000. The case began as a qui tam action filed by a former quality control manager, an internal employee who knew the gap between what the company claimed and what it had implemented.

That detail matters more than the dollar figure. Whistleblowers under the FCA are entitled to a share of the recovery, generally between 15 and 25 percent when the government intervenes. The people best positioned to file are exactly the ones inside your operation: IT staff, a compliance lead, a quality manager who saw the SSP and knew it did not match reality. DOJ reported a record number of qui tam filings in FY2025.

The broader numbers reinforce the direction. In its FY2025 False Claims Act report, announced January 16, 2026, DOJ recovered over $52 million across nine cybersecurity fraud settlements, and noted that cyber settlements have more than tripled in each of the past two years. Named resolutions that year included $11.2 million against a health benefits administrator and its parent for falsely certifying cybersecurity compliance, and $4.6 million against a defense contractor over a false SPRS score. Individually these are modest by FCA standards. As a pattern, they show an enforcement area that is still building.

## What to do before anyone signs

The goal here is not to scare an owner out of signing. The affirmation is a normal part of doing defense work, and most contractors will sign one truthfully for years without incident. The goal is to make sure the person signing has a defensible basis for the claim. A few concrete steps:

- **Confirm who your affirming official actually is.** Write it down. It should be a senior person with contract authority who is willing to read what they are attesting to, not a default name in SPRS.
- **Make the SSP match reality.** The affirmation references continuing compliance, and the SSP is the record of what you implemented and how. If the document describes controls you do not actually run, the signature inherits that gap. Read the SSP against your environment before the affirmation, not after a whistleblower complaint.
- **Verify the SPRS score is defensible.** The score you entered should follow the DoD scoring methodology and reflect your current state. A score that was right a year ago and wrong today is the kind of drift the annual affirmation is supposed to catch.
- **Keep your evidence.** 32 CFR 170.15 requires retaining assessment artifacts for six years. If you are ever asked to show the basis for an affirmation, that evidence is what stands between a clean record and a reckless-disregard argument.

The affirmation is only as solid as the SSP and the score behind it. If those two documents are accurate and current, the signature is a routine annual step. If they are not, the signature is where the problem becomes personal and legal.

If you are building that documented basis from scratch, the [CMMC Level 2 System Security Plan (SSP) Template](https://payhip.com/b/gB6oD) ($77) gives you the structure an assessor reads from, written to NIST SP 800-171 and the assessment objectives, so what you affirm and what your SSP says line up. If you would rather assemble the whole basis at once, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) pairs the SSP with the scoping worksheet, the SPRS score workbook, the evidence tracker, and the POA&M tracker, which together are the paper trail an affirming official signs behind ahead of an audit or a prime's request. The [NIST 800-171 SPRS Score Workbook for CMMC Level 2](https://payhip.com/b/R5g4Y) ($87) covers the score side on its own.

## The bottom line

CMMC made cybersecurity compliance a contractual condition, and the affirmation made it personal. A named senior official signs in SPRS after every assessment, at POA&M closeout, and every year after, attesting that the organization meets every applicable requirement. Under the False Claims Act, signing without a reasonable basis can be enough on its own, with no breach involved. The work that protects that signature is the same work that gets you certified: an accurate SSP, a defensible SPRS score, and the evidence to back both. Get those right before anyone clicks affirm.

---

### Sources

- 32 CFR 170.22, Affirmation. eCFR. https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.22
- 32 CFR 170.15, CMMC Level 1 self-assessment and affirmation requirements (artifact retention). eCFR.
- DFARS 252.204-7021, Contractor Compliance with the CMMC Level Requirements. Acquisition.GOV.
- 31 U.S.C. 3729, False Claims Act (definition of "knowingly").
- U.S. Department of Justice, False Claims Act Settlements and Judgments Fiscal Year 2025, announced January 16, 2026.
- U.S. Department of Justice, December 2025 settlement with a defense supply chain subcontractor (precision machining, DFARS 252.204-7012).
