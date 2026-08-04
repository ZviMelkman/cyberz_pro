---
layout: post
title: "Can You Use ChatGPT With CUI? What DFARS and CMMC Actually Require in 2026"
date: 2026-08-04
description: "The CMMC Phase 2 suspension did not touch DFARS 252.204-7012. What the cloud clause requires of AI tools, which services qualify, and what to do when CUI lands in a chatbot."
category: AI Security
tags: [CUI, ChatGPT, AI security, DFARS 252.204-7012, FedRAMP, CMMC, NIST 800-171, defense contractor, Copilot, AI governance]
image: /blog/images/1-ai-tools-cui-compliance-hero.png
author: CyberZ
---

*Every CMMC deadline is suspended. The rule that governs whether your team can put CUI into an AI tool is not one of them.*

**No. Controlled Unclassified Information cannot be placed into consumer ChatGPT, a commercial ChatGPT Enterprise tenant, commercial-tenant Microsoft 365 Copilot, or Gemini on a commercial tenant. DFARS 252.204-7012(b)(2)(ii)(D) requires that any external cloud service used to store, process, or transmit covered defense information meet security requirements equivalent to the FedRAMP Moderate baseline, and that the provider also comply with paragraphs (c) through (g) of the clause. A handful of AI services do meet that bar, but only in specific government offerings, and only when the use is documented in your system security plan.**

<div class="key-takeaways" style="background:#16161a;border-left:4px solid #EE4C48;padding:20px 24px;margin:24px 0;">
<strong>Key Takeaways</strong>
<ul>
<li>The July 13, 2026 suspension paused CMMC Phase 2 and all future program milestones. It left DFARS 252.204-7012, NIST SP 800-171 Revision 2, SPRS scores, and 72-hour incident reporting fully in force.</li>
<li>The governing text is DFARS 252.204-7012(b)(2)(ii)(D). It covers any external cloud service that stores, processes, or transmits covered defense information, which includes a chat window.</li>
<li>"FedRAMP Authorized" is not a single status. 32 CFR 170.17(c)(5)(i) points at the FedRAMP Marketplace by name, and the impact level on the record is what decides whether the service can hold CUI.</li>
<li>Microsoft's own documentation states that Microsoft 365 Copilot is not certified as compliant with CMMC Level 2 or NIST SP 800-171. Copilot for GCC High is a separate offering with a separate answer.</li>
<li>Pasting CUI into an unauthorized tool is a cyber incident, not a policy violation. Paragraph (c) sets a 72-hour reporting clock and paragraph (e) requires you to preserve the evidence rather than delete it.</li>
<li>FY2026 NDAA Section 1513 directs DoD to build an AI and machine learning security framework as an extension of CMMC and fold it into the DFARS. The Phase 2 pause came from a memo. Section 1513 is statute.</li>
</ul>
</div>

![Table comparing seven AI services against what FedRAMP authorization each actually holds and whether it can process CUI under DFARS 252.204-7012](/blog/images/2-ai-tools-cui-authorization-status.png)

## Did the CMMC Phase 2 suspension change the rules for AI tools?

It did not, and the gap between what contractors think changed and what actually changed is where the risk now lives.

On July 13, 2026, the DoD Chief Information Officer suspended the transition to CMMC Phase 2, along with all pending and future program milestones, and stood up a 60-day CMMC Reform Task Force. The Department was explicit that suspending Phase 2 does not eliminate the requirement to protect federal data. Phase 1 self-assessments remain. DFARS 252.204-7012 remains. NIST SP 800-171 Revision 2 remains the enforced standard during the interim, through self-assessments and select government-led assessments. SPRS submissions and the 72-hour incident reporting duty are untouched.

That matters here because the AI question was never a CMMC question in the first place. It is a 7012 question. Suspending the certification schedule does nothing to the clause that decides whether a cloud service is allowed to hold your CUI. If your contract contains 7012, and it almost certainly does if you handle covered defense information, the analysis below applies today with the same force it had on July 12.

For the broader picture on what survived the suspension, see our breakdown of [whether CMMC is still required]({% post_url 2026-07-19-is-cmmc-still-required %}) and the [RFI response window closing August 14]({% post_url 2026-08-02-cmmc-reform-task-force-rfi-response %}).

## What does DFARS 252.204-7012 require of a cloud service that touches CUI?

