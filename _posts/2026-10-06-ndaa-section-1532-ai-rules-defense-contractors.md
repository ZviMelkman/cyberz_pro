---
layout: post
title: "NDAA Section 1532 and Brilliant at the Basics: The Two AI Rules Already Binding a Defense Contractor That NIST 800-171 Never Mentions"
date: 2026-10-06
description: "Since January 17, 2026, Section 1532 of the FY2026 NDAA has barred any DoD contractor from using AI developed by DeepSeek or High Flyer in contract performance. DeepSeek-V4 is sold inside Microsoft Foundry and DeepSeek-R1 inside Amazon Bedrock. Separately, the DoW CIO's Brilliant at the Basics Top 10 tells DIB partners to write an AI policy and ban sensitive data from public AI. NIST SP 800-171 Rev 2 has no AI requirement at all. What both rules say, where the banned models hide, and what a small subcontractor does this month."
category: CMMC
tags: [CMMC, NDAA Section 1532, DeepSeek, Brilliant at the Basics, AI policy, AI acceptable use policy, NIST 800-171, DFARS 252.204-7012, Microsoft Foundry, Amazon Bedrock, CUI, defense contractors]
image: /blog/images/1-ndaa-section-1532-ai-rules-hero.png
author: CyberZ
---

*The CMMC Reform Task Force report is still weeks away, and the DIB is waiting to see what the reform says about AI. Two AI rules are not waiting. One has been federal law since January 17. The other is item 8 on the Department's own Top 10 list, the list the reform is widely expected to be built around. Neither one appears anywhere in the 110 controls your SSP describes.*

**Section 1532 of the National Defense Authorization Act for Fiscal Year 2026 (Public Law 119-60, enacted December 18, 2025) prohibits any contractor, during the period of performance of a contract with the Department of Defense, from using "covered artificial intelligence" with respect to the performance of that contract. Covered AI means any AI, or successor AI, developed by the Chinese company DeepSeek, or by High Flyer or an entity High Flyer owns, funds, supports, or holds at least a 20 percent stake in. The prohibition took effect 30 days after enactment, on January 17, 2026, and it operates through the statute itself, not through a DFARS clause. Separately, the Department of War CIO's "Brilliant at the Basics" IT Top 10, published alongside the July 13, 2026 CMMC Phase 2 pause, directs DIB partners to establish AI policies and technical guardrails and to explicitly prohibit the input of sensitive Department data into public, commercial AI systems. NIST SP 800-171 Revision 2, the standard behind CMMC Level 2 and DFARS 252.204-7012, contains no AI-specific requirement.**

<div class="key-takeaways" style="border-left:4px solid #EE4C48;background:#15151a;padding:18px 24px;margin:28px 0;border-radius:6px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;">
<li>Section 1532(a)(3)(A) bans DeepSeek and High Flyer AI from DoD contract performance. It has been in force since January 17, 2026, applies at every tier, and needs no contract clause to bite. The only exception is a case-by-case waiver signed by the Secretary of Defense for four narrow purposes.</li>
<li>The ban follows the developer, not the login page. DeepSeek-V4-Pro and V4-Flash are "Direct from Azure" models in Microsoft Foundry, billed through Azure and supported by Microsoft. DeepSeek-R1 has run fully managed in Amazon Bedrock since March 2025. Thousands of DeepSeek-derived models sit on Hugging Face and run locally in one command.</li>
<li>The broader ban on AI from companies in China, Russia, North Korea, or Iran, or on the Consolidated Screening List, only reaches contractors if the Secretary issues guidance under Section 1532(a)(2). As of October 6, 2026, no such guidance and no implementing DFARS text could be found.</li>
<li>Brilliant at the Basics item 8 asks for three things: a written AI policy with technical guardrails, an explicit prohibition on sensitive Department data in public commercial AI, and content filtering, endpoint controls, and an approved enterprise AI environment. The Cyber AB's CEO calls the Top 10 the clearest published statement of DoW priorities, and the reform is expected to lean on it.</li>
<li>NIST 800-171 Rev 2 has zero AI controls. Rev 3 does not add one. An SSP that scores 110 of 110 can be silent on both rules, and a developer using DeepSeek-V4 on a deliverable with no CUI in it is still inside the statute.</li>
<li>This month: inventory models rather than apps, block the known covered endpoints and model IDs at the boundary, put the three Brilliant at the Basics parts and a Section 1532 clause into your AI acceptable use policy, and anchor the policy in the SSP under 3.4.8, 3.4.9, and 3.1.20.</li>
</ul>
</div>

## Rule one: Section 1532 is a statute, and it has been in force since January 17

