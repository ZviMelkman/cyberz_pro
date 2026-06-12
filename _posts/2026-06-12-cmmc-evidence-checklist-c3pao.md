---
layout: post
title: "CMMC Evidence Checklist: What a C3PAO Examines, Interviews, and Tests"
date: 2026-06-12
description: "A C3PAO scores 320 NIST 800-171A objectives, not 110 controls. What assessors examine, interview, and test, and the evidence file that passes."
category: cmmc
tags: [CMMC, NIST 800-171, NIST 800-171A, C3PAO, CMMC assessment]
image: /blog/images/1-cmmc-evidence-checklist-c3pao-hero.png
author: CyberZ
---

*The assessor is not grading your effort. The assessor is grading 320 pieces of proof, one objective at a time.*

**A CMMC Level 2 certification assessment is conducted by a C3PAO using the assessment procedures in NIST SP 800-171A, which break the 110 NIST 800-171 controls into 320 assessment objectives and judge each one through three evidence methods: Examine (documents, configurations, and records), Interview (the people responsible), and Test (watching the control actually work). Every objective under a control must be satisfied for that control to score Met.**

<div style="border:1px solid #EE4C48;border-left:6px solid #EE4C48;background:#0D0D0F;color:#ffffff;border-radius:6px;padding:22px 26px;margin:28px 0;">
  <p style="margin:0 0 14px;font-weight:700;letter-spacing:1px;color:#EE4C48;">KEY TAKEAWAYS</p>
  <ul style="margin:0;padding-left:20px;line-height:1.6;">
    <li>NIST SP 800-171A expands the 110 controls into 320 assessment objectives. A C3PAO works at the objective level, and one unmet objective scores the whole control Not Met.</li>
    <li>Every objective is judged through three methods: examine, interview, and test. Interviews alone do not prove a control; DoD's own assessment guidance treats them as what staff believe, not what is implemented.</li>
    <li>The assessor reads your System Security Plan first. Evidence that contradicts the SSP is worse than evidence that is missing.</li>
    <li>As of June 2026 there are 103 authorized C3PAOs for roughly 80,000 organizations that need Level 2 certification, so a failed first attempt is a calendar problem, not just a findings problem.</li>
    <li>Conditional certification requires at least 88 of 110 controls Met, a 180-day POA&M window, and only one-point controls are POA&M-eligible.</li>
  </ul>
</div>

Defense contractors are booking C3PAO assessments right now for the runway to November 10, 2026, when Phase 2 of the CMMC program makes third-party Level 2 assessments the default for contracts involving CUI under 32 CFR Part 170. In a June 2026 Federal News Network interview, the CEO of one large compliance provider described firms arriving six months out, asking to be certified by the deadline, and noted that subcontractors who assumed they were exempt, including sole-source suppliers, are not. The crunch is real, and it makes one question urgent for every contractor on a C3PAO's calendar: what, exactly, will the assessor ask to see?

The answer is not a mystery. The entire assessment runs on a published NIST document, and you can read the test before you take it.

## The assessment runs on NIST 800-171A, not on your security posture

NIST SP 800-171 defines the 110 security requirements for protecting Controlled Unclassified Information on a non-federal system. Its companion document, NIST SP 800-171A (June 2018), defines how those requirements are assessed. It decomposes the 110 controls into 320 assessment objectives, granular determination statements that an assessor marks Met or Not Met one at a time.

This is the single most common surprise in a first assessment. Contractors prepare a mental checklist of 110 items. The C3PAO arrives with a checklist of 320. The CMMC rule at 32 CFR Part 170 calls the material that satisfies those objectives "objective evidence": verifiable records, system outputs, and observed practices, not assurances.

If you have posted an SPRS score, you have already met this structure once, because an honest self-assessment scores the same 320 objectives. The difference now is that someone else is checking, and the [score, the plan, and the evidence have to tell the same story]({% post_url 2026-06-09-cmmc-ssp-template %}).

## The three evidence methods: examine, interview, test

For every assessment objective, NIST SP 800-171A gives the assessor three methods for gathering evidence, and a C3PAO will typically use more than one per control.