The operative sentence sits in paragraph (b)(2)(ii)(D). If a contractor intends to use an external cloud service provider to store, process, or transmit any covered defense information, the contractor shall require and ensure that the provider meets security requirements equivalent to those established for the FedRAMP Moderate baseline, and that the provider complies with paragraphs (c) through (g) for cyber incident reporting, malicious software, media preservation and protection, access to additional information and equipment necessary for forensic analysis, and cyber incident damage assessment.

Two halves, and most coverage only reads the first one.

The first half is the security bar: FedRAMP Moderate or a documented equivalent. The second half is a contractual obligation you owe, not the vendor. You have to "require and ensure" that the provider will report incidents, preserve media, and hand over systems and information for forensic analysis if something goes wrong. That is a term in an agreement. A consumer subscription paid on a credit card does not contain it, and no amount of configuration adds it.

This is also why "we turned off model training" is not an answer. Training opt-out addresses one risk. It does not create FedRAMP equivalency, and it does not bind the provider to paragraph (e) preservation duties.

## What does FedRAMP Moderate equivalent actually mean?

Before December 2023, "equivalent" was doing a lot of work in vendor marketing. A DoD CIO memorandum dated December 21, 2023, titled Federal Risk and Authorization Management Program Moderate Equivalency for Cloud Service Provider's Cloud Service Offerings, ended that.

Under the memo, a cloud service offering is FedRAMP Moderate equivalent only if it achieves 100 percent compliance with the FedRAMP Moderate baseline, assessed by a FedRAMP-recognized third-party assessment organization, and documented in a body of evidence. A SOC 2 Type 2 report does not satisfy it. An ISO 27001 certificate does not satisfy it. A vendor security whitepaper claiming alignment with NIST 800-53 does not satisfy it. Neither does a trust-center page.

There are two clean paths, then. Either the offering holds a FedRAMP authorization at Moderate or higher, which you verify on the FedRAMP Marketplace, or the provider hands you a 3PAO-validated body of evidence. If a vendor cannot produce one of those two things on request, you have your answer, and you have it in writing, which is worth something later.

The CMMC rule points at the same place. 32 CFR 170.17(c)(5) permits an organization seeking certification to use a cloud environment for CUI where the provider's offering is FedRAMP Authorized at Moderate or higher in accordance with the FedRAMP Marketplace, or where it meets equivalent requirements in accordance with DoD policy. Our post on [external service provider requirements]({% post_url 2026-07-12-cmmc-external-service-provider-requirements %}) walks through the CSP and ESP distinction in more detail.

![Five sequential gates an AI tool must clear before it can process CUI, from CUI handling through FedRAMP status, body of evidence, clause flow-down, and SSP documentation](/blog/images/3-ai-tools-cui-decision-flow.png)

## Which AI services can hold CUI, and which cannot?

Authorization attaches to a specific service offering, in a specific environment, sometimes down to specific features. The brand name on the login page tells you very little. Two examples make the point.

OpenAI's ChatGPT Enterprise and API Platform appear on the FedRAMP Marketplace under package ID FR2533155773, FedRAMP Certified, Type 20x, Path Program, Class C (Moderate), certified as of January 9, 2026. That is a real authorization at the level 7012 asks for. It is also not the product most people mean when they say "we have ChatGPT Enterprise." The authorized offering is the FedRAMP build, which routes API traffic through a designated government endpoint and ships with a reduced feature set. Your commercial tenant is a different service, and it is not covered by that record.

Microsoft is the mirror image. Microsoft's own guidance states plainly that Microsoft 365 Copilot is not certified as compliant with CMMC Level 2 or NIST SP 800-171. Microsoft 365 Copilot became available in GCC High in December 2025, built for the FedRAMP High, DFARS, and ITAR boundary, and that is a different answer to a different question. A license in a commercial tenant is not a boundary, and the presence of Copilot in your tenant does not migrate your data anywhere.

Azure OpenAI Service in Azure Government carries FedRAMP High plus DoD Impact Level 4 and 5. Amazon Bedrock in AWS GovCloud carries the GovCloud FedRAMP High authorization, which is currently the only route to using Claude models against regulated federal data, with the caveat that model availability in GovCloud lags the commercial regions. Gemini and the rest of the commercial-tenant assistants carry nothing that meets the clause.

