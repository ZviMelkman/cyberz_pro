---
layout: post
title: "How to Improve Your SPRS Score Without Creating False Claims Act Exposure"
date: 2026-09-06
description: "The remediation order that raises a NIST 800-171 SPRS score fastest, when you can post a corrected score, and how to document the jump so it never looks like LOGZONE."
category: cmmc
tags: [CMMC, NIST 800-171, SPRS, False Claims Act, DFARS]
image: /blog/images/1-improve-sprs-score-remediation-order-hero.png
author: CyberZ
---

*Raising the number is the easy part. Two DOJ settlements were built on scores that went up, or stayed up, without the evidence to match.*

**Improving an SPRS score means fully implementing unmet NIST SP 800-171 controls, re-running the self-assessment under the DoD Assessment Methodology, and posting the corrected score to the Supplier Performance Risk System with dated evidence behind every regained point. The fastest path runs through the 42 five-point controls, which carry roughly two-thirds of the total available weight, and through the two variable controls (3.5.3 multi-factor authentication and 3.13.11 FIPS-validated cryptography) where partial implementation still costs 3 points each.**

<div style="border:1px solid #EE4C48;border-left:6px solid #EE4C48;background:#0D0D0F;color:#ffffff;border-radius:6px;padding:22px 26px;margin:28px 0;">
  <p style="margin:0 0 14px;font-weight:700;letter-spacing:1px;color:#EE4C48;">KEY TAKEAWAYS</p>
  <ul style="margin:0;padding-left:20px;line-height:1.6;">
    <li>Prioritize by weight, not by control number: 42 controls deduct 5 points each, 14 deduct 3, 52 deduct 1. The five-pointers include all 17 FAR 52.204-21 basic safeguards.</li>
    <li>Two controls give partial credit: MFA (3.5.3) costs 5 points with no MFA, 3 if general users still lack it. FIPS crypto (3.13.11) costs 5 with no encryption, 3 if encryption is not FIPS-validated.</li>
    <li>You can post a corrected score at any time. DFARS 252.204-7019 only requires the score on file to be less than three years old, and the risk lives in the delay, not the update.</li>
    <li>LOGZONE self-assessed 110 in October 2021, was assessed at -170 by DIBCAC in 2024, never corrected the number, and settled with DOJ for $507,144 in June 2026.</li>
    <li>Every regained point needs evidence dated before the new score posts: the updated SSP, the assessment worksheet, and the artifact proving the control works.</li>
  </ul>
</div>

For most of the defense industrial base, the third-party assessment calendar is gone. On July 13, 2026, the Department of War suspended CMMC Phase 2 and put the program under a Reform Task Force review, with the public report expected in late September. What did not go anywhere: the self-assessed score sitting in SPRS under DFARS 252.204-7019, the annual affirmation under 32 CFR 170.22, and the Department of Justice's willingness to treat the gap between that score and reality as a False Claims Act case.

That combination changes what "improve your SPRS score" means. It is no longer a race to be assessment-ready by November 10. It is a self-reported number that a DCMA or DIBCAC review can test at any time, and that you or your affirming official re-certify every year. This guide covers the three things that actually matter: which controls to fix first, when you are allowed to post the new score, and how to document the improvement so the jump itself never becomes evidence.

## Why Is Improving Your SPRS Score Still Urgent With Phase 2 Suspended?

Because the enforcement mechanism that has actually collected money never depended on Phase 2.

LOGZONE Inc., a Huntsville, Alabama logistics contractor, self-assessed a perfect 110 in October 2021. A DIBCAC assessment in February 2024 scored the same environment at -170, near the floor of the -203 to 110 range. The company never corrected the number, kept billing two Navy contracts, and on June 18, 2026 settled False Claims Act allegations with DOJ for $507,144. No breach. No Phase 2. No C3PAO. Just the distance between the posted score and the assessed one.

