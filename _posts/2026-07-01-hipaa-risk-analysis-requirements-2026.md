---
layout: post
title: "HIPAA Risk Analysis Requirements in 2026: The Scope Gaps OCR Is Fining"
date: 2026-07-01
category: healthcare
tags: [HIPAA, risk analysis, OCR, compliance, ePHI]
image: /blog/images/1-hipaa-risk-analysis-2026-hero.png
description: "What a HIPAA risk analysis has to cover in 2026, what OCR is actually fining, and why the AI and SaaS tools your staff already use belong in scope."
permalink: /blog/2026/07/01/hipaa-risk-analysis-requirements-2026/
---

*The 2026 rule everyone is bracing for is still only proposed. Meanwhile OCR keeps fining practices under the rule already in force, and the failure keeps showing up in the same place.*

**A HIPAA risk analysis is the accurate and thorough assessment of the risks and vulnerabilities to all electronic protected health information (ePHI) your organization creates, receives, maintains, or transmits. It is a required implementation specification under 45 CFR 164.308(a)(1)(ii)(A), not an optional best practice. In 2026, the word "thorough" carries more weight than it used to, because ePHI now flows through cloud apps, SaaS platforms, and AI assistants, not just your electronic health record.**

<div style="background:#16161a;border-left:4px solid #EE4C48;border-radius:8px;padding:20px 24px;margin:28px 0;">
<strong style="color:#EE4C48;letter-spacing:1px;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0 0;padding-left:20px;line-height:1.6;">
<li>The sweeping 2026 HIPAA Security Rule update is still a proposed rule. As of mid-2026 there is no final rule, so OCR is enforcing the current Security Rule today.</li>
<li>On April 23, 2026, OCR announced four ransomware settlements totaling $1,165,000. In every case the cited failure was a missing risk analysis, not the ransomware itself.</li>
<li>"Accurate and thorough" means mapping every place ePHI lives, including the tools staff adopted without telling anyone.</li>
<li>Un-scoped AI chatbots, SaaS apps, and cloud storage are the gap OCR investigations keep finding.</li>
<li>A risk analysis must be documented, reviewed, and updated whenever your technology or business changes.</li>
</ul>
</div>

## The rule you are preparing for is still proposed. The rule you are judged by is not.

If your inbox looks like most compliance officers', it is full of warnings about the "biggest HIPAA change in a decade." That refers to the Security Rule overhaul HHS proposed in December 2024 and published in the Federal Register on January 6, 2025. The proposal would end the longstanding "addressable" flexibility and make encryption, multi-factor authentication, asset inventories, network segmentation, and annual audits mandatory.

Here is the part several vendor blogs get wrong: it has not happened yet. The public comment period closed in March 2025, OCR reportedly received more than 4,700 comments, and a coalition of over 100 hospital and provider groups asked HHS to withdraw the proposal. The agency's own agenda targeted a spring 2026 final rule, but that window passed with nothing published. As of mid-2026 it remains a proposed rule. It binds no one.

What binds you is the Security Rule that has been in force since 2003, most recently updated in 2013. Under that rule, the risk analysis provision is the single most frequently cited deficiency in OCR investigations. So while it is smart to prepare for the proposed controls, the enforcement risk sitting in front of you today is much simpler, and much older, than the headlines suggest.

## What OCR actually fined in April 2026

![Stat callout showing four HIPAA settlements on April 23 2026, $1.16 million total, 427,000-plus individuals affected, root cause a missing accurate and thorough risk analysis.](/blog/images/3-hipaa-ocr-2026-enforcement-stat.png)

On April 23, 2026, the HHS Office for Civil Rights announced settlements with four separate organizations following ransomware investigations under the Security Rule. The four incidents were unrelated, but together they exposed the ePHI of more than 427,000 individuals, and they produced $1,165,000 in penalties. Each organization also agreed to a corrective action plan monitored by OCR for two years.

The settling entities were Regional Women's Health Group (doing business as Axia Women's Health), Assured Imaging, Consociate Health, and the Star Group health benefits plan. Different sizes, different corners of the industry.

Read one at a time, these look like ordinary breach cases. Read together, they are a statement of enforcement philosophy. In each case, OCR concluded that the organization had failed to conduct an accurate and thorough risk analysis before the attack. That failure, under 45 CFR 164.308(a)(1)(ii)(A), is the violation. The attacker who encrypted the data did not create the legal exposure. The unexamined gap in the security program did.

These four bring OCR's Risk Analysis Initiative to 13 completed enforcement actions. The message from the agency has been consistent: you cannot protect ePHI you never accounted for, and OCR treats "we never looked" as its own offense.

## What is required in a HIPAA risk analysis?

The Security Rule does not hand you a template, and HHS has said repeatedly that it will not dictate a single methodology. But its guidance on risk analysis is specific about what a compliant one contains. At minimum:

- **Scope and asset inventory.** Every system, application, device, and location that creates, receives, maintains, or transmits ePHI. This is the step most small practices shortchange.
- **Data-flow mapping.** How ePHI enters your environment, moves through it, and leaves it, including transfers to business associates.
- **Threat and vulnerability identification.** The realistic threats to each asset and the weaknesses an attacker could exploit.
- **Assessment of current safeguards.** What you already have in place, and whether it works as intended.
- **Likelihood and impact.** A rating of how probable each risk is and how much damage it would cause, so you can prioritize.
- **Documentation.** A written record. If it is not written down, from OCR's perspective it did not happen.

