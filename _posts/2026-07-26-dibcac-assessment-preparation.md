---
layout: post
title: "How to Prepare for a DIBCAC Assessment: The Government Audit the CMMC Pause Did Not Touch"
date: 2026-07-26
description: "CMMC Phase 2 is suspended, but DIBCAC assessments are not. What DFARS 252.240-7997 obligates you to provide, what Medium and High assessments involve, and how to prepare."
category: cmmc
tags: [CMMC, NIST 800-171, DIBCAC, DCMA, DFARS, SPRS, assessment]
image: /blog/images/1-dibcac-assessment-preparation-hero.png
author: CyberZ
---

*On July 13 the Department suspended the assessment everybody was preparing for. It left the one nobody talks about fully in place.*

**A DIBCAC assessment is a government-led review of your NIST SP 800-171 implementation, conducted by the Defense Industrial Base Cybersecurity Assessment Center, a component of the Defense Contract Management Agency. Under DFARS 252.240-7997, the clause that replaced 252.204-7020 in February 2026, you are contractually required to provide access to your facilities, systems, and personnel so the government can conduct a Medium or High assessment. The resulting score is posted to SPRS by the government, not by you. The July 13, 2026 suspension of CMMC Phase 2 paused third-party certification. It did not pause this.**

<div class="key-takeaways" style="border-left:4px solid #EE4C48;background:#15151a;padding:18px 24px;margin:28px 0;border-radius:6px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;">
<li>The Department suspended CMMC Phase 2 on July 13, 2026 and said it will keep enforcing compliance during the pause through self-assessments and selected government-led assessments. Government-led means DIBCAC.</li>
<li>DFARS 252.240-7997 defines only Medium and High assessments. Both are performed by the government. There is no longer a "Basic" assessment definition in the clause text.</li>
<li>The clause obligates you to provide access to facilities, systems, and personnel. You do not get to decline a DIBCAC assessment the way you can postpone a C3PAO engagement.</li>
<li>In June 2026 the Justice Department settled a False Claims Act case for $507,144 after a DCMA assessment scored a contractor at -170 against a self-reported 110. There was no breach and no whistleblower.</li>
<li>Preparation is the same evidence work CMMC required. What changed is who shows up and how little warning you get.</li>
</ul>
</div>

## What DIBCAC Is, and Why It Matters More This Month Than Last

The Defense Industrial Base Cybersecurity Assessment Center sits inside the Defense Contract Management Agency. Its job is to verify that defense contractors have actually implemented the 110 security requirements in NIST SP 800-171, rather than taking the contractor's word for it.

For most of the last three years, DIBCAC was a background actor for small subcontractors. The attention went to CMMC and the C3PAO ecosystem, because that was the thing with a deadline attached. DIBCAC was something that happened to large primes and to organizations on programs of particular interest.

That changed on July 13, 2026, when the Department suspended CMMC Phase 2 and the November 10 third-party certification milestone, and opened a 60-day review of the program. The suspension announcement was explicit that enforcement continues in the interim through self-assessments and selected government-led assessments.

Read that phrase carefully. Government-led assessment is not a vague policy gesture. It is a defined term with a clause behind it, a methodology behind that, and a scoring system that feeds a federal database. The third-party layer went away. The government layer did not.

If you have not read the companion piece on what the suspension did and did not change, start with [Is CMMC Still Required? What the Phase 2 Suspension Did and Did Not Change]({% post_url 2026-07-19-is-cmmc-still-required %}).

## The Clause That Lets the Government In

On February 1, 2026, a DoD class deviation restructured a large part of the cybersecurity clause set. DFARS 252.204-7019 was eliminated. DFARS 252.204-7020 was renumbered to DFARS 252.240-7997 under a new DFARS Part 240. FAR 52.204-21 became FAR 52.240-93. We covered the mechanics of that shift in [DFARS 7019 Is Gone. Do You Still Need an SPRS Score?]({% post_url 2026-06-16-dfars-7019-deleted-sprs-score %}).

The renumbering was not cosmetic. The old 7020 defined three assessment types: Basic, Medium, and High. The revised clause removed the Basic definition entirely. What remains in 252.240-7997 are two assessment types, and both of them are performed by the government.

The operative sentence, carried forward from 7020, is the access obligation. The contractor shall provide access to its facilities, systems, and personnel necessary for the government to conduct a Medium or High NIST SP 800-171 DoD Assessment.

That sentence is the whole reason this article exists. A C3PAO engagement is a contract you sign, schedule, and can postpone. A DIBCAC assessment is an obligation you already agreed to when you accepted a contract carrying the clause. The distinction matters more now that the C3PAO track is on hold and the government track is what the Department says it will lean on.

## Medium and High: The Two Assessments That Remain

![DIBCAC Medium versus High assessment comparison showing scope, method, and confidence level for each](/blog/images/2-dibcac-medium-vs-high-assessment.png)

