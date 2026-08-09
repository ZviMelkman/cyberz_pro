---
layout: post
title: "AI Vendor Due Diligence: What to Ask When Software You Already Approved Adds AI"
date: 2026-08-09
description: "A vendor audit of 2,400 software providers found 63.6% never name the third-party AI subprocessor touching customer data. What 16 CFR 314.4(f), 45 CFR 164.308(b), and NIST AI RMF require when a vendor changes its data flow, plus the 12 questions to send."
category: AI Security
tags: [AI vendor due diligence, AI subprocessor, third-party risk, shadow AI, FTC Safeguards Rule, HIPAA, business associate, NIST AI RMF, AI governance, vendor risk management]
image: /blog/images/1-ai-vendor-due-diligence-hero.png
author: CyberZ
---

*Most shadow AI advice assumes an employee went out and signed up for something. The harder version is the vendor you approved two years ago quietly adding a model provider to the back of your data flow.*

**AI vendor due diligence is the process of verifying which AI systems and AI subprocessors a third-party vendor uses to handle your data, whether that data trains or is retained by a model, and whether the answers are documented in a current contract. It differs from ordinary vendor due diligence in one respect that matters operationally: the trigger is not onboarding. A vendor you already assessed can add an AI subprocessor through a routine product release, which changes where your data goes without changing anything you signed. Under 16 CFR 314.4(f)(3) and 45 CFR 164.308(a)(8), the duty to reassess sits with you, not with the vendor's release calendar.**

<div class="key-takeaways" style="background:#16161a;border-left:4px solid #EE4C48;padding:20px 24px;margin:24px 0;">
<strong>Key Takeaways</strong>
<ul>
<li>DataGrail's Privacy and AI Trends Report 2026 reviewed the data protection assessments of 2,400 business software providers advertising AI capabilities and found 63.6% did not disclose a third-party AI subprocessor. IAPP reported the findings on July 22, 2026.</li>
<li>The same report found 32.8% of AI systems self-disclosed high-risk processing of sensitive data or automated decision-making, which is the category most likely to carry a documentation obligation.</li>
<li>Feature bundling is the common delivery mechanism, not a new purchase. Google folded Gemini into every Workspace Business and Enterprise tier in January 2025 and retired the standalone add-on, so the AI arrived without a procurement decision anywhere.</li>
<li>16 CFR 314.4(f) has three prongs, and the third is the one firms skip: periodically assess service providers based on the risk they present and the continued adequacy of their safeguards. 314.4(g) adds a duty to adjust the program on any material change to business arrangements.</li>
<li>Under 45 CFR 164.308(b)(2), your business associate must obtain satisfactory assurances from its own subcontractor. You do not sign a BAA with the model provider, and a covered entity is expressly not required to. The chain still has to exist, and your risk analysis still has to reflect where ePHI actually goes.</li>
<li>NIST AI RMF GOVERN 6.1 asks for policies addressing AI risks from third-party entities. GOVERN 1.6 asks for a mechanism to inventory AI systems. Neither is satisfied by a policy that only governs employee tool use.</li>
<li>A vendor that will not answer in writing has given you an answer. Document the request, the non-response, and the compensating control you applied.</li>
</ul>
</div>

![Three statistics from the DataGrail Privacy and AI Trends Report 2026: 2,400 business software providers reviewed, 63.6% did not disclose a third-party AI subprocessor, 32.8% self-disclosed high-risk processing](/blog/images/2-ai-vendor-subprocessor-disclosure-gap.png)

## What changed about vendor risk when vendors started shipping AI?

The mechanics of vendor approval assume a stable product. You assess a tool, you record what data it touches, you sign a data processing agreement or a business associate agreement, and the file describes reality until the contract renews. Product releases were not supposed to move data.

That assumption broke quietly. DataGrail's Privacy and AI Trends Report 2026, released at the end of May 2026, reviewed the data protection assessments of 2,400 popular business software providers that advertise AI capabilities. It found that 63.6% did not disclose sub-processing activity conducted by another AI provider, and that 32.8% of AI systems self-disclosed engaging in high-risk processing of sensitive data or automated decision-making. IAPP covered the report on July 22, 2026, with commentary from privacy counsel on what the gap means for buyers.