![Three-column CyberZ infographic showing the NIST SP 800-171A evidence methods: Examine (SSP and policies, config exports, logs and inventories), Interview (admins and users, process owners, management), and Test (MFA logins, access denials, backup restores), with the line "Interviews show belief. Documents show intent. Tests show it works."](/blog/images/2-cmmc-examine-interview-test-methods.png)

**Examine** is document and artifact review: your SSP, policies and procedures, configuration exports, network diagrams, asset inventories, and logs. This is where most of the assessment hours go.

**Interview** is conversation with the people responsible: system administrators, ordinary users, process owners, and management. Assessors use interviews to check whether what the documents say actually matches how people work.

**Test** is demonstration. The assessor watches the control operate: a user logging in with MFA, an unauthorized account being denied access, a backup being restored, a session locking after the configured timeout.

DoD's own CMMC assessment guidance draws the hierarchy plainly: interviews capture what staff believe to be true, documentation shows what was planned, and testing demonstrates what has actually been done. The practical consequence is that a confident interview cannot rescue a control that has no artifact behind it. If your administrator describes a beautiful access review process and there is no dated record of a review ever happening, the objective is Not Met.

## How one control becomes six chances to fail

Take the very first requirement, 3.1.1: limit system access to authorized users, processes acting on behalf of authorized users, and devices. NIST SP 800-171A breaks it into six objectives, 3.1.1[a] through 3.1.1[f]: authorized users are identified; processes acting on their behalf are identified; authorized devices are identified; and access is actually limited to each of those three categories.

![CyberZ graphic showing six boxes labeled 3.1.1[a] through 3.1.1[f], five with green checks and one with a red X, under the headline "One control. Six objectives. One miss = Not Met."](/blog/images/3-cmmc-320-objectives-one-miss.png)

Suppose you maintain a clean user list and Active Directory enforces it, but nobody ever documented which service accounts and processes are authorized to touch CUI. Objectives [a], [c], [d], and [f] pass. Objective [b] fails. The whole control scores Not Met, the corresponding points come off your score under the DoD Assessment Methodology's 1, 3, and 5 point weights, and there is no partial credit anywhere in the system.

Multiply that pattern across 110 controls and the lesson is clear: assessment prep that works at the control level is prep for the wrong exam. The unit of work is the objective.

## What evidence actually looks like, family by family

There is no single mandated artifact list; DoD's assessment guides say so explicitly. But in practice, assessors converge on predictable evidence per control family. A sample of what a C3PAO typically asks to examine or test:

| Control family | Evidence a C3PAO typically asks for |
|---|---|
| Access Control (3.1) | Access control policy, account inventory and group exports, a demonstrated access denial, termination and offboarding records |
| Identification & Authentication (3.5) | MFA configuration exports, password policy settings, a live MFA login demonstration |
| Awareness & Training (3.2) | Training records with names and dates, role-based training content, phishing exercise results |
| Audit & Accountability (3.3) | Log retention configuration, sample logs traceable to named users and events, dated evidence of log review |
| Configuration Management (3.4) | Baseline configurations, change tickets, software inventory with allow and deny decisions |
| System & Communications Protection (3.13) | FIPS-validated encryption module certificates (CMVP numbers), firewall rules, a network diagram that matches the SSP |
| Incident Response (3.6) | The IR plan, records of a tested exercise, the DFARS 252.204-7012 72-hour reporting procedure |

Two patterns separate evidence that passes from evidence that creates findings.

First, evidence must be dated and attributable. A policy with no revision date, a training record with no names, or a screenshot with no timestamp invites the question of whether the control was operating before assessment week.

Second, evidence must trace to the SSP. The assessor reads your System Security Plan first and uses it as the map for everything else. An artifact that contradicts the SSP, a network diagram showing a system the plan never mentions, an MFA configuration narrower than the plan claims, is worse than a gap, because it puts every other claim in the document under suspicion. The Cyber AB's CMMC Assessment Process has assessors weigh whether evidence is adequate (the right kind of proof for the objective) and sufficient (enough of it to be convincing). One artifact per objective is a thin file; the contractors who pass comfortably tend to hold at least two independent artifacts for anything load-bearing.

