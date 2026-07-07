---
layout: post
title: "AI Acceptable Use Policy: What a Small Business Actually Needs in 2026"
date: 2026-07-07
image: /blog/images/1-ai-acceptable-use-policy-hero.png
description: "What an AI acceptable use policy must cover for a small business: approved tools, four data classes, incident reporting, and a one-session rollout plan."
---

*Your employees did not wait for permission to start using AI. The rules can either catch up or stay theoretical.*

**An AI acceptable use policy (AI AUP) is a short internal document that names which AI tools employees may use, on which account types, with which categories of company and client data, and what everyone does when data ends up somewhere it should not.** Most small businesses in regulated industries do not have one. Most of their employees are already using AI tools anyway.

<div class="key-takeaways" style="background:#f6f6f8;border-left:4px solid #EE4C48;padding:18px 22px;margin:24px 0;">
<strong>Key Takeaways</strong>
<ul>
<li>Cyberhaven found 27.4% of corporate data entered into AI tools in March 2024 was sensitive, up from 10.7% a year earlier. Most flows through personal accounts the business cannot see.</li>
<li>Personal AI accounts are the core exposure: model training is commonly on by default and there are no admin controls. Business tiers flip both.</li>
<li>Four data classes (Public, Internal, Confidential, Regulated) decide almost every real question an employee will have.</li>
<li>An approved-tools register with a fast request process beats a blanket ban, which just moves usage to personal phones.</li>
<li>No-blame incident reporting is the clause that makes everything else enforceable in practice.</li>
</ul>
</div>

## The gap between AI use and AI rules

The numbers on unsanctioned AI use came into focus early. In February 2023, security firm Cyberhaven measured that about 11% of what employees paste into ChatGPT is confidential company data. By March 2024, its follow-up analysis found 27.4% of corporate data entered into AI tools was classified as sensitive, up from 10.7% a year before.

Two details in that pattern matter more than the headline percentages.

First, most of this usage runs through personal accounts. A personal ChatGPT, Gemini, or Claude account typically reserves the right to use entered content for model training unless the user opts out, and gives the employer no visibility, no retention control, and nothing to switch off when someone leaves. OpenAI's own enterprise privacy documentation draws the line explicitly: business and enterprise tier inputs are excluded from training by default, consumer tiers are not.

Second, none of it is malicious. The paralegal summarizing a deposition, the bookkeeper drafting a client email, the office manager cleaning up meeting notes: these are productive people using the fastest tool available. That is exactly why discipline-first responses fail. You are not fighting sabotage. You are competing with convenience.

If you want the fuller picture of what unsanctioned AI tools do inside a small firm, the earlier breakdown is here: [what AI is actually doing inside your business]({% post_url 2026-04-14-shadow-ai-risks-small-business %}).

## Why "just ban it" fails

The tempting answer is a one-line memo: no AI tools at work. It fails predictably, and it fails silently.

A ban does not remove the productivity pressure that drove adoption. It removes the visibility. Usage shifts to personal phones and home laptops, where no policy, no network control, and no offboarding process reaches it. The business trades a manageable, inspectable risk for an invisible one, and gains a false sense of resolution in the bargain.

The workable posture is the opposite: a short list of approved tools on business accounts, a fast process for requesting new ones, and clear data rules. People get a sanctioned way to do what they were going to do anyway. The business gets its visibility back.

## The four data classes that do the heavy lifting

Most of an AI policy's daily value comes from one table: what class of information is this, and what does that class allow?

![The four data classes: what may and may not go into an AI tool](/blog/images/2-ai-data-classes-matrix.png)

**Public** information (published copy, website text, press releases) can go into any approved tool.

**Internal** information (meeting notes without client names, process documentation, drafts) belongs only in approved tools on business or enterprise accounts.

**Confidential** information (client names and matters, pricing, contracts, financials, proprietary code) enters an AI tool only where the approved-tools register explicitly allows it for that specific tool, with a training opt-out confirmed. The default answer is no.

**Regulated** information never enters an AI tool unless the tool is contractually approved for that data type. This is where industry regimes attach by data type, not by preference: protected health information under HIPAA, controlled unclassified information under DFARS 252.204-7012 and CMMC, taxpayer data under IRS Publication 4557, cardholder data under PCI DSS. Credentials, passwords, and API keys sit in this class too, with no exceptions at all.