Two caveats worth stating, because the number gets quoted loosely. This is a vendor-published study, so treat 63.6% as directional rather than as a regulator's finding. And DataGrail's own CEO framed the cause as speed rather than concealment: engineering ships features faster than legal teams can update the paperwork behind them. That framing does not reduce your exposure. It does change what a productive vendor conversation sounds like.

The delivery mechanism is usually bundling. In January 2025 Google folded Gemini into all Workspace Business and Enterprise tiers, eliminated the separate Gemini add-on that had been sold at roughly $20 per user per month, and raised base plan prices by about $2 per user per month. New-customer pricing took effect January 16, 2025, and existing subscriptions moved no sooner than March 17, 2025. Nobody at any customer submitted a purchase request. The AI showed up with the invoice.

## Why does a new AI subprocessor matter if the vendor is already approved?

Because the approval was not a judgment about the vendor. It was a judgment about a data flow.

When you approved the tool, you assessed a specific path: your data goes to the vendor, is processed for a defined purpose, and rests in a known location under known terms. Adding a model provider extends that path by a link you never evaluated. Your practice management vendor is your direct relationship. The inference host behind its new summarization feature is a fourth party, one step further out, and it is the one now holding text derived from your records.

That extra link changes four things at once:

- **Location.** Inference may run in a different region or a different cloud than the vendor's primary hosting, which matters for any contractual or regulatory data residency commitment you made.
- **Retention.** The vendor's retention schedule does not automatically bind its model provider. Prompt and output retention at the inference layer is a separate setting with a separate default.
- **Training.** Whether your data trains a model is a term in the vendor's agreement with its provider, not in yours.
- **Breach scope.** An incident at the model provider is a vendor incident that flows to you. Your notification analysis has to reach a party you cannot name.

None of this requires anyone to behave badly. It requires only that a product team shipped and nobody re-opened the file.

## What do the rules require when a vendor's data flow changes?

No US regulation currently says "assess your vendor's AI subprocessors" in those words. Several say something functionally equivalent, and the obligation lands on you rather than on the vendor.

### FTC Safeguards Rule: the third prong is the one that binds

16 CFR 314.4(f) requires a financial institution to oversee service providers by doing three things: taking reasonable steps to select and retain providers capable of maintaining appropriate safeguards, requiring those safeguards by contract, and periodically assessing providers based on the risk they present and the continued adequacy of their safeguards.

Most programs implement the first two and stop. The third prong is what a vendor's AI release triggers, because "continued adequacy" is a moving target by construction. 16 CFR 314.4(g) reinforces it from the other direction, requiring you to evaluate and adjust your information security program in light of any material changes to your operations or business arrangements, or any other circumstances you know or have reason to know may materially affect the program. A vendor routing customer information through a new model provider is a material change to a business arrangement. Whether you had reason to know is a question you would rather answer with a dated file than with a memory.

This reaches accounting practices, tax preparers, auto dealers, mortgage brokers, and every other non-bank financial institution inside the FTC's jurisdiction, most of which run on exactly the kind of bundled SaaS that added AI over the last eighteen months.

### HIPAA: the chain has to hold, but you do not hold all of it

The HIPAA structure is more specific than most summaries suggest, and getting it right matters here.

Under 45 CFR 164.308(b)(1), a covered entity may let a business associate handle ePHI only if it obtains satisfactory assurances that the business associate will safeguard the information. The same paragraph states plainly that a covered entity is **not** required to obtain those assurances from a business associate that is a subcontractor. Under 164.308(b)(2), the business associate must obtain them from its subcontractor, and 164.314(a)(2)(i)(B) requires the business associate to ensure any subcontractor handling ePHI enters a compliant contract.

So a 20-person practice does not sign a BAA with the model provider behind its EHR vendor's new note-summarization feature, and should not try. What it must be able to establish is that the chain exists: the vendor has a BAA with the subcontractor, and the vendor is willing to say so in writing.