The two assessment types differ in depth, in method, and in the confidence level attached to the resulting score.

| | Medium Assessment | High Assessment |
|---|---|---|
| Performed by | Government | Government |
| Basis | Review of your system security plan and supporting documentation | NIST SP 800-171A assessment procedures |
| Method | Documentation review, no on-site verification | Verification, examination, and demonstration of the SSP |
| Confidence level | Medium | High |
| Score posted to SPRS by | Government | Government |

A Medium assessment tests whether your system security plan describes an implementation that would actually satisfy the requirement. It is a paper exercise in the sense that nobody watches your multifactor authentication prompt fire, but it is not a rubber stamp. Assessors read the SSP looking for descriptions that do not properly address the requirement they claim to address.

A High assessment goes further. It runs on NIST SP 800-171A, the same publication that breaks the 110 requirements into 320 assessment objectives and grades each through examine, interview, and test. The clause language for a High assessment includes verification, examination, and demonstration. Demonstration means someone asks you to make the control work while they watch.

If you want the objective-level detail, the walkthrough is in [CMMC Evidence Checklist: What a C3PAO Examines, Interviews, and Tests]({% post_url 2026-06-12-cmmc-evidence-checklist-c3pao %}). The methods are identical whether the assessor works for a C3PAO or for the government. Only the badge changes.

## What a Bad Score Costs: The LOGZONE Settlement

![Chart showing LOGZONE self-reported SPRS score of 110 against a DCMA-assessed score of negative 170](/blog/images/3-dibcac-sprs-score-gap-logzone.png)

On June 18, 2026, the Justice Department announced that LOGZONE Inc., a logistics contractor based in Huntsville, Alabama, agreed to pay $507,144 to resolve False Claims Act liability for knowingly failing to comply with cybersecurity requirements in two Navy contracts.

The Department's own account of the case is short and worth sitting with. From May 2021 to March 2025, LOGZONE allegedly failed to implement certain NIST SP 800-171 controls that, if not implemented, could lead to significant exploitation of the system or exfiltration of sensitive defense information. Those issues were identified when the Defense Contract Management Agency assessed the company's implementation of the controls. The assessment produced a score of -170, at the low end of a range that runs from -203 to 110.

According to the settlement agreement as reported by DefenseScoop, LOGZONE had submitted a self-assessed score of 110 in October 2021. That is the maximum possible score, the one that says every control is fully implemented.

Three details make this the most instructive enforcement action in the current cycle.

**There was no breach.** Nothing was exfiltrated as far as the public record shows. The liability came from billing on contracts whose cybersecurity terms the company had not met while representing that it had.

**There was no whistleblower.** As Foley & Lardner noted in its analysis, this was not a relator case. A government assessment produced a finding, and the finding produced a referral to the Justice Department. The assessment was the enforcement mechanism.

**The dollar figure is small.** The company received a little over $682,000 under the two contracts. Assistant Attorney General Brett A. Shumate's statement made clear the Department intends to keep investigating these violations. Enforcement here is not reserved for eight-figure primes.

The gap between a self-reported 110 and an assessed -170 is not a rounding error or a methodology dispute. It is the distance between what a company said and what was true, and under the False Claims Act that distance is the whole case.

## What DIBCAC Actually Looks At

The short answer is your system security plan, and then everything that is supposed to be behind it.

The SSP is the spine. Every requirement in NIST SP 800-171 has to be described in it, and the description has to say how the requirement is met in your environment, not restate the requirement in different words. A meaningful share of findings come from SSP descriptions that sound compliant and describe nothing specific.

Underneath the SSP sits the evidence. Policies, procedures, configuration baselines, system inventories, scan results, access reviews, training records, incident response artifacts. For a High assessment these get mapped against the 320 objectives in 800-171A, and an objective you cannot evidence fails the requirement it belongs to, which costs you points on a weighted scale.

Then there are the people. Interviews are part of both assessment types in practice, and they surface a specific failure mode: a control that exists on paper and in configuration, but that nobody in the building can explain or has ever operated. That gap is visible in about ninety seconds of conversation.

The evidence work is the same work described in [NIST 800-171 Self-Assessment Evidence: What Backs Your Score Now That No Assessor Is Coming]({% post_url 2026-07-22-nist-800-171-self-assessment-evidence %}). The difference is the audience.

## How to Prepare for a DIBCAC Assessment

![Five preparation steps for a DIBCAC assessment covering SSP currency, evidence mapping, POA&M dates, named control owners, and a defensible SPRS score](/blog/images/4-dibcac-assessment-evidence-checklist.png)

Preparation is not a project you start when the notification arrives. By then the useful window has closed. The work below is what a 20 to 50 person shop can realistically hold in a ready state.

**Make the SSP describe the system you actually run.** Not the system you designed two years ago, not the one in the template you bought. If you moved to a new MDM, changed identity providers, or added a cloud enclave, the SSP has to reflect it. An SSP that describes a decommissioned environment is worse than a thin one, because it reads as a misrepresentation rather than a gap.

