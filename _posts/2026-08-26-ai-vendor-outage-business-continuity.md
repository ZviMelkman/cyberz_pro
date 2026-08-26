---
layout: post
title: "AI Vendor Outage Business Continuity: What HIPAA Already Requires, What CMMC Does Not, and What a 30-Person Firm Does This Week"
date: 2026-08-26
description: "An export-control order took Anthropic's newest models offline for 18 days. August added seven status-page incidents. Where an AI vendor outage sits in a HIPAA contingency plan, a Safeguards incident response plan, and a CMMC self-assessment."
category: AI Security
tags: [AI vendor outage, business continuity, HIPAA contingency plan, AI tools, FTC Safeguards Rule, incident response plan, CMMC, NIST 800-171, AI vendor risk, NIST AI RMF, small business cybersecurity]
image: /blog/images/1-ai-vendor-outage-business-continuity-hero.png
author: CyberZ
---

*Most AI risk advice is about what a model might say or leak. The quieter risk is that the model is simply not there on a Tuesday morning, and nobody wrote down what happens next.*

**AI vendor outage business continuity is the part of a contingency plan that treats a third-party AI model as a dependency in its own right: something that can be withdrawn by the vendor, by a regulator, or by an infrastructure failure, with no notice and no workaround inside the product. It differs from ordinary IT continuity planning in one respect that matters. Most firms adopted AI tools without a procurement decision, so the dependency was never inventoried, never given a recovery time objective, and never added to the plan that HIPAA, the FTC Safeguards Rule, or a DoD contract already required them to keep.**

<div class="key-takeaways" style="background:#16161a;border-left:4px solid #EE4C48;padding:20px 24px;margin:24px 0;">
<strong>Key Takeaways</strong>
<ul>
<li>On June 12, 2026, the US Commerce Department applied export controls to Anthropic's Claude Fable 5 and Mythos 5. Because the order took effect immediately and nationality could not be verified in real time, Anthropic suspended both models for every user worldwide. Access returned July 1. Eighteen days.</li>
<li>Anthropic's status page then logged incidents on August 5, 12, 13, 16, 18, 20 and 24, according to CybersecurityNews' review of the page. The August 24 event hit claude.ai, the API, Claude Code and Claude Cowork at once.</li>
<li>45 CFR 164.308(a)(7) makes a contingency plan a required HIPAA standard, with data backup, disaster recovery and emergency mode operation as required implementation specifications. An AI scribe or triage bot that touches ePHI belongs in that plan.</li>
<li>16 CFR 314.4(h) requires a written incident response plan covering events that affect the availability of customer information, not only breaches. A "security event" under 314.2 includes disruption of an information system.</li>
<li>NIST SP 800-171 Rev 2 tailors the entire Contingency Planning family out of scope (footnote 18). CMMC Level 2 does not require a contingency plan. Only 3.8.9, protecting the confidentiality of backup CUI, survives.</li>
<li>NIST AI RMF GOVERN 6.2 asks for contingency processes to handle failures in third-party AI resources deemed high risk. Almost nobody has one.</li>
<li>The fix is a three-question dependency map per AI workflow: which provider is underneath, what breaks in 72 hours, and what is the tested fallback.</li>
</ul>
</div>

![Timeline of Anthropic Claude Fable 5 availability from the June 9 launch, the June 12 export-control shutdown, the July 1 restoration, and seven August 2026 status-page incidents](/blog/images/2-ai-vendor-outage-timeline-june-august-2026.png)

## What actually happened in June?

Anthropic released Claude Fable 5 and Claude Mythos 5 on June 9, 2026. Three days later, on Friday, June 12, the US government applied export controls to both models. In its own account, published June 30, Anthropic explains that the order required it to restrict access by foreign nationals, whether inside or outside the United States. Because the order took effect immediately and the company had no reliable way to verify nationality in real time, it suspended access to both models for all users.

The trigger was a report from Amazon researchers who had found a way past Fable 5's safeguards, prompting it to identify software vulnerabilities and, in one case, produce exploit code. Commerce partially eased the restriction on June 26, authorizing Mythos 5 for a set of approved US organizations. The controls were lifted June 30, and Fable 5 came back on the Claude Platform, claude.ai, Claude Code and Claude Cowork on July 1. Access through AWS, Google Cloud and Microsoft Foundry was to follow "as quickly as possible," which means a firm reaching the model through a cloud marketplace was still waiting after the headline said "restored."

Two details in that account matter more than the drama.

The first is the mechanism. This was not a bug, not a breach, and not a capacity problem. It was a regulatory instrument applied to a commercial product accessed through a web interface, and it removed the product from every customer on the planet in a single step. No SLA covers that. No status page predicts it.