The [CMMC Level 2 Evidence Tracker for NIST 800-171 Audit](https://payhip.com/b/LN2UB) ($67) maps every control to the evidence and assessment method that will judge it, so the gaps surface months before the assessor does.

## Why the calendar is the silent risk

The evidence problem would be manageable if a failed first attempt simply meant rescheduling. Right now it does not. As of June 2026, there are 103 authorized C3PAOs serving roughly 80,000 organizations expected to need Level 2 certification, and assessor calendars are filling through the November 10, 2026 Phase 2 start.

The scoring rules sharpen the deadline. To walk away with even a conditional Level 2 status, you need at least 88 of 110 controls Met, every open item on a Plan of Action and Milestones, a 180-day clock to close them, and the constraint that only one-point controls are POA&M-eligible. Miss the 88 floor, or fail a five-point control, and there is no conditional path; you remediate and rejoin the queue. Meanwhile, [primes are already setting their own acceptance bars]({% post_url 2026-06-08-what-your-prime-is-actually-accepting-cmmc %}) for what subcontractors must show, and "scoped, scored, scheduled, and moving" only satisfies them if the scheduled assessment actually goes well.

The contractors who clear this comfortably are not the ones with the most security spend. They are the ones whose evidence file was assembled, dated, and reconciled against the SSP before the assessment was ever booked.

## Build the evidence file this week

A practical sequence for a small contractor starting now:

1. Print or export the 320 assessment objectives from NIST SP 800-171A and treat that list, not the 110 controls, as the master checklist.
2. For each objective, record three things: the artifact that proves it, where the artifact lives, and which method (examine, interview, test) an assessor would apply to it.
3. Run your own mock pass using the same three methods. Read the document, ask the responsible person to explain it cold, then watch the control work. Anywhere the three answers disagree is a finding in waiting.
4. Reconcile everything against the SSP. Every system in the diagram appears in the plan; every control narrative points at a real, dated artifact.
5. Date-stamp and attribute every artifact, and put a named owner on keeping each one current, because evidence goes stale faster than policies do.
6. Score the result honestly against the 88-of-110 conditional floor before booking a C3PAO, and put anything unmet on a POA&M only if it is genuinely POA&M-eligible.

## The bottom line

A CMMC Level 2 assessment is an evidence exercise governed by a public document. NIST SP 800-171A tells you all 320 questions in advance and the three methods the assessor will use to check your answers. The contractors who fail are rarely the insecure ones; they are the ones who prepared for 110 questions, kept the proof in people's heads, and discovered the gap with an assessor in the room and no calendar slot left to recover.

The [CMMC Level 2 Evidence Tracker for NIST 800-171 Audit](https://payhip.com/b/LN2UB) ($67) turns the 320-objective list into a working evidence inventory with status and ownership per control. And if you are building the whole readiness picture at once before an assessment date, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) bundles the evidence tracker with the SSP template, asset scoping worksheet, SPRS score workbook, and POA&M tracker, so the plan, the score, and the proof all agree before a C3PAO reads any of them.

## Sources

- NIST Special Publication 800-171A, *Assessing Security Requirements for Controlled Unclassified Information* (June 2018): the 320 assessment objectives and the examine, interview, and test methods.
- NIST Special Publication 800-171 (Rev. 2), *Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations*: the 110 security requirements.
- DoD CMMC Assessment Guides (DoD CIO): assessment method guidance, including the distinction between interviews, documentation, and testing.
- CMMC Program rule, 32 CFR Part 170: Level 2 certification assessments, objective evidence, conditional certification (88 of 110, 180-day POA&M window), and POA&M eligibility limits.
- DoD, *NIST SP 800-171 DoD Assessment Methodology*, Version 1.2.1: the 1, 3, and 5 point control weights.
- DFARS 252.204-7012, -7019, -7020, -7021: NIST 800-171 implementation, assessment, SPRS reporting, and CMMC flow-down.
- CyberSheath announcement (June 9, 2026): 103 authorized C3PAOs serving roughly 80,000 organizations needing Level 2 certification.
- Federal News Network, interview with CyberSheath CEO Emil Sayegh (June 2026): contractors approaching the deadline six months out; no exemptions, including for sole-source subcontractors.
- Cyber AB, *CMMC Assessment Process (CAP)*: evidence adequacy and sufficiency.