Most coverage of the FY2026 NDAA's AI provisions focused on Section 1513, which tells DoD to build a cybersecurity framework for AI and machine learning systems and fold it into the DFARS. That is a future obligation, and the [August 4 post on AI tools and CUI]({% post_url 2026-08-04-ai-tools-cui-compliance %}) covered it. Section 1532 is different in kind. It is already in effect, it names specific companies, and it reaches every contractor performing a DoD contract.

The operative text is short. Paragraph (a)(3)(A): except as provided in the waiver subsection, not later than 30 days after enactment, "no contractor may, during the period of performance of such contractor under a contract with the Department of Defense, use covered artificial intelligence with respect to the performance of a contract with the Department." Enactment was December 18, 2025. Day 30 was January 17, 2026.

"Covered artificial intelligence" is defined in (c)(2) as any AI, or successor AI, developed by the Chinese company DeepSeek, or developed by High Flyer or by an entity that High Flyer owns, funds, supports, or holds a direct or indirect stake of at least 20 percent in. High Flyer is the quantitative hedge fund that founded DeepSeek. That is the whole hard list. It is a company test, not a country test.

The statute also contains a second, wider tier that is easy to misread. Section 1532(a)(2) directs the Secretary to consider issuing guidance to remove from Department systems any AI from a "covered artificial intelligence company," defined in (c)(4) as a company on the Commerce Department's Consolidated Screening List or the 1260H Chinese military company list, domiciled in a covered nation (China, Russia, North Korea, or Iran under 10 U.S.C. 4872), or under unmitigated foreign ownership, control, or influence by one. Paragraph (a)(3)(B) then says contractors are barred from that wider set only "if the Secretary of Defense issues guidance described in paragraph (2)." Several law-firm summaries describe the contractor ban as already covering every covered-nation model. The text does not say that. The wider ban is conditional on guidance, and as of October 6, 2026, I could not find that guidance published, nor any DFARS clause or class deviation implementing Section 1532 at all. The DeepSeek and High Flyer ban does not need either. It applies on its own terms.

The waiver in subsection (b) belongs to the Secretary of Defense, case by case, for four purposes: scientifically valid research, evaluation or testing needed for national security, counterterrorism or operational military activity, and mission-critical functions. A prime cannot grant it. A contracting officer cannot grant it. A 15-person machine shop will not be applying for it.

## The ban follows the model, not the login page

The reflex response to "DeepSeek is banned" is to block deepseek.com and check that nobody installed the app. That handles the smallest part of the exposure.

DeepSeek publishes its models as open weights under an MIT license and leaves distribution to others. The result is that the models most likely to be inside a defense contractor's environment carry someone else's logo.

Microsoft Foundry lists DeepSeek-V4-Pro and DeepSeek-V4-Flash as "Direct from Azure" models with the model provider shown as DeepSeek. Microsoft's own description of that tier: purchased and managed through Azure with a single license, billed through your Azure subscription, covered by Azure service-level agreements, and supported by Microsoft. An engineer who deploys one of them from the Foundry catalog never visits a Chinese website and never sees a DeepSeek invoice. The developer of the model is still DeepSeek, which is the only thing Section 1532 asks.

Amazon Web Services has offered DeepSeek-R1 as a fully managed, serverless model in Amazon Bedrock since March 10, 2025, and R1 distilled variants through Bedrock Custom Model Import since January 2025. Hugging Face lists thousands of DeepSeek-based models, most of them community fine-tunes and distills. Ollama and similar tools pull a distilled DeepSeek model to a laptop in a single command, and Microsoft said in January 2025 that distilled R1 would run locally on Copilot+ PCs. Cheap tokens also mean that an unknown number of "AI writing assistant" and coding-assistant products route requests to a DeepSeek endpoint without saying so on the pricing page.

![Where DeepSeek-developed models run without a deepseek.com login: Microsoft Foundry sells DeepSeek-V4 as a Direct from Azure model, Amazon Bedrock has run DeepSeek-R1 fully managed since March 2025, Hugging Face and Ollama distribute open weights and thousands of distills, and third-party apps route to DeepSeek endpoints](/blog/images/3-section-1532-where-deepseek-models-run.png)

So the question for a contractor is not "does anyone here use DeepSeek?" It is "which models do our tools call?" Those are different inventories, and most small firms have only built the first one.

Two points of honest uncertainty. The statute does not define "developed by," and it says nothing about hosted copies, fine-tuned forks, or distillations, where a Llama or Qwen model has been trained on DeepSeek outputs. No DoD guidance I could find addresses any of that. Until one does, the only defensible position is to treat model lineage as the test, write down the decision, and keep DeepSeek-derived weights out of anything touching contract performance. Second, "with respect to the performance of a contract" is the trigger, not CUI. A developer who uses DeepSeek-V4 to draft code for a DoD deliverable that contains no CUI is inside the statute. That is a broader net than DFARS 252.204-7012 has ever cast.