One more caution worth stating clearly. FedRAMP's AI Prioritization Initiative, which began in August 2025, was completed in April 2026 and is closed to new entrants. The set of authorized AI services is not going to expand as quickly as vendor roadmaps imply. Check the Marketplace record for the exact offering, note the impact level and the date, and re-check it before each assessment.

## Is pasting CUI into a chatbot a spillage event?

Yes, and treating it as an HR matter instead of an incident is the more expensive mistake.

When CUI enters a system that is not authorized to hold it, the data has moved outside the boundary described in your system security plan. That is a cyber incident under the clause, and paragraph (c) requires a rapid report to DoD within 72 hours of discovery through the DoD reporting portal. Paragraph (e) requires you to preserve and protect images of known affected information systems and relevant monitoring data for at least 90 days from the report. Paragraphs (f) and (g) cover access for forensic analysis and the damage assessment.

The instinct in the room is always to delete the conversation. Do not. Deletion does not un-transmit the data, it destroys the record you are obligated to preserve, and it converts a reportable incident into a much harder conversation about spoliation. Revoke the account, preserve what you have, and report.

![Five-step response sequence after CUI enters an unauthorized AI tool: contain, preserve, report within 72 hours, support damage assessment, document](/blog/images/5-ai-tools-cui-spillage-response.png)

## Which NIST SP 800-171 requirements govern AI tool use?

NIST SP 800-171 Revision 2 never mentions artificial intelligence. It does not need to, because four of its requirements already reach the behavior.

Requirement 3.1.3 requires you to control the flow of CUI in accordance with approved authorizations. A paste into a chat window is a flow of CUI to an external system. Either the flow is authorized and documented or it is neither.

Requirement 3.1.20 requires you to verify and control or limit connections to and use of external systems. This is the requirement practitioners in the CMMC community consistently land on for AI tools, and it is the correct one. It is also the one an assessor will use to ask how you know what your people are connecting to.

Requirement 3.4.9 requires you to control and monitor user-installed software. Browser extensions, desktop assistants, and IDE plugins are user-installed software with network egress, and they are the most common way an unapproved AI tool arrives inside a scoped environment.

Requirement 3.12.4 requires a system security plan that describes system boundaries and environments of operation. An AI tool absent from the SSP is not out of scope. It is undocumented, which is worse.

![The four NIST SP 800-171 Revision 2 requirements that already govern AI tool use: 3.1.3, 3.1.20, 3.4.9, and 3.12.4](/blog/images/4-ai-tools-cui-nist-800-171-controls.png)