The second is what came back. Anthropic trained an improved classifier and, per its post, a blocked request to Fable 5 is now flagged to the user and rerouted to Claude Opus 4.8. That is a sensible safety design. It is also a documented case of a vendor changing which model answers a request, after the fact, on the vendor's terms. If a workflow was validated on one model, the firm's validation no longer describes what is running.

## Why does August matter more than June?

June was a rare event. August was ordinary, and that is the problem.

The August 24 incident opened on Anthropic's status page at 05:06 UTC as elevated errors on requests to Claude Mythos 5, Claude Fable 5, Claude Opus 5 and Claude Opus 4.8. The cause was identified by 05:27. Remediation was still in progress past 06:42. The affected components were claude.ai, the Claude API, Claude Code and Claude Cowork, which is every surface a business would use. CybersecurityNews, reviewing the same status page, counted prior incidents on August 5, 12, 13, 16, 18 and 20.

None of that is a criticism of one vendor. Every major model provider has had multi-hour incidents this year. The point is that a firm which folded a model into a daily workflow in the spring now has a dependency whose measured behavior includes an 18-day withdrawal and a month with seven dated incidents. That is a planning input. It is not a surprise anymore.

It also interacts with something we covered in the [AI vendor due diligence]({% post_url 2026-08-09-ai-vendor-due-diligence %}) post: many firms do not know which provider sits under their tools. An AI scribe, a support chatbot and a contract-drafting assistant sold by three different vendors can all be wrappers around the same model, reached through the same API. Three tools, one dependency. On a bad morning they fail together.

## What does HIPAA require when an AI tool goes dark?

More than most practices assume, because the requirement predates AI by two decades.

![Comparison grid of what HIPAA 45 CFR 164.308(a)(7), the FTC Safeguards Rule 16 CFR 314.4(h), and NIST SP 800-171 Rev 2 each require when an AI tool becomes unavailable](/blog/images/3-ai-vendor-outage-hipaa-ftc-cmmc-requirements-grid.png)

The Security Rule's general requirement at 45 CFR 164.306(a)(1) is to ensure the confidentiality, integrity and **availability** of all electronic protected health information the entity creates, receives, maintains or transmits. Availability is not an add-on. It is one third of the rule's purpose.

The operative standard is 45 CFR 164.308(a)(7), the contingency plan. It is a required standard, and it carries five implementation specifications:

- **Data backup plan** (required): retrievable exact copies of ePHI.
- **Disaster recovery plan** (required): procedures to restore any loss of data.
- **Emergency mode operation plan** (required): procedures to enable continuation of critical business processes for protection of the security of ePHI while operating in emergency mode.
- **Testing and revision procedures** (addressable).
- **Applications and data criticality analysis** (addressable): assessing the relative criticality of specific applications and data in support of the other components.

Read those against a practice that uses an ambient AI scribe for visit documentation, an AI phone agent for scheduling and triage, and an AI-assisted coding tool for claims. When the model behind those tools is unavailable, the emergency mode operation plan is the document that is supposed to say what clinicians do instead, who reverts to manual documentation, and how ePHI stays protected during the reversion. The criticality analysis is where those three tools should already be ranked against the EHR, the practice management system and email.

For most practices, none of that exists in the plan, because the plan was written before the tools arrived. That is a gap an OCR investigator can read straight off the page, and it is a trigger under the [reassessment logic]({% post_url 2026-07-27-when-to-update-hipaa-risk-assessment %}) OCR already names.

One more item, because it will come up: the January 2025 Security Rule NPRM proposes, among other things, restoring critical electronic information systems and data within 72 hours. As we detailed in the [Security Rule changes]({% post_url 2026-07-30-hipaa-security-rule-changes-2026 %}) post, that rule is not final and is now targeted for July 2027. It is worth knowing the direction of travel. It is not a current obligation.