## Rule two: the DoW CIO already told you what an AI policy must say

On July 13, 2026, the same day the Department paused CMMC Phase 2, the DoW CIO launched "Brilliant at the Basics," two Top 10 lists of cybersecurity practices for DIB partners, one for IT and one for operational technology. Item 8 on the IT list is titled "Secure AI Adoption and Data Protection." Its text, in full:

"Establish clear policies and technical guardrails governing the use of artificial intelligence and automation tools across your workforce. Explicitly prohibit the input of sensitive Department data into public, commercial AI systems. By implementing content filtering, endpoint controls, and approved enterprise AI environments, you prevent accidental data exposure while enabling the safe adoption of advanced technologies."

Read as a checklist, that is three deliverables. A written policy plus technical enforcement, not a policy alone. A specific, explicit prohibition on sensitive Department data in public commercial AI, which is wider than CUI and would catch Federal Contract Information and unmarked technical data. And a named set of controls: content filtering, endpoint controls, and an approved enterprise AI environment, which the [GCC High post]({% post_url 2026-09-23-do-i-need-gcc-high-for-cmmc %}) covered from the Microsoft side.

Brilliant at the Basics is not a regulation. The DoW CIO page carries a disclaimer saying the practices are educational and must be tailored to each organization's requirements. Nothing in it changes DFARS 7012, the 110 controls, or the SPRS posting. The reason it matters is what it signals.

At the Cyber AB's September 30 town hall, CEO Matthew Travis described Brilliant at the Basics as the clearest published statement of DoW cybersecurity priorities for the DIB, and said the task force's recommendations are now in the drafting and coordination stage, with public release in the back half of October at the earliest. At the Billington summit on September 9, CIO Kirsten Davies tied the reform directly to defending against attacks accelerated by frontier AI models. The CyberEF is running an ecosystem-wide session on AI and the future of CMMC on October 15. Whatever the reformed program measures, the Department has already published the list it is drawing from, and AI governance is item 8 on it.

A subcontractor writing its AI policy this month is therefore building to the list the reform is most likely to be graded against, before the grading rubric exists.

![Table comparing the two AI rules against NIST 800-171 Rev 2: NDAA Section 1532 has been law since January 17, 2026 and bans DeepSeek and High Flyer AI from DoD contract performance; Brilliant at the Basics item 8 was published by the DoW CIO on July 13, 2026 and asks for an AI policy, guardrails, and no sensitive data in public AI; NIST 800-171 Rev 2 is binding through DFARS 7012 and has no AI requirement in its 110 controls](/blog/images/2-section-1532-brilliant-basics-vs-nist-800-171-table.png)

## Why a perfect SSP does not catch either rule

NIST SP 800-171 Revision 2 was published in February 2020. None of its 110 requirements mention artificial intelligence, machine learning, or language models. Revision 3, published in May 2024, does not add one, and the [Rev 3 transition post]({% post_url 2026-07-08-nist-800-171-rev-3-cmmc-transition %}) explained why CMMC still assesses against Rev 2. At the September 30 town hall, Travis confirmed the program office's Rev 3 transition rule has been held in abeyance since July 13.

The nearest hooks in Rev 2 are indirect. 3.4.8 asks you to apply deny-by-exception or allow-by-exception policies for software. 3.4.9 asks you to control user-installed software. 3.1.20 asks you to verify and control connections to external systems. 3.1.3 asks you to control the flow of CUI. A contractor can satisfy all four with an allow-list that never names an AI model, because the controls were written for software packages and network connections, not for a model called through an API inside software you already approved. The [AI vendor due diligence post]({% post_url 2026-08-09-ai-vendor-due-diligence %}) covered that exact failure: approved software quietly adds an AI feature, and the SSP never changes.

The August 4 post made the DFARS 7012 case: CUI in an unauthorized cloud AI is a cloud-clause violation and a reportable incident. That remains true. Section 1532 and Brilliant at the Basics each reach further in a different direction. Section 1532 bites with no CUI involved at all. Brilliant at the Basics covers "sensitive Department data," a phrase the Department did not define and that a careful reader should assume includes FCI. An SSP can be complete and accurate against the 110 controls, score 110 in SPRS, and still have nothing to say about either.

## What a 15-person subcontractor does this month