![Timeline showing LOGZONE's self-assessed 110 in October 2021, DIBCAC's -170 assessment in February 2024, and the $507,144 DOJ settlement in June 2026](/blog/images/3-sprs-score-logzone-gap-timeline.png)

MORSECORP ran the same pattern from the other direction: a $4.6 million settlement in March 2025, in part because it took months to correct scores it knew were wrong. The lesson from both cases is identical. The score is a representation to the government, and the government now checks.

So a low-but-honest score is a business problem: contracting officers see it, primes see the affirmation status, and it costs you work. An inflated score is a legal problem. The only good position is a score that is higher *and* true, which is what the rest of this guide is about. If you have not read how the number is calculated in the first place, start with the [scoring walkthrough]({% post_url 2026-06-19-how-nist-800-171-sprs-score-calculated %}) and come back.

## Which Controls Should You Fix First to Raise the Score Fastest?

Sort your gap list by point weight, not by control family order. The DoD Assessment Methodology assigns every unmet control a deduction of 5, 3, or 1 point, and the distribution is lopsided:

![Table of DoD Assessment Methodology control weights: 42 controls at 5 points, 14 at 3 points, 52 at 1 point, and 2 variable controls](/blog/images/2-sprs-score-control-weights-table.png)

The 42 five-point controls carry 210 of the 314 total deductible points, roughly two-thirds of the entire scoring range. They include all 17 basic safeguards from FAR 52.204-21, the ones every federal contractor already committed to for FCI. If any of those 17 are unmet, they are both your biggest point recovery and your hardest gap to explain, because you attested to them the day you signed any federal contract.

The practical order of operations:

1. **Unmet five-point controls with cheap fixes.** Access control basics, session lock, unsuccessful-logon limits, physical access items. Many are configuration changes, not purchases. Each one is +5.
2. **The two variable controls.** MFA (3.5.3) deducts 5 points if it is missing entirely, but only 3 if it covers remote and privileged users while general users still lack it. FIPS-validated cryptography (3.13.11) deducts 5 with no encryption of CUI, 3 if you encrypt but the modules are not FIPS-validated. Moving from nothing to partial buys 2 points each; finishing the job buys the rest. These are the only two places in the methodology where partial implementation earns anything.
3. **Three-point controls that share infrastructure with fixes you already made.** If deploying MFA meant standing up a modern identity platform, several three-pointers in the Identification and Authentication family may now be one policy away.
4. **The 52 one-point controls last.** They are the long tail. A contractor who spends the first month on documentation-heavy one-pointers while five-point technical gaps sit open has optimized the wrong list.

One structural note before any of it: control 3.12.4, the System Security Plan, has no point value because without a current SSP there is no valid score to post at all. Every control you remediate has to land in the SSP as an update, which is where the documentation section below comes in.

## When Are You Allowed to Post a Corrected Score?

Any time. This is the most misunderstood part of the system.

DFARS 252.204-7019 requires the score in SPRS to be current, meaning not more than three years old, at the time of contract award. Nothing in the clause restricts how often you can reassess and post. When you complete remediation, you re-run the self-assessment under the methodology, record the new assessment date, and post the new summary-level score. The three-year clock restarts from the new assessment date.

The risk is not updating too often. The risk is the LOGZONE posture: a stale, wrong number left standing while invoices go out. Under 32 CFR 170.22, a senior official also affirms continuous compliance annually and after any POA&M closeout, so every year that a wrong score survives, someone re-signs it. The [affirmation analysis]({% post_url 2026-08-23-cmmc-affirmation-false-claims-act %}) covers why that signature, not the assessment, is now the sharpest edge of FCA exposure.

Two timing rules worth adopting as policy:

**Post within the same week remediation completes.** MORSECORP's settlement documents the cost of sitting on a known-wrong score. If you know the number changed, in either direction, the paper trail should show you acted on that knowledge promptly.