Two of your own obligations do not delegate. 164.308(a)(1)(ii)(A) requires an accurate and thorough assessment of risks to the ePHI you hold, and an assessment that describes a data flow the vendor stopped using is neither accurate nor thorough. 164.308(a)(8) requires periodic evaluation of your safeguards against changes affecting ePHI security. A vendor adding an AI subprocessor is such a change, whether or not the vendor called it one. Our post on [when to update your HIPAA risk assessment]({% post_url 2026-07-27-when-to-update-hipaa-risk-assessment %}) covers the trigger standard in detail, and the [ChatGPT and HIPAA breakdown]({% post_url 2026-07-23-is-chatgpt-hipaa-compliant %}) covers the direct-use version of the question.

If you need the assessment itself rather than the theory, the [HIPAA Security Risk Assessment Tool: Excel + Guide](https://payhip.com/b/vXmYA) ($57) is the workbook we use to document risks, safeguards, and the evaluation dates that 164.308(a)(8) asks about.

### Defense contractors: the clause does not care that the feature was free

If your contracts carry DFARS 252.204-7012, paragraph (b)(2)(ii)(D) requires any external cloud service that stores, processes, or transmits covered defense information to meet security requirements equivalent to the FedRAMP Moderate baseline and to comply with paragraphs (c) through (g) for incident reporting and media preservation. A vendor enabling an AI feature that routes CUI-adjacent text through a commercial inference endpoint has moved your data outside the boundary described in your system security plan, and the fact that the feature arrived as an update does not change the analysis. The full treatment is in our post on [whether you can use ChatGPT with CUI]({% post_url 2026-08-04-ai-tools-cui-compliance %}) and the [external service provider requirements]({% post_url 2026-07-12-cmmc-external-service-provider-requirements %}) breakdown.

### NIST AI RMF and the EU AI Act: inventory and role

NIST AI RMF GOVERN 6.1 calls for policies and procedures addressing AI risks arising from third-party entities, and GOVERN 6 more broadly covers third-party software, data, and supply chain issues. GOVERN 1.6 calls for mechanisms to inventory AI systems, resourced according to risk priorities. An inventory that lists only the AI tools your staff signed up for is missing the category this article is about.

For anyone in scope of the EU AI Act, the role question is sharper. Article 50 transparency obligations became applicable on August 2, 2026, and the obligations attaching to a deployer differ from those attaching to a provider. You can inherit a deployer role through a vendor feature you did not know had shipped, which is the least comfortable way to acquire a legal obligation. Our post on [AI content labeling requirements]({% post_url 2026-08-03-ai-content-labeling-requirements %}) walks through the transparency rules that went live that day.

## How do you find out what your vendors actually turned on?

Waiting for notice does not work, because the notice mechanism is usually a subprocessor page updated silently. The sweep below takes about half an hour for a stack of ten to fifteen tools and produces a dated record either way.

![Five-step sweep for discovering vendor AI features: subprocessor page, DPA version date, release notes, admin console toggles, and OAuth grants](/blog/images/3-ai-vendor-ai-feature-discovery-sweep.png)

The fifth step catches the case that looks least like a vendor problem. An AI assistant that a staff member connected to your mail or file storage through an OAuth grant holds a persistent token and appears in no procurement record at all. Our [Google Workspace OAuth audit walkthrough]({% post_url 2026-06-04-shadow-ai-oauth-google-workspace-audit %}) covers how to enumerate and revoke those grants, and the broader pattern is in the [shadow AI risks]({% post_url 2026-04-14-shadow-ai-risks-small-business %}) post.

Rank what you find by data sensitivity, not by vendor size. The tool holding client files matters more than the tool holding your marketing calendar, regardless of which vendor has the better trust page.

## The 12 questions to send

Send one email per vendor. Ask for written answers. A support agent's verbal reassurance that "your data isn't used for training" is worth nothing in a file six months from now, and a dated email from the vendor is worth quite a lot.

![Twelve vendor AI due diligence questions grouped into data flow, control, and evidence categories](/blog/images/4-ai-vendor-due-diligence-12-questions.png)

Two of these carry more weight than the rest. Question 7, on notice before a new subprocessor is added, is the only one that fixes the problem going forward rather than describing it today. Question 12, on liability for a subprocessor-caused breach, is the one that tends to produce a phone call from someone with authority.

## What if the vendor will not answer?

Some will not, particularly the large ones where you are a small account. That outcome is workable as long as you treat it as a finding rather than a dead end.

- **Document the request and the silence.** A dated email, the vendor's non-response, and your assessment of the residual risk is a defensible record. An undocumented assumption is not.
- **Apply the control you do have.** Most enterprise suites expose a tenant-level or group-level switch for AI features. Turning it off for the groups handling regulated data is a real control, available today, that does not require the vendor's cooperation.
- **Write the risk acceptance down and date it.** Name who accepted it and when it gets revisited. This is the difference between a decision and a gap.
- **Set an exit condition.** For the small number of tools where the answer genuinely matters and the vendor will not engage, decide now what would make you migrate, so the decision is not made during an incident.

The policy layer is what makes any of this repeatable. If you need the governing document rather than a one-off sweep, the [AI Acceptable Use Policy Kit](https://payhip.com/b/AKSw2) ($47) includes the vendor and subprocessor language that most AI policies leave out, alongside the employee-use sections. Our post on [building an AI acceptable use policy]({% post_url 2026-07-07-ai-acceptable-use-policy-small-business %}) covers the employee-facing half.

## What this looks like at a 25-person firm

A 25-person accounting practice runs roughly a dozen tools: a tax package, a document portal, a practice management system, email and file storage, e-signature, a payroll integration, a CRM, a scheduling tool, and a handful of utilities.

Three of those touch customer information in the FTC Safeguards sense. The sweep takes an afternoon. Realistically it returns one bundled AI feature the firm did not know was on, one vendor whose subprocessor page is newer than the DPA on file, and one OAuth grant to a meeting-notes assistant that somebody connected in March.

The remediation is not dramatic. Disable the AI features in the two tools where nobody asked for them. Send the twelve questions to the three vendors that matter. Revoke the OAuth grant and add the assistant to the approved list properly, or do not. Write the results into the written risk assessment that 314.4(b) already requires, with today's date on it.

Total effort is a few hours. What it buys is that the file on the shelf describes the firm that exists.

## The bottom line

Vendor due diligence built around onboarding cannot keep up with vendors that ship AI features into live subscriptions. The regulations already anticipated this in general terms: 16 CFR 314.4(f)(3) asks for periodic reassessment, 314.4(g) asks for adjustment on material change, 45 CFR 164.308(a)(8) asks for periodic evaluation, and NIST AI RMF GOVERN 6.1 asks for policies covering third-party AI risk. None of them will tell you which of your vendors turned something on last quarter. Half an hour per vendor and twelve questions in writing will.

## Sources

- 16 CFR 314.4, Standards for Safeguarding Customer Information, Elements. Paragraph (f) on service provider oversight and paragraph (g) on evaluating and adjusting the program. Electronic Code of Federal Regulations.
- 45 CFR 164.308, Administrative safeguards. Paragraph (a)(1)(ii)(A) risk analysis, paragraph (a)(8) evaluation, paragraph (b)(1) and (b)(2) business associate and subcontractor assurances. Electronic Code of Federal Regulations.
- 45 CFR 164.314(a)(2)(i)(B), business associate contract requirement to ensure subcontractor compliance. Electronic Code of Federal Regulations.
- DFARS 252.204-7012(b)(2)(ii)(D), safeguarding covered defense information and cyber incident reporting, cloud service provider requirements.
- NIST AI 100-1, Artificial Intelligence Risk Management Framework (AI RMF 1.0), GOVERN 1.6 and GOVERN 6. NIST, January 2023.
- NIST AI 600-1, Generative AI Profile, GOVERN 6.1 third-party entity risks. NIST, July 2024.
- DataGrail, Privacy and AI Trends Report 2026, released end of May 2026. Data protection assessments of 2,400 business software providers advertising AI capabilities.
- Alex LaCasse, "How shadow AI and hidden subprocessors are challenging governance and compliance efforts," IAPP, July 22, 2026.
- Google Workspace Updates, Gemini included across Business and Enterprise editions with revised plan pricing, announced January 15, 2025, new-customer pricing effective January 16, 2025.
- Regulation (EU) 2024/1689, Artificial Intelligence Act, Article 50 transparency obligations, applicable August 2, 2026.
