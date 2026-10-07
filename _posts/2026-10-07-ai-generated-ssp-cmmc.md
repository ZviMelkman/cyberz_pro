---
layout: post
title: "Your CMMC SSP Was Written by AI. Here Is What Happens When Someone Checks It."
date: 2026-10-07
description: "AI tools now offer a DIBCAC-ready System Security Plan in minutes. NIST SP 800-171 requirement 3.12.4 and the eight 800-171A objectives do not care who wrote the plan. They test whether it describes your actual system. DFARS 252.204-7020 defines a government assessment as validation that the requirements were implemented as described in the SSP, and LOGZONE's $507,144 settlement shows what a plan that reads better than the network costs. The three ways AI drafts fail, the data you handed over to get them, and how to use a model on an SSP without signing a false statement."
category: CMMC
tags: [CMMC, system security plan, SSP, AI-generated SSP, NIST 800-171, NIST 800-171A, CA.L2-3.12.4, DFARS 252.204-7020, DIBCAC, False Claims Act, LOGZONE, SPRS, affirming official, defense contractors]
image: /blog/images/1-ai-generated-ssp-cmmc-hero.png
author: CyberZ
---

*The pitch is now in your inbox and on the AWS Marketplace: answer a questionnaire, get a DIBCAC-ready System Security Plan in minutes. Nothing in NIST SP 800-171 or 32 CFR Part 170 says you cannot write an SSP that way. Both say exactly what the plan has to be, and the Justice Department spent this summer showing what a plan that overstates the network costs.*

**An AI-generated System Security Plan is an SSP drafted partly or wholly by a language model from a questionnaire, a template, or the text of the 110 requirements, rather than from an inspection of the system it describes. Neither NIST SP 800-171 Rev 2 nor 32 CFR Part 170 regulates how an SSP is written. Both regulate what it must be. Requirement 3.12.4 calls for a plan that describes the system boundary, the environment of operation, how each security requirement is implemented, and the relationships with or connections to other systems, and NIST SP 800-171A tests those descriptions through eight objectives, 3.12.4[a] through [h]. DFARS 252.204-7020 defines a government assessment as verification of the SSP "to validate that NIST SP 800-171 security requirements have been implemented as described in the contractor's system security plan." A plan that describes controls the contractor does not have is a false description of its own system, and since June 18, 2026, the Justice Department has a $507,144 example of what that costs with no breach involved.**

<div class="key-takeaways" style="border-left:4px solid #EE4C48;background:#15151a;padding:18px 24px;margin:28px 0;border-radius:6px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;">
<li>No rule bans AI drafting. Requirement 3.12.4 and the eight NIST SP 800-171A objectives regulate what the SSP says, not what wrote it. Objectives [b], [c], [e] and [f] are facts about one specific system; a model that never inspected it can imitate them, not supply them.</li>
<li>The SSP is the statement the government tests. DFARS 252.204-7020, now 252.240-7997 under the September 3 class deviation, defines a government assessment as validation that the requirements "have been implemented as described in the contractor's system security plan."</li>
<li>LOGZONE self-reported 110 in October 2021. DCMA assessed it at -170 on February 2, 2024. DOJ settled for $507,144 on June 18, 2026, with no breach and no whistleblower. The gap between the description and the network was the whole case.</li>
<li>AI drafts fail in three predictable ways: controls you do not have described as implemented, a boundary that belongs to a different company, and statements that contradict your own POA&M and SPRS score. All three are what a reviewer cross-reads first.</li>
<li>The second exposure is the input. A specific SSP needs your network diagram, IP ranges, admin accounts and vendor list. Into a consumer AI tool, that is a disclosure you cannot retrieve, and if contract numbers or CUI went in with it, Brilliant at the Basics item 8 was broken to write the compliance document.</li>
<li>This month: let the model build structure only, put a named artifact behind every "implemented," keep system specifics out of public tools, reconcile SSP, POA&M and SPRS score, and have the affirming official sign only what the evidence shows.</li>
</ul>
</div>

## The pitch: a DIBCAC-ready SSP in minutes