The test that resolves most edge cases in five seconds: would you be comfortable if this exact text appeared on a stranger's screen? If not, it does not get pasted.

## What belongs in the policy itself

A usable small-business AI policy runs six to eight pages, not thirty. NIST's AI Risk Management Framework puts governance, meaning documented policies and clear accountability, at the foundation of managing AI risk, and that is precisely what this document is: the governance layer, sized for a firm without a compliance department. The sections that earn their place:

**Scope that matches reality.** The policy covers chat assistants, AI features embedded in software you already pay for (Microsoft 365 Copilot, Zoom AI Companion, Grammarly), browser extensions, meeting transcribers, and code assistants, on any device and any account. Scoping only to "AI websites" misses most of the actual surface.

**Business accounts only.** The single highest-value rule available. It converts the training-default problem and the visibility problem in one move, usually for a modest per-seat cost.

**An approved-tools register as an appendix.** The living list of what is allowed, on which account type, up to which data class. Employees get one place to look. The register updates without re-issuing the policy.

**A request path with a deadline.** Tool name, use case, data class involved, answer within five business days. If requesting takes longer than working around the rule, people work around the rule.

**No-blame incident reporting.** When confidential data goes into the wrong tool, the clock matters: vendor deletion controls, credential rotation, client notification duties under contracts. A policy that punishes the person who reports guarantees you hear about incidents late or never. Concealment is the violation; the prompt report is the system working.

**Human review of output.** AI output is a draft. Whoever ships the deliverable owns it, whatever tool produced the first version.

## The regulated-data overlay

If your firm operates under HIPAA, handles CUI on defense contracts, prepares tax returns, or takes card payments, the AI policy does not replace your compliance obligations. It closes a specific new gap in them: the informal channel through which regulated data reaches third-party processors nobody vetted.

A dental office manager pasting a patient email thread into a consumer chatbot has just disclosed PHI to a vendor with no business associate agreement. A defense subcontractor's engineer asking a public model to debug code containing CUI has created exactly the kind of nonconformity that surfaces in assessments and, lately, in False Claims Act theories. The policy's regulated class exists so those events are named, prohibited, and reportable before they become findings.

## Rolling it out in one working session

The order of operations matters, because a policy written before discovery describes a fantasy company.

![Five steps: discover, score, register, publish, maintain](/blog/images/3-ai-policy-5-step-rollout.png)

**Discover (60 to 90 minutes).** Inventory every AI tool actually in use: ask department leads directly, check browser extensions on a few sample machines, scan expense reports for AI vendors, review SSO third-party app logs if you have them.

**Score (30 minutes).** For each tool: account type, most sensitive data class anyone has entered, formally approved or not. Rank the results and fix the high-risk items first, which usually means moving personal accounts to a business tier with training turned off.

**Register (15 minutes).** Everything you keep goes onto the approved-tools register with its account type and data ceiling.

**Publish (45 minutes).** Fill in the policy, attach the register as Appendix A, distribute, and collect signed acknowledgments. An unacknowledged policy is close to unenforceable.

**Maintain (ongoing).** One 20-minute team walkthrough beats any memo. Review annually and whenever a vendor changes its data terms.

## The bottom line

Shadow AI is a visibility problem before it is a policy problem, and it is already inside the building. The response that works is boring and fast: find what is in use, move it onto accounts you control, publish rules built on four data classes, and protect the person who reports the mistake. A firm of ten can have this done, signed, and enforceable inside a week.

The [AI Acceptable Use Policy Template & Shadow AI Worksheet](https://payhip.com/b/AKSw2) ($47) is the fill-in policy and the discovery worksheet this walkthrough is built on, ready to run as-is.

## Sources

- Cyberhaven, "11% of data employees paste into ChatGPT is confidential," February 2023, and Cyberhaven AI adoption and risk analysis, March 2024 (27.4% vs 10.7% sensitive-share figures)
- OpenAI, Enterprise Privacy documentation (training defaults by account tier)
- NIST, Artificial Intelligence Risk Management Framework (AI RMF 1.0), January 2023
- IRS Publication 4557, Safeguarding Taxpayer Data
- DFARS 252.204-7012; 32 CFR Part 170 (CMMC Program)
- HHS, HIPAA Privacy and Security Rules (45 CFR Parts 160 and 164)