Documenting an approved tool list, the data classes each tool may touch, and the request path for new tools is what turns those four requirements into something you can show. The [AI Acceptable Use Policy Kit](https://payhip.com/b/AKSw2) ($47) contains the policy, the approved-tools register, and the incident-reporting language, written so a 20-person shop can adopt it in one working session. Our post on [what an AI acceptable use policy needs]({% post_url 2026-07-07-ai-acceptable-use-policy-small-business %}) covers the structure at no cost.

## Is encrypted CUI still CUI?

Yes. Encryption changes who can read the data. It does not change what the data is, who is responsible for it, or which systems are authorized to process it. FIPS-validated cryptography is itself a 800-171 requirement rather than an exemption from the rest of them.

The related trap is a vector store. Embeddings, cached context, chat history, and retrieval indexes derived from CUI are still derived from CUI, and they persist inside whichever environment generated them. If a tool builds a searchable index of documents you fed it, that index lives inside your boundary or it does not, and the answer needs to be in your SSP either way. Scoping the AI tool as an asset is the practical first step, which is what the [CMMC Level 2 Asset Scoping Worksheet for NIST 800-171](https://payhip.com/b/2nzjO) ($47) is built to do.

## What does FY2026 NDAA Section 1513 change?

This is the part worth reading if you are tempted to treat the suspension as permission to stop.

The FY2026 National Defense Authorization Act, Public Law 119-60, includes Section 1513, "Physical and Cybersecurity Procurement Requirements for Artificial Intelligence Systems." It directs the Department of Defense to develop a security framework for AI and machine learning systems it acquires, built on the NIST SP 800 series, and implemented as an extension or augmentation of existing DoD cybersecurity frameworks, naming CMMC directly. It further directs DoD to incorporate the framework into the DFARS and into CMMC, so that contractors developing, deploying, storing, or hosting AI or machine learning for DoD must comply. Covered technology is defined broadly enough to include source code, model weights, training data, and algorithms.

Section 1513 sets no implementation deadline. It required a status update to Congress by June 16, 2026, and directs DoD to produce a plan with timelines and milestones. CMMC itself began as a provision in the FY2020 NDAA and took years to arrive, so nobody should expect this next year.

The point is directional. Phase 2 was suspended by a memorandum, and a memorandum can be reversed as quickly as it was issued. Section 1513 is a statutory instruction that points AI security requirements back into the same CMMC and DFARS machinery. Contractors building AI governance now are building the thing Congress has already told the Department to require.

## What should a small contractor do this week?

Five things, in order, none of which requires a consultant.

Inventory what is actually in use. Not the approved list, the real one. Check browser extensions, check the identity provider for OAuth grants to AI vendors, and check expense reports for individual AI subscriptions. Our post on [AI agent security risks]({% post_url 2026-07-02-ai-agent-security-risks-small-business %}) covers where these connections hide.

Ask one question of each tool that touches company data: which exact offering are we on, and does it appear on the FedRAMP Marketplace at Moderate or higher? Write the answer down with the date.

Draw the line in writing. One page naming approved tools, the data classes each may touch, and what happens when someone gets it wrong. A rule nobody has read is not a control.

Put the answer in the SSP. Name the service, the environment, the customer responsibility matrix, and the boundary. The [CMMC Level 2 System Security Plan (SSP) Template](https://payhip.com/b/gB6oD) ($77) has the external-services and boundary sections structured the way an assessor reads them.

Decide the incident path before you need it. Who declares, who preserves, who reports within 72 hours. Practice it once. The [nine-item evidence discipline for self-assessments]({% post_url 2026-07-22-nist-800-171-self-assessment-evidence %}) applies here too.

If you are standing up the whole documentation set rather than patching one gap, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) bundles the scoping worksheet, SSP template, SPRS workbook, evidence tracker, and POA&M tracker. It is the right purchase when an assessment or a prime's documentation request is on the calendar and you need the artifacts to line up with each other.

## The Bottom Line

The suspension bought the Defense Industrial Base time on certification. It bought nobody anything on the cloud clause, because the cloud clause was never part of the phased schedule.

Meanwhile the tools got better and the temptation got stronger. The gap between a contractor who can name the exact authorized offering their team uses and a contractor who assumes the enterprise license covers it is not a technical gap. It is a documentation gap, and documentation gaps are precisely what the Civil Cyber-Fraud Initiative has spent three years converting into settlements.

Nothing about that changed on July 13.

## Sources

- DFARS 252.204-7012, Safeguarding Covered Defense Information and Cyber Incident Reporting, paragraphs (b)(2)(ii)(D) and (c) through (g) — acquisition.gov
- Memorandum, "Federal Risk and Authorization Management Program (FedRAMP) Moderate Equivalency for Cloud Service Provider's (CSP) Cloud Service Offerings (CSO)," December 21, 2023 — dodcio.defense.gov
- CMMC Program Final Rule, 32 CFR 170.16, 170.17(c)(5), and 170.19(c)(2) — ecfr.gov
- FedRAMP Marketplace, ChatGPT Enterprise and API Platform, package FR2533155773, OpenAI — fedramp.gov
- FedRAMP AI Prioritization Initiative status — fedramp.gov
- Microsoft Learn, "Evaluating Microsoft Copilot Compliance with NIST SP 800-171 and CMMC Level 2" — learn.microsoft.com
- Microsoft Community Hub, "Microsoft 365 Copilot is now available in GCC High," December 1, 2025 — techcommunity.microsoft.com
- Azure Government, Azure OpenAI Service FedRAMP High and DoD IL4/IL5 authorization — devblogs.microsoft.com
- National Defense Authorization Act for Fiscal Year 2026, Public Law 119-60, Section 1513 — congress.gov
- Congressional Research Service, "Cyber and Artificial Intelligence Provisions in the FY2026 National Defense Authorization Act," IF13197 — congress.gov
- Memorandum, "Implementing the Suspension of the Advancement to CMMC Phase 2 Requirements," July 13, 2026 — dodcio.defense.gov
- NIST SP 800-171 Revision 2, requirements 3.1.3, 3.1.20, 3.4.9, and 3.12.4 — csrc.nist.gov