The market arrived before the rule did. An AWS Marketplace listing from a cloud consultancy advertises SSP and POA&M artifacts "generated and managed via our AI-based Documentation Management Tool." A registered practitioner organization sells an SSP generator under the headline "Create DIBCAC-Ready SSPs in Minutes." A managed service provider published a tiered policy in June 2026 giving AI drafting of SSP sections a green light for framework content. None of them are breaking a rule, because there is no rule about who or what writes the plan.

Two things make the pitch land harder this year than in 2024.

First, verification moved. Since the [September 3 class deviation]({% post_url 2026-09-10-cmmc-phase-2-class-deviation %}) stripped third-party assessment requirements out of contracts, self-assessment is the codified default for CUI work. The Cyber AB reported 2,362 final Level 2 certificates at its September 30 town hall. Everyone else handling CUI describes their own system to the government in their own words, and no outside reader opens the document until a government assessment or a complaint. That lowers the perceived cost of a weak SSP and raises the real one.

Second, the ecosystem itself is leaning toward machine-written compliance. The same town hall had the Cyber AB's leadership speculating, with every slide labeled speculative, about compliance-as-code, configuration baselines in OSCAL, and continuous monitoring in place of point-in-time review. On October 15 the CyberEF runs an ecosystem-wide session on AI and the future of CMMC. "Do not use AI" is not where the program is heading. The useful question is narrower: which parts of an SSP can a model produce, and which can only come from the building.

## What 3.12.4 asks the SSP to be

Requirement 3.12.4 in NIST SP 800-171 Rev 2 is one sentence. Develop, document, and periodically update system security plans that describe system boundaries, system environments of operation, how security requirements are implemented, and the relationships with or connections to other systems. NIST SP 800-171A turns that sentence into eight determination statements:

- **3.12.4[a]** a system security plan is developed.
- **3.12.4[b]** the system boundary is described and documented in the plan.
- **3.12.4[c]** the system environment of operation is described and documented in the plan.
- **3.12.4[d]** the security requirements identified and approved by the designated authority as non-applicable are identified.
- **3.12.4[e]** the method of security requirement implementation is described and documented in the plan.
- **3.12.4[f]** the relationship with or connection to other systems is described and documented in the plan.
- **3.12.4[g]** the frequency to update the plan is defined.
- **3.12.4[h]** the plan is updated with the defined frequency.

Read those as a list of what a language model can and cannot do. It can satisfy [a], [g] and the format of everything else in seconds. Objectives [b], [c], [d], [e] and [f] are facts about one specific system: where the boundary falls, what runs inside it, which requirements a named official decided do not apply, how each of the 110 is met, and what the system connects to. A model that has never seen your network produces plausible text for each. It cannot produce the fact, because the fact is not in its training data or your questionnaire. It is in your firewall, your identity provider and your vendor contracts.

![What NIST SP 800-171A objectives 3.12.4[b], [d], [e] and [f] ask the SSP to state, and where an AI draft goes wrong on each](/blog/images/2-ai-ssp-what-800-171a-tests-table.png)

The surrounding rules close the exits. Under the DoD Assessment Methodology, 3.12.4 carries no point value, and the absence of an SSP means the assessment cannot be completed. 32 CFR 170.24(c)(2)(i)(B)(5) requires the plan to be up to date at assessment, 170.24(b)(1) rejects drafts and working papers as evidence, and 170.21(a)(2)(iii) bars CA.L2-3.12.4 from any POA&M. The [SSP update requirements breakdown]({% post_url 2026-09-17-cmmc-ssp-update-requirements %}) walks through those provisions. The SSP is the one document you cannot defer, cannot leave in draft, and cannot be assessed without.

## Three ways an AI-written SSP fails when someone checks it

