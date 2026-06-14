---
layout: post
title: "What a C3PAO Actually Examines, Interviews, and Tests in a CMMC Level 2 Assessment"
date: 2026-06-14
description: "A CMMC Level 2 assessment grades 320 evidence objectives, not 110 controls. Here is what a C3PAO examines, interviews, and tests, and the evidence each method needs."
category: CMMC
tags: [CMMC, NIST 800-171, C3PAO, evidence, assessment]
image: /blog/images/1-cmmc-evidence-tracker-c3pao-hero.png
author: CyberZ
---

*You can implement all 110 controls and still walk out of a CMMC Level 2 assessment with findings. The reason is almost never the controls. It is the evidence.*

**A CMMC Level 2 assessment is an evidence review, not a controls checklist.** A Certified Third-Party Assessment Organization (C3PAO) does not grade your 110 NIST SP 800-171 controls as a simple pass or fail. It works through the 320 assessment objectives published in NIST SP 800-171A, verifies each one using up to three methods (examine, interview, and test), and a single objective you cannot prove fails the entire requirement it belongs to.

<div class="key-takeaways" style="border-left:4px solid #EE4C48;background:#15151a;padding:18px 24px;margin:28px 0;border-radius:6px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;">
<li>A Level 2 assessment grades 320 assessment objectives, not 110 controls. One unproven objective fails the whole requirement.</li>
<li>Assessors verify three ways under NIST SP 800-171A: examine your artifacts, interview your staff, test the control live.</li>
<li>A policy binder proves you wrote it down, not that the system does it.</li>
<li>Every SSP claim needs a current artifact an assessor can trace, and a test that demonstrates it.</li>
<li>Evidence with no owner and no date goes stale before assessment day.</li>
</ul>
</div>

## The grade is the objective, not the control

NIST SP 800-171 lists 110 security requirements. People call them controls and treat the count of 110 as the size of the job. The assessment does not work that way. NIST SP 800-171A decomposes those 110 requirements into 320 assessment objectives, each one a discrete determination statement an assessor scores as MET or NOT MET. For a requirement to be scored MET, every one of its objectives has to be MET.

Take 3.1.1, "limit system access to authorized users." It reads like a single line. In 800-171A it splits into several determination statements: authorized users are identified, processes acting on behalf of users are identified, devices are identified, and access is limited to each of those. Miss the statement about devices and the whole of 3.1.1 is NOT MET, even though you would have sworn the control was in place.

That is why the gap between 110 and 320 matters. You are not preparing 110 answers. You are preparing 320, and the assessor is looking for the weakest one.

![Three assessment methods in NIST SP 800-171A: examine, interview, and test](/blog/images/2-cmmc-examine-interview-test-methods.png)

## The three methods a C3PAO uses

NIST SP 800-171A gives the assessor three ways to gather evidence for an objective, and most objectives are checked with more than one.

### Examine

The assessor reads. Policies, procedures, your System Security Plan, network diagrams, configuration exports, audit logs, access-review records, training completion. Examination shows what you have written down and what your systems are set to do. The DoD's own assessment guidance is blunt about the limit: documentation shows that a policy or procedure exists, not that anyone follows it.

### Interview

The assessor talks to your people. Not the compliance lead reciting the SSP, but the system administrator and the help-desk tech who actually provisions accounts. Interviews surface the gap between the written procedure and the lived practice. If your access-control procedure says a manager approves every new account and the admin says he just creates them when HR emails, that gap is a finding.

### Test

The assessor watches the control run. Show multifactor authentication challenging a privileged login. Trigger the account lockout after the configured number of failed attempts. Pull a live audit log and show the events it captures. The DoD guidance is explicit that testing demonstrates what has or has not actually been done, where interviews capture only what staff believe and documents capture only intent. Not every objective is tested, but the ones that are cannot be talked or written around.

The pattern to internalize: examine confirms intent, interview confirms practice, test confirms reality. An objective is strongest when all three line up.

## Why a binder of policies fails

The most common preparation mistake is treating documentation as the deliverable. A contractor writes seventeen polished policies, prints them, and calls it evidence.

Documentation proves you wrote it down. It does not prove the system does it, and the assessment is designed to find exactly that gap. Your access-control policy can state that accounts lock after five failed attempts; if the assessor tests it and the account does not lock, the objective is NOT MET, and the clean policy on file does not save you. Your configuration-management program can require baseline configurations under 3.4.1; if you cannot produce the baseline and show the running system matches it, the policy is just paper.