That last point matters more than practices expect. When OCR opens an investigation, one of the first requests is for your most recent risk analyses, often the last five to six years of them. A verbal understanding of your risks is not a risk analysis.

## Where ePHI actually lives in 2026

![Two-column comparison of systems usually scoped in a HIPAA risk analysis versus the 2026 gap of AI tools, SaaS apps, cloud storage, and telehealth.](/blog/images/2-hipaa-ephi-scope-map-2026.png)

Here is where "thorough" has quietly changed. A risk analysis written three years ago probably covered the EHR, the practice email, the billing system, and the server in the back room. In 2026, that inventory is incomplete on its face, because patient data no longer stays in those four places.

Consider a common question practices are now searching: does a HIPAA risk analysis need to include AI tools? The answer follows directly from the rule. If a staff member pastes a patient summary into a consumer version of ChatGPT, Copilot, or Gemini to speed up a letter, that is ePHI leaving your environment into a system with no business associate agreement and, often, terms that allow the vendor to train on the input. That is an ePHI flow. If it is not in your risk analysis, your analysis is not thorough.

The same logic applies to the SaaS scheduling and intake apps a front desk signed up for, the cloud storage a clinician uses for convenience, and the telehealth and messaging platforms added during and after the pandemic. None of these are exotic. All of them touch ePHI. Most of them are missing from the risk analysis on file.

This is the gap that turns a ransomware incident into a settlement. The attacker gets in through the tool nobody scoped, because the tool nobody scoped is the tool nobody secured.

## Risk analysis versus risk management: doing it is not enough

OCR has drawn a second distinction that trips practices up. The risk analysis is the assessment. Risk management is what you do about the findings. In April 2026, OCR released a guidance video, "Risk Management Under the HIPAA Security Rule," precisely because so many organizations conduct an analysis, file it, and change nothing.

A risk analysis that identifies an unencrypted laptop and a missing MFA control, followed by no action to fix either, is not compliance. It is a documented admission. OCR expects to see that high risks were assigned owners and timelines, and that they were actually reduced. The analysis opens the loop. Risk management closes it.

## How often is a HIPAA risk analysis required?

The Security Rule does not set a fixed calendar interval. It requires the analysis to be ongoing and current. In practice, that means two things. Conduct a full analysis at least annually, which is the widely accepted baseline. And run an event-driven analysis whenever something material changes: a new EHR, a merger, a move to a new cloud service, a new AI or SaaS tool, or a security incident. The moment your technology footprint changes, last year's analysis is out of date.

## Do small practices need a HIPAA risk analysis?

Yes, and there is no small-practice exemption. A solo dental office and a hospital system face the same requirement. OCR has settled cases against practices of every size, and the corrective action plans read the same. The difference is resources, not obligation. A large system has a security team and a seven-figure budget. A ten-person clinic has neither, which is exactly why the risk analysis is the highest-leverage hour a small practice can spend: it tells you where the actual risk is before an attacker or an auditor does.

## What does OCR look for in a risk analysis?

Based on its published guidance and its enforcement pattern, OCR looks for comprehensive scope above all. An all-inclusive inventory of every system and location where ePHI lives. Evidence that you assessed threats and vulnerabilities against each, rated them, and prioritized. Proof that you acted on the high-risk findings. And a documented history showing the analysis is a living process, not a one-time file created the week before an audit. Thin scope is the fastest way to fail, and it is the failure the 2026 settlements have in common.

## What to do this quarter

You do not need to wait for the proposed rule to finalize. The work that protects you under the current rule is the same work that will position you for the new one.

- Rebuild your asset inventory from scratch and ask every team what tools they actually use, including the ones they adopted without IT.
- Add AI assistants, SaaS apps, cloud storage, and telehealth platforms to your ePHI data-flow map.
- Confirm you have a signed business associate agreement with every vendor that touches ePHI, and cut off the ones you cannot get one from.
- Rate your findings by likelihood and impact, assign owners and dates to the high risks, and track them to closure.
- Write all of it down, and schedule the next update now.

If you would rather work from a structured template than a blank spreadsheet, the [HIPAA Security Risk Assessment Tool: Excel + Guide](https://payhip.com/b/vXmYA) ($57) is the 9-tab fillable workbook and methodology guide built for exactly this. It maps the CFR safeguards, runs a 5x5 risk score, and produces a documented remediation plan and dashboard you can hand to an auditor. It is a working tool, not another PDF to read.

## Sources

- HHS Office for Civil Rights, "HHS' Office for Civil Rights Settles Four HIPAA Security Rule Ransomware Investigations," press release, April 23, 2026.
- HHS Office for Civil Rights, Guidance on Risk Analysis Requirements under the HIPAA Security Rule.
- 45 CFR 164.308(a)(1)(ii)(A), Security Management Process, Risk Analysis (eCFR).
- HHS Office for Civil Rights, "HIPAA Security Rule To Strengthen the Cybersecurity of Electronic Protected Health Information," Notice of Proposed Rulemaking, Federal Register, January 6, 2025 (90 FR 800).
- HHS Office for Civil Rights, "Risk Management Under the HIPAA Security Rule," guidance video, April 2026.