**It describes controls you do not have.** The model's default output is the fluent "implemented" paragraph. Multi-factor authentication is enforced for all users. Audit logs are collected, reviewed and retained. Those sentences are true for the system the model imagined and may be false for yours. Your SPRS score is derived from the SSP under the Assessment Methodology's one, three and five point weights, so a paragraph that says 3.5.3 is implemented when it is not is five points of distance between the number you posted and the number an assessor would post. LOGZONE is that distance at scale. The company self-reported a perfect 110 in October 2021. The Defense Contract Management Agency assessed the same environment on February 2, 2024 and scored it -170, near the floor of -203. On June 18, 2026 the company paid $507,144 to resolve False Claims Act allegations covering invoices from May 2021 to March 2025. No breach, no whistleblower; the government found the gap itself. On September 1, Honeywell Aerospace paid $2,042,518 over NIST SP 800-171 gaps on a single network, in a case brought by a former employee; the [Honeywell breakdown]({% post_url 2026-09-02-honeywell-fca-cybersecurity-settlement %}) covers the mechanics. Both cases ran on the difference between what the contractor said about its controls and what was true.

**It describes a system that is not yours.** An assessor, including you during a self-assessment, reads three documents against each other: the SSP boundary and environment sections, the network diagram, and the asset inventory sorted into the five categories in 32 CFR 170.19. A model fed a questionnaire tends to produce a generic enclave: one flat network, an MFA vendor you never bought, a cloud provider that appears on no invoice, and no mention of the managed service provider that actually holds your admin credentials. 32 CFR 170.16(c)(2)(iii) and (c)(3)(i) require cloud and external service providers to be documented in the SSP; the [external service provider post]({% post_url 2026-07-12-cmmc-external-service-provider-requirements %}) covers what that has to say. An SSP that omits the MSP is a boundary description that fails 3.12.4[b] and [f] on its face.

**It contradicts the rest of your record.** The SSP does not stand alone. The POA&M lists what is open, the SPRS score is the arithmetic of what is met, and the annual affirmation under 32 CFR 170.22 is a named official's signature over the whole package. When a model drafts the SSP after the POA&M was written, the two disagree: the POA&M says 3.13.11 FIPS-validated cryptography is open, the SSP says it is implemented, and the score could be either. Inconsistency is the first thread a reviewer pulls. It is also what a relator screenshots. The $4.6 million MORSECORP case of March 26, 2025 was brought by the company's own head of security, who collected 18.5 percent. The people who can prove an SSP is fiction are usually the people who were asked to make it true.

![Three ways an AI-generated SSP fails under review: controls you do not have described as implemented, a boundary that belongs to a different company, and statements that contradict the POA&M and SPRS score](/blog/images/3-ai-ssp-three-ways-it-fails-when-checked.png)

## The second exposure: what you pasted in to get the draft

A generic SSP is useless, so the sales pitch is specificity, and specificity comes from you. To get a plan that names your systems, you feed the tool your network diagram, IP ranges, firewall rule set, administrator account names, vendor list, contract numbers and, usually, an honest list of the gaps. That bundle is the roadmap to the environment holding CUI. If a sample of the CUI or the program names went in to help the model understand the data flow, the bundle is CUI.