The [HIPAA Security Risk Assessment Tool: Excel + Guide](https://payhip.com/b/vXmYA) ($57) is where the criticality ranking and the availability risks get recorded so the contingency plan has something to point at.

## What does the FTC Safeguards Rule require?

If you are a tax preparer, a CPA firm, a mortgage broker or an auto dealer, the Safeguards Rule at 16 CFR Part 314 applies, and it has a provision people skip because they think it is about hacking.

16 CFR 314.4(h) requires a written incident response plan designed to promptly respond to, and recover from, any security event materially affecting the confidentiality, integrity, or availability of customer information in your control. The definition of "security event" at 314.2 includes an event resulting in disruption of an information system. An AI tool that processes customer tax or financial data, and that stops working for a day, is a disruption of an information system that handles customer information.

The plan has to address, among other things, the goals of the plan, internal processes for responding, roles and responsibilities, communications, remediation of identified weaknesses, documentation, and post-event evaluation and revision. There is no carve-out for the event being the vendor's fault.

## What does CMMC require? (Less than you think)

Here is the part defense contractors should get right, because getting it wrong in either direction costs money.

NIST SP 800-171 Rev 2 is the assessment baseline for CMMC Level 2. Footnote 18 of that publication states that the contingency planning, system and services acquisition, and planning requirement families are not included within its scope due to the tailoring criteria. The one exception drawn from contingency planning is a requirement to protect the confidentiality of system backups, derived from CP-9, which appears as 3.8.9 in the Media Protection family.

So a CMMC Level 2 self-assessment does not ask for a contingency plan, a disaster recovery plan, or a recovery time objective. It asks whether backup CUI is protected at its storage locations. Separately, 3.6.1 requires an operational incident-handling capability that includes preparation, detection, analysis, containment, recovery and user response. That is about security incidents, not vendor availability, though a well-written incident response plan can carry both.

The practical consequences:

- **Do not claim more than you have.** If a prime's questionnaire asks about business continuity and you point to your SSP, you are pointing at a document that was never required to cover it. Answer the prime's question on its own terms.
- **Do not assume DoD is indifferent.** DFARS 252.204-7012 is about safeguarding CUI and reporting cyber incidents. Availability is a contract performance issue, and a subcontractor that misses a delivery because its AI-assisted engineering workflow went dark for three days will discover the prime cares.
- **The pause changed nothing here.** The Phase 2 suspension we covered in [Is CMMC still required?]({% post_url 2026-07-19-is-cmmc-still-required %}) left self-assessment and the DIBCAC in place. 3.8.9 is still a scored control, and a [DIBCAC assessment]({% post_url 2026-07-26-dibcac-assessment-preparation %}) will still ask to see backup protection evidence.

If a contractor uses an AI tool anywhere near CUI, the bigger question is whether it should be there at all, which we covered in the piece on [ChatGPT and CUI]({% post_url 2026-08-04-ai-tools-cui-compliance %}). Continuity is the second question. Scope is the first.

## What does NIST AI RMF say?

For a firm that has adopted the AI Risk Management Framework as its governing reference, which we recommend for anyone in a regulated vertical, the relevant subcategory is GOVERN 6.2: contingency processes are in place to handle failures or incidents in third-party data or AI resources that are deemed to be high-risk. MANAGE 3.1 adds that AI risks and benefits from third-party resources are regularly monitored, with risk controls applied and documented.

The framework is voluntary. It is also the reference point regulators and auditors increasingly cite, and "we mapped to AI RMF" is a claim that can be tested by asking for the GOVERN 6.2 artifact. For most firms the honest answer is that there is none.

## How do you build the dependency map?

The work is a table, not a program. One row per workflow that calls an AI model. Three columns.

![The three-question AI dependency map: which provider is underneath each tool, what breaks in 72 hours, and what is the tested fallback](/blog/images/4-ai-dependency-map-three-questions.png)

**Which provider is underneath?** Look below the application. The vendor's subprocessor page, DPA or security documentation will name the model provider. If it does not, ask in writing, using the questions from the vendor due diligence post. Then look across rows. If four workflows resolve to one provider, you have one dependency wearing four logos.

**What breaks in 72 hours?** For each row, one of three answers: the process stops, the process slows, or the process shifts to a person. Write down who that person is and roughly what the shift costs per day. Where a workflow touches ePHI, this is the emergency mode operation plan entry. Where it touches customer financial information, it is the 314.4(h) entry. A 72-hour horizon is not a regulatory number for most readers. It is the length of an outage that is long enough to matter and short enough to plan around, and it happens to match the direction the HIPAA NPRM is pointing.

**What is the tested fallback?** Manual procedure, queued work, or a second approved provider. Two rules. An untested fallback does not exist. And a second provider only counts if the tool can actually switch to it, which for most SaaS products you do not control. For those, the fallback is manual, and the plan should say so plainly rather than implying a resilience the vendor never built.

The map is not a substitute for a contingency plan or an incident response plan. It is the annex those plans reference so that the words "AI tools" in the plan resolve to specific systems, owners and procedures.

## What this looks like at a 30-person firm

A 30-person medical practice runs an EHR, a practice management system, a patient portal, a phone system, email and file storage, an ambient AI scribe, an AI phone agent that handles after-hours scheduling and symptom triage, and a coding assistant inside the billing platform.

The scribe and the phone agent both turn out to sit on the same frontier model provider through their respective vendors. The coding assistant sits on a different one. That is two dependencies, not three tools.

![Six-item checklist for a small firm to add AI vendor outage planning to its HIPAA contingency plan or Safeguards incident response plan this week](/blog/images/5-ai-vendor-outage-continuity-checklist-this-week.png)

If the first provider is dark for a day, clinicians document manually, which they did before the scribe arrived, and the after-hours line rolls to the answering service that is still under contract. The cost is provider time and some scheduling lag. That is a workable fallback, and it takes ten minutes to write down. If the same provider is dark for eighteen days, the practice needs to know by day three whether the vendor can switch models, whether the answering service can absorb the daytime load, and who signs off on that spend. That decision is easier to make on a Tuesday in August than at 6 a.m. on the morning it happens.

The billing assistant is the interesting one. Its loss slows claims rather than stopping care, but slow claims are a cash-flow event for a practice this size. It belongs in the criticality analysis at a higher rank than most people would guess.

Total effort: an afternoon to build the map, an hour to revise the contingency plan, a lunch hour for a tabletop. The plan on the shelf then describes the practice that exists, which is the entire point of the HIPAA standard.

## What to do this week

1. **Inventory every workflow that calls an AI model**, including features bundled into tools you already had. The vendor due diligence sweep is the same list.
2. **Write the provider name next to each row.** Note where rows share a vendor.
3. **Set a recovery time objective per row**: minutes, same day, or next week. Be honest about "next week." Some things can wait.
4. **Write the manual fallback and assign an owner.** For ePHI workflows, this goes in the emergency mode operation plan. For customer financial data, it goes in the 314.4(h) plan.
5. **Add the rows to the plan and date the revision.** A plan revised in 2022 that does not mention AI is evidence of a gap. The same plan with an August 2026 revision date and an AI annex is evidence of a program.
6. **Run one tabletop.** Assume the main provider is dark for 72 hours. Walk each fallback out loud with the people who would execute it. Fix what does not work.

The policy layer that makes this stick is the acceptable use policy, because that is where approved tools, approved fallbacks and the rule that nobody adds a new AI dependency without a row in the map all live. The [AI Acceptable Use Policy Kit](https://payhip.com/b/AKSw2) ($47) includes the vendor, subprocessor and continuity language most AI policies leave out, alongside the employee-use sections, and our post on [building an AI acceptable use policy]({% post_url 2026-07-07-ai-acceptable-use-policy-small-business %}) covers how to roll it out.

## The bottom line

An AI model is now the same class of dependency as email or the practice management system, with one difference: it can be withdrawn by a vendor, a regulator or an infrastructure fault with no notice, and the product you bought usually cannot switch to anything else. HIPAA's contingency plan standard already requires you to plan for that. The Safeguards Rule's incident response plan already covers disruption. CMMC Level 2 does not require a contingency plan at all, which is worth knowing before you claim one. NIST AI RMF names the artifact at GOVERN 6.2. None of those documents will list your AI dependencies for you. An afternoon with a three-column table will.

## Sources

- Anthropic, *Redeploying Claude Fable 5*, June 30, 2026. Account of the June 12 export-control order, the worldwide suspension, the June 26 partial authorization, the June 30 lifting, and the July 1 restoration. anthropic.com/news/redeploying-fable-5.
- Anthropic status page, incident of August 24, 2026 (investigating 05:06 UTC, identified 05:27 UTC, remediation ongoing 06:42 UTC; components claude.ai, Claude API, Claude Code, Claude Cowork). Timeline as quoted by Arabian Business and CybersecurityNews, August 24, 2026.
- CybersecurityNews, *Anthropic's Claude AI Suffers Another Outage With Elevated Errors*, August 24, 2026. Review of status-page incidents dated August 5, 12, 13, 16, 18 and 20, 2026.
- 45 CFR 164.306(a)(1), Security standards: general rules. Electronic Code of Federal Regulations.
- 45 CFR 164.308(a)(7), Administrative safeguards, contingency plan standard and implementation specifications (ii)(A) through (E). Electronic Code of Federal Regulations.
- HHS Office for Civil Rights, *HIPAA Security Rule To Strengthen the Cybersecurity of Electronic Protected Health Information*, Notice of Proposed Rulemaking, 90 FR 898, January 6, 2025 (RIN 0945-AA22). Proposed 72-hour restoration requirement. Not final.
- 16 CFR 314.2, definition of "security event," and 16 CFR 314.4(h), incident response plan. Electronic Code of Federal Regulations.
- NIST SP 800-171 Rev 2, *Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations*, footnote 18 on tailoring of the contingency planning family, requirement 3.8.9, requirement 3.6.1. NIST, February 2020 (updated January 2021).
- NIST AI 100-1, *Artificial Intelligence Risk Management Framework (AI RMF 1.0)*, GOVERN 6.2 and MANAGE 3.1. NIST, January 2023.
- DFARS 252.204-7012, Safeguarding Covered Defense Information and Cyber Incident Reporting.