**Never post ahead of the work.** A score that reflects planned remediation is exactly the misrepresentation DOJ's Civil Cyber-Fraud Initiative was built to chase. A control counts when it is implemented and evidenced, not when it is scheduled. If you are tempted to count a POA&M item as done, the [POA&M eligibility breakdown]({% post_url 2026-06-15-cmmc-poam-eligibility-what-you-can-defer %}) covers what deferral actually permits.

## How Do You Document the Improvement So the Jump Isn't the Story?

Assume a future DIBCAC assessor, or a DOJ attorney, looks at your SPRS history and sees a score that moved from 45 to 88 in one quarter. That trajectory is either the record of a company that did the work, or the opening exhibit in a misrepresentation case. The difference is entirely in what exists behind the number, dated before the post.

For every regained point, three artifacts:

**The evidence the control works.** Screenshots of enforced configuration, MFA enrollment reports, FIPS module validation certificates by number, access control lists, training completion logs. Dated, stored, and named to the control.

**The SSP update.** The control's implementation description changes from gap to implemented, with the date and the how. An SSP that still describes the old state contradicts your own score.

**The assessment worksheet.** Keep the completed DoD Assessment Methodology worksheet from each reassessment, showing the per-control determinations that produced the number. When two scores are three months apart, the two worksheets are what make the delta legible.

This is also the honest answer to a question contractors ask quietly: does raising the score quickly look suspicious? No. DIBCAC assessed LOGZONE at -170, and remediating from a number like that necessarily produces a steep curve. What looks suspicious is a steep curve with no artifacts underneath it, or a score that jumped the day before a contract award. Speed with evidence reads as diligence. Speed without it reads as MORSECORP.

## What Does a Realistic 90-Day Improvement Look Like?

Take a 20-person machine shop that scored itself honestly at 45: ten unmet five-point controls, five unmet three-point controls, and an accurate SSP. Total gap: 65 points.

A 90-day push that closes seven of the five-point controls, brings MFA from nothing to full coverage, and gets CUI encryption onto FIPS-validated modules recovers 35 points from the seven controls plus 10 from the two variable controls, landing the score at 90. That crosses the 88 threshold that matters for conditional Level 2 status under 32 CFR 170.21, and it is achievable because most five-point gaps at small contractors are configuration and coverage problems, not capital projects.

The same 90 days spent clearing one-point documentation controls would have moved the score less than 15 points. Weight ordering is the whole game.

## The Bottom Line

With Phase 2 suspended, your SPRS score and the annual affirmation behind it are the entire surface where compliance meets enforcement. Improving the score is a sorting problem and a paperwork problem: fix the 42 five-point controls first, harvest the partial credit on MFA and FIPS crypto, post the corrected score the same week the work completes, and keep the dated evidence that makes the improvement a record instead of a red flag. LOGZONE's $507,144 settlement was not the price of a low score. It was the price of a wrong one, left standing while the invoices kept going out.

The [NIST 800-171 SPRS Score Workbook for CMMC Level 2](https://payhip.com/b/R5g4Y) ($87) walks every control with its exact weight, tracks per-control evidence, and recalculates your score as you remediate. If you are starting from the "where do I even begin" position, with no current SSP and no gap list, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) bundles the workbook with the SSP template, evidence tracker, scoping worksheet, and POA&M tools, the full set for getting from an honest low score to a documented high one.

## Sources

- U.S. Department of Justice, "Alabama Defense Contractor Agrees to Pay $507,144 to Resolve False Claims Act Liability Relating to Cybersecurity Violations," June 18, 2026
- U.S. Department of Justice, MORSECORP Inc. settlement announcement, March 26, 2025
- NIST SP 800-171 DoD Assessment Methodology, Version 1.2.1
- DFARS 252.204-7019 and 252.204-7020
- 32 CFR Part 170 (§170.21, §170.22)
- Department of War memorandum suspending CMMC Phase 2, July 13, 2026
- FAR 52.204-21