Where it went matters. Consumer AI tools retain prompts, and personal tiers of the major products may use conversations to improve models unless the account opts out; OpenAI, for example, states that it does not train on ChatGPT Team, Enterprise or API data by default, while a personal account has to turn training off. The vendor's data-use page is the control, and most people who paste a diagram into a chat window have not read it. The DoW CIO's Brilliant at the Basics item 8, covered in [yesterday's post on the two AI rules]({% post_url 2026-10-06-ndaa-section-1532-ai-rules-defense-contractors %}), tells DIB partners to "explicitly prohibit the input of sensitive Department data into public, commercial AI systems." Contract numbers, CUI categories and program references are sensitive Department data. A contractor that used a consumer tool to write its CMMC documentation may have broken the Department's stated expectation to produce the document that claims it meets them. If the tool runs a DeepSeek-derived model, the drafting is arguably contract performance under NDAA Section 1532 as well.

Inside NIST SP 800-171, the relevant requirements are 3.1.3, control the flow of CUI, and 3.1.20, verify and control connections to external systems. An AI drafting session that received system details is an undocumented external connection, which is its own 3.12.4[f] problem.

## Who compares the plan to the network

Three readers eventually do.

The first is you. DFARS 252.204-7020 defines the Basic assessment as one that "is based on the Contractor's review of their system security plan(s)." The SPRS score is the output of that review. If the plan is wrong, the score is wrong, and the [wrong SPRS score post]({% post_url 2026-09-14-sprs-score-wrong-self-disclosure %}) covers the disclosure clock that starts when you find out.

The second is DIBCAC. The same clause defines a Medium or High assessment as "verification, examination, and demonstration of a Contractor's system security plan to validate that NIST SP 800-171 security requirements have been implemented as described in the contractor's system security plan." The deviation renumbered the clause to 252.240-7997 and kept government-led assessment; the [DIBCAC preparation post]({% post_url 2026-07-26-dibcac-assessment-preparation %}) describes how that review runs. The assessor audits your network against your own description of it. Every fluent "implemented" the model wrote is a claim you have invited the government to test.

The third is the Justice Department, which assesses nothing. It takes the assessor's score, the SSP, the SPRS submission and the affirmation, puts them next to the invoices submitted while those statements were on file, and applies 31 U.S.C. 3729. That is the LOGZONE record: a document in 2021, a government score in 2024, a settlement in 2026 covering every claim in between.

## How to use AI on an SSP without creating a false statement

None of this says do not use the tool. It says know which half of the document it can write.

1. **Structure only, never the facts.** Let the model produce the skeleton: section headings, the 110 requirement texts, the 320 objective list, a consistent format for each implementation statement, the revision history table. That is framework content and contains nothing about you.
2. **Every "implemented" points to a named artifact.** A human writes or verifies each implementation statement and records what supports it: a configuration export, a dated screenshot, an approved policy, a log sample. If no artifact exists, the objective is NOT MET, it goes on the POA&M if 32 CFR 170.21 allows it, and the score drops by the control's weight. The [evidence checklist]({% post_url 2026-06-12-cmmc-evidence-checklist-c3pao %}) lists what counts for each method.
3. **Keep the specifics out of public tools.** If system details must go into a model, use a tenant whose terms exclude training and retention, inside a boundary you control, and document the decision as an external connection under 3.1.20. If you cannot meet that bar, the details stay out.
4. **Record provenance.** Keep a drafting log: which sections were model-generated, who reviewed each one, and when. Remove "draft" from the header only after that review, because 170.24(b)(1) will not accept a working paper.
5. **Reconcile the three documents.** SSP against POA&M against SPRS score, then boundary against network diagram against asset inventory. If the model's draft changed any statement, recompute the score from the corrected SSP using the 170.24 point values.
6. **Sign only what you can show.** The affirming official under 32 CFR 170.22 signs for the package and should be able to open any implementation statement and reach its artifact in minutes. If the only person who can do that is the IT contractor, the signature is a trust exercise, and the [affirming official post]({% post_url 2026-06-18-cmmc-affirming-official-personal-liability %}) explains whose name it is in.

![Six rules for using AI on a CMMC SSP without creating a false statement: structure only, named artifacts, no specifics in public tools, provenance log, three-document reconciliation, and an affirming official who can reach the evidence](/blog/images/4-ai-ssp-safe-use-six-rules.png)

## What a 12-person shop does this month

- **Find out who wrote each section and from what.** Ask whoever delivered the SSP, staff, MSP or consultant, which parts came out of a model and what was pasted in to get them. Write the answer down.
- **Run the ten-minute test on ten statements.** Pick ten "implemented" sentences at random. For each, find the artifact in under ten minutes. Every miss is a NOT MET you are currently affirming as met.
- **Lay the three boundary documents side by side.** SSP boundary and environment sections, network diagram, asset inventory in 170.19 categories. Every system on the diagram appears in the SSP; every provider in the SSP appears on an invoice.
- **Check the inputs.** If network details or contract data went into a consumer AI account, treat it as an undocumented external connection: record it, close it, change the practice.
- **Fix the number.** If the ten-minute test moved any control to NOT MET, recompute the score and decide the disclosure question on the 30-day timeline the September 14 post lays out.

If your SSP started as a generated draft and you are rebuilding the implementation statements by hand, the [CMMC Level 2 System Security Plan (SSP) Template](https://payhip.com/b/gB6oD) ($77) is structured around all 110 requirements and their 800-171A objectives, with an evidence reference on each statement so "implemented" cannot be written without naming what proves it. The [CMMC Level 2 Evidence Tracker for NIST 800-171 Audit](https://payhip.com/b/LN2UB) ($67) is the ten-minute test as a workbook, mapping each objective to its examine, interview and test artifacts. If you are running the full reconciliation before an affirmation, with a government assessment or a prime's compliance letter already on the calendar, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) bundles the SSP template, evidence tracker, SPRS score workbook, POA&M tracker and asset scoping worksheet so the three documents are built from one set of facts. It is what a small contractor uses to make the number, the plan and the signature say the same thing.

## The bottom line

A model can write a System Security Plan that reads better than yours. It cannot write one that is true, because the truth of an SSP is not a writing problem. It is the contents of your firewall, your identity provider and your vendor contracts, described accurately. NIST SP 800-171A tests those descriptions objective by objective, DFARS 252.204-7020 defines the government's audit as a check against your own words, and the LOGZONE record shows the Justice Department treating the gap between description and network as a false claim with no breach required. Use the tool for the skeleton. Put a human and an artifact behind every sentence that makes a claim. And do not hand a public chatbot the map of the building to get there.

## Sources

- NIST SP 800-171 Rev 2, requirement 3.12.4; NIST SP 800-171A, assessment objectives 3.12.4[a] through [h]; NIST SP 800-171 requirements 3.1.3, 3.1.20, 3.5.3, 3.13.11
- DFARS 252.204-7020, NIST SP 800-171 DoD Assessment Requirements (Nov 2023), paragraphs defining Basic, Medium and High assessments; DARS class deviation 2026-O0025 Revision 3 (September 3, 2026), renumbering to 252.240-7997
- DoD, NIST SP 800-171 DoD Assessment Methodology, Version 1.2.1 (scoring weights, the -203 floor, treatment of 3.12.4)
- 32 CFR 170.16(c)(2)(iii) and (c)(3)(i), 170.19, 170.21(a)(2)(iii), 170.22, 170.24(b)(1) and (c)(2)(i)(B)(5)
- U.S. Department of Justice, "Alabama Defense Contractor to Pay $507,144 to Resolve False Claims Act Cybersecurity Allegations," June 18, 2026 (LOGZONE Inc.; self-assessment of 110 in October 2021; DCMA assessment of -170 dated February 2, 2024; claims May 2021 to March 2025; $253,572 restitution)
- U.S. Department of Justice, Honeywell Aerospace Inc. settlement, September 1, 2026 ($2,042,518; April 2020 to December 2023; one network; qui tam by a former employee; United States intervened August 18, 2026)
- U.S. Department of Justice, MORSECORP Inc. settlement, March 26, 2025 ($4.6 million; relator the company's head of security and facility security officer, 18.5 percent share)
- Cyber AB Town Hall, September 30, 2026, as recapped by CMMC.com (2,362 final Level 2 certificates; 117 authorized or accredited C3PAOs; speculative discussion of compliance-as-code and OSCAL; CyberEF session on AI and the future of CMMC, October 15, 2026)
- Department of War CIO, "Brilliant at the Basics," IT Top 10, item 8, July 13, 2026; National Defense Authorization Act for Fiscal Year 2026, Public Law 119-60, Section 1532
- OpenAI, Enterprise privacy and consumer data controls pages (training defaults by product tier)
- AWS Marketplace, Asante Cloud, "Asante AI CMMC Gap Analysis and Readiness Services" listing; Petronella Technology Group, ComplianceArmor "System Security Plan Generator" page; VSO, "Using AI for CMMC Evidence Collection: What's Safe, What's Not," June 2026
- 31 U.S.C. 3729, False Claims Act