**Map evidence to objectives, not to controls.** Requirement-level organization feels tidy and falls apart in an assessment, because the assessor is working through 800-171A at the objective level. One requirement can carry six objectives, and you need something for each. This is the single highest-yield change most shops can make to their prep.

**Put real dates on the POA&M.** An open item with a credible remediation date is a manageable finding. An open item that has been rolling forward for eighteen months with no movement reads as a decision not to comply.

**Name a human for each control family.** Someone who can answer for access control, someone for audit and accountability, someone for incident response. They do not have to be different people in a small shop. They do have to exist and know what they own.

**Make your SPRS score defensible line by line.** You should be able to open the scoring worksheet and point to the evidence behind every requirement you claimed. If you cannot do that for a given requirement, the honest move is to lower the score before someone else does it for you. The LOGZONE case is what happens when that reconciliation never occurs.

The [CMMC Level 2 Evidence Tracker for NIST 800-171 Audit](https://payhip.com/b/LN2UB) ($67) is the objective-level mapping described above, built as a working Excel file rather than a checklist.

If your SPRS score is the part that worries you, the [NIST 800-171 SPRS Score Workbook for CMMC Level 2](https://payhip.com/b/R5g4Y) ($87) walks the weighted scoring the government uses, so the number you post is one you can defend.

For a shop starting from scratch on all five items above, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) bundles the scoping, SSP, evidence, POA&M, and scoring tools together. It is built for the case where a prime has flowed down a compliance demand and you need a defensible position before the next contract action, not a twelve-month consulting engagement.

## Frequently Asked Questions

**Can I request a DIBCAC assessment?**
No. Medium and High assessments are conducted by the government. They are not services you procure. Contractors who want a rehearsal engage a consultant or a C3PAO for a mock or gap assessment, which carries no official standing but surfaces the same problems.

**Does the CMMC Phase 2 suspension mean DIBCAC stopped?**
No. The suspension paused the third-party certification requirement. The Department stated it will continue enforcing compliance during the interim through self-assessments and selected government-led assessments.

**What is the difference between DIBCAC and a C3PAO?**
DIBCAC is a government organization inside DCMA that assesses compliance with DFARS cybersecurity requirements. A C3PAO is an accredited private company that conducts CMMC certification assessments. Both use NIST SP 800-171A methods. Only one of them can refer you to the Justice Department.

**How much warning do I get?**
Public accounts of notification periods vary, and the specifics are not something to plan around. The practical answer is that the preparation window is the time before the call, not after it.

**Does this apply to me if I only handle FCI?**
The access obligation in DFARS 252.240-7997 is scoped to systems required to comply with NIST SP 800-171 under DFARS 252.204-7012. If your contracts carry 7012 because you handle CUI, this applies. Contractors handling only FCI sit under FAR 52.240-93, the renumbered basic safeguarding clause.

## The Bottom Line

The July 13 suspension removed a deadline. It did not remove an obligation, and it narrowed the field of people who can verify your compliance down to one: the government. DFARS 252.240-7997 already gives them access to your facilities, systems, and people. NIST SP 800-171A already tells them what to look for. SPRS already holds a number you attested to.

LOGZONE is the case study for what happens when that number and the evidence behind it diverge. No breach, no whistleblower, $507,144. The assessment found the gap and the gap was the violation.

The preparation work has not changed since June. The reason to do it has.

## Sources

- U.S. Department of Justice, Office of Public Affairs, "Alabama Defense Contractor Agrees to Pay $507,144 to Resolve False Claims Act Liability Relating to Cybersecurity Violations," June 18, 2026 — justice.gov
- DFARS 252.204-7020, NIST SP 800-171 DoD Assessment Requirements (definitions and access obligation carried into 252.240-7997) — acquisition.gov
- DoD class deviation 2026-O0025, DFARS Part 240 and clause 252.240-7997, effective February 1, 2026 — acq.osd.mil
- NIST SP 800-171 Revision 2, Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations — csrc.nist.gov
- NIST SP 800-171A, Assessing Security Requirements for Controlled Unclassified Information — csrc.nist.gov
- NIST SP 800-171 DoD Assessment Methodology, Version 1.2.1 — acq.osd.mil
- CMMC Program Final Rule, 32 CFR Part 170 — ecfr.gov
- Federal News Network, "Pentagon suspends CMMC phase two requirements, launches review of program," July 13, 2026
- WilmerHale, "Pentagon Suspends CMMC Phase 2 Requirements and Launches Review of Cybersecurity Certification Program," July 20, 2026
- Foley & Lardner, "DOJ's LOGZONE Settlement Highlights FCA Risk in Cybersecurity Compliance Representations," July 2026
- DefenseScoop, "Defense contractor settles cybersecurity False Claims Act allegations," June 18, 2026