1. **Inventory models, not apps.** List every AI product, IDE assistant, browser extension, chat tool, and API key in use, including the ones inside software you already approved. For each, record the model provider as the vendor's own documentation names it. A Foundry model card that says "Model provider: DeepSeek" answers the question regardless of what the invoice says.
2. **Block the known covered sources at the boundary.** The deepseek.com domain and the DeepSeek API endpoints on the firewall and DNS filter, the DeepSeek mobile app in your MDM, and the DeepSeek model IDs in your cloud governance: Azure Policy for Foundry, model access settings in Bedrock, and whatever your Google Cloud equivalent is. This is the "technical guardrails" half of item 8 and the enforcement half of 3.4.8.
3. **Write the AI section of your acceptable use policy to the three parts of item 8, plus one sentence for Section 1532.** The sentence: no model developed by DeepSeek or High Flyer, or derived from their weights, may be used in the performance of any DoD contract, regardless of where it is hosted or who bills for it. The [AI acceptable use policy post]({% post_url 2026-07-07-ai-acceptable-use-policy-small-business %}) covered the structure for a small firm. This is the addition a defense contractor needs on top of it.
4. **Name the approved enterprise AI environment, or state that there is none.** Item 8 expects one. If your answer today is "we do not use AI with Department data," write that down as a policy statement with the controls that enforce it. An assessor, a prime, or a DIBCAC reviewer treats a documented "none" very differently from silence.
5. **Anchor it in the SSP.** Reference the AI policy from 3.4.8, 3.4.9, and 3.1.20, and from 3.1.20's external-system list name any enterprise AI environment that is in scope. The [SSP template post]({% post_url 2026-06-09-cmmc-ssp-template %}) covers what an assessor reads for those controls.
6. **Record the distillation decision.** One paragraph: the statute does not define "developed by," the firm treats DeepSeek-derived weights as covered, and here is the date and the name of the person who decided. If guidance later says otherwise, you loosen a policy. If it says the same, you have a dated record of compliance.
7. **Check your prime's flow-down.** Some subcontracts already carry AI-use language. If yours names Section 1532, your policy should quote it back.

## The bottom line

The CMMC pause created a comfortable story that the AI question can wait for the task force. It cannot. One AI rule has been a federal statute for nearly nine months and follows the model wherever Microsoft or Amazon hosts it. The other is the Department's own stated priority list, item 8 of 10, and it asks for a policy, guardrails, and an explicit prohibition that no NIST 800-171 control will ever ask you for. A contractor whose only AI control is an SSP with 110 green rows has neither rule covered.

The written policy is the fastest piece to close. The [AI Acceptable Use Policy Kit](https://payhip.com/b/AKSw2) ($47) gives you the policy structure to drop the three Brilliant at the Basics parts and the Section 1532 sentence into. If the policy then needs a home in your system description, the [CMMC Level 2 System Security Plan (SSP) Template](https://payhip.com/b/gB6oD) ($77) has the 3.4.8, 3.4.9, and 3.1.20 sections already laid out to reference it from.

## Sources

- National Defense Authorization Act for Fiscal Year 2026, Public Law 119-60, Section 1532, "Guidance and Prohibition on Use of Certain Artificial Intelligence," enacted December 18, 2025 (text via congress.gov, S.1071)
- National Defense Authorization Act for Fiscal Year 2026, Section 1513
- 10 U.S.C. § 4872 (definition of "covered nation")
- Congressional Research Service, IF13197, "Cyber and Artificial Intelligence Provisions in the FY2026 National Defense Authorization Act"
- Department of War CIO, "Brilliant at the Basics," Top 10 IT Cybersecurity Best Practices for DIB Partners, item 8 (dodcio.defense.gov/BrilliantBasics and the IT Tips v1 PDF)
- Cyber AB, September 2026 Town Hall (September 30, 2026), as recapped by CMMC.com
- DefenseScoop, "Pentagon pores over heaps of industry feedback on CMMC reform," September 9, 2026 (Davies at the Billington CyberSecurity Summit)
- Microsoft Foundry model catalog, DeepSeek-V4-Pro and DeepSeek-V4-Flash model cards ("Direct from Azure," model provider DeepSeek); Microsoft Foundry Blog, "Expanding Open Model Choice in Microsoft Foundry with New DeepSeek and NVIDIA Nemotron Models"
- AWS, "DeepSeek-R1 is available fully-managed in Amazon Bedrock," March 10, 2025; AWS News Blog, same date
- Microsoft, Azure AI Foundry Blog, "DeepSeek R1 is now available on Azure AI Foundry and GitHub," January 29, 2025
- NIST SP 800-171 Revision 2 (February 2020) and Revision 3 (May 2024), requirements 3.1.3, 3.1.20, 3.4.8, 3.4.9
- DFARS 252.204-7012, Safeguarding Covered Defense Information and Cyber Incident Reporting