![The evidence chain: policy, procedure, implementation, artifact, mapped in the SSP](/blog/images/3-cmmc-evidence-chain-policy-to-proof.png)

Evidence is the chain from policy to procedure to implementation to a concrete artifact, with that artifact mapped back to the objective it satisfies. Break the chain anywhere and you have a finding waiting to happen.

## Your evidence has to match your SSP

Your System Security Plan is the assessor's roadmap. Required under 3.12.4, the SSP describes how each requirement is implemented and, done well, points to where the evidence lives. The assessor reads the SSP, then goes looking for the artifacts and tests that back each claim.

This is where orphaned claims surface. The SSP says CUI is encrypted in transit; the assessor asks to see the configuration and the cipher suite, and no one can produce it. The SSP describes a quarterly access review; the most recent record is fourteen months old. Every statement in the SSP is a claim the assessor can pull on. If the artifact behind it is missing, stale, or contradicts the claim, that is a finding, and a contradicted SSP raises the assessor's scrutiny on everything else.

The fix is unglamorous. Read your SSP the way an assessor will, claim by claim, and confirm each one points to a current artifact you can actually produce.

## What counts as evidence

Useful evidence falls into four buckets, and each maps to the methods above.

![Four evidence types and the assessment method each serves](/blog/images/4-cmmc-what-counts-as-evidence-checklist.png)

Documents are your SSP, policies, procedures, and plans. They are examined, and they establish intent. Records are the operational byproduct of running the controls: audit logs, change tickets, access-review sign-offs, training completion, incident records. They are examined, and they show the control operating over time. Configurations are the system state itself: settings, baseline exports, screenshots of the actual console. They are examined and often tested. Demonstrations are the control running live, and they are the strongest evidence you can offer because they are tested in front of the assessor.

A folder of documents with no records and no demonstrations is the profile of a contractor who wrote the program but never operated it. Assessors recognize it on sight.

## The stale-evidence problem

Evidence has a shelf life, and it has an owner, and most contractors manage neither.

A log from eight months ago does not prove the control is operating now. A configuration screenshot taken before the last firewall change describes a system that no longer exists. A training record for an employee who left in March is dead weight. Evidence that is not current is not evidence.

It also needs an owner. When no single person is responsible for keeping the artifact behind a given objective current, the artifact drifts out of date between the day you collect it and assessment day, often a span of months given how far out C3PAO scheduling now runs. The discipline that survives an assessment is one artifact per objective, each with a named owner and a date, refreshed on a cycle rather than scrambled together the week before.

That is the entire job of an evidence tracker: hold each of the 320 objectives against a current artifact, the method the assessor will use, and the person who owns it. The [CMMC Level 2 Evidence Tracker for NIST 800-171 Audit ($67)](https://payhip.com/b/LN2UB) is built to do exactly that, so nothing is orphaned when the assessor starts pulling threads.

## Where conditional status fits

If you go in with gaps, the rules are narrow. Conditional certification requires at least 88 of 110 requirements MET, with the remainder closed on a Plan of Action and Milestones inside 180 days, or the conditional status expires. And some one-point requirements the DoD deems fundamental to protecting CUI cannot go on a POA&M at all; they must be fully implemented and provable before the assessment. A POA&M covers a small set of remaining gaps. It is not a substitute for evidence you never collected.

## The bottom line

A C3PAO does not grade what you have. It grades what you can prove, objective by objective, through examination, interview, and test. The contractors who pass treat evidence as the product: every one of the 320 assessment objectives tied to a current artifact, an owner, and where applicable a demonstration that the control works. The control work is the easier half. Proving it is the assessment.

If you are scoping the full path from readiness to a scheduled assessment, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools ($147)](https://payhip.com/b/LutGC) bundles the evidence tracker with the SSP, asset-scoping, SPRS, and POA&M tools, so the SSP claims, the scope, and the evidence all reference the same system. It is built for a small contractor standing up a Level 2 program without a dedicated compliance team.

## Sources

- NIST SP 800-171 Rev. 2, *Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations* (110 security requirements).
- NIST SP 800-171A, *Assessing Security Requirements for Controlled Unclassified Information* (320 assessment objectives; examine, interview, and test methods).
- DoD CIO, *CMMC Assessment Guide, Level 2* (assessment methods; MET / NOT MET scoring at the objective level).
- 32 CFR Part 170, *Cybersecurity Maturity Model Certification Program* (conditional certification, 180-day POA&M, Phase 2 effective November 10, 2026).
- NIST SP 800-171 Rev. 2, requirement 3.12.4 (System Security Plan).
