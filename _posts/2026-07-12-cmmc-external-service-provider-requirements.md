---
layout: post
title: "CMMC External Service Provider Requirements: Does Your MSP Need to Be Certified?"
description: "Your MSP does not need its own CMMC certification, but its services get assessed inside your assessment. What 32 CFR 170 requires of ESPs, CSPs, and the contractors who hire them."
image: /blog/images/1-cmmc-external-service-provider-hero.png
---

*Every defense contractor with an outsourced IT provider eventually asks the same question: does my MSP need to be CMMC certified? The answer the final rule gives is short. What it means for your assessment is not.*

**An External Service Provider (ESP) under CMMC is external people, technology, or facilities a contractor uses for IT or cybersecurity services, where CUI or Security Protection Data is processed, stored, or transmitted on the provider's assets (32 CFR 170.4). Under the final rule, an ESP that is not a cloud service provider does not need its own CMMC certification. Instead, its services are assessed within the scope of your assessment, against all 110 Level 2 requirements, and the relationship must be documented in your SSP and a customer responsibility matrix (32 CFR 170.17).**

<div class="key-takeaways" style="background:#0D0D0F;border-left:4px solid #EE4C48;padding:1.2em 1.5em;margin:1.5em 0;color:#fff;">
<strong style="color:#EE4C48;">Key Takeaways</strong>
<ul style="margin-top:0.6em;">
<li>Your MSP does not need its own CMMC certification. The December 2023 proposed rule would have required it; the final rule published October 15, 2024 dropped the requirement.</li>
<li>The requirement did not disappear. If your MSP touches CUI, its services are assessed inside your assessment against all 110 requirements, on your timeline and your invoice.</li>
<li>Cloud services holding CUI are the exception: FedRAMP Moderate authorization or DoD-recognized equivalency, with no CMMC substitute.</li>
<li>Providers that hold only Security Protection Data (your SIEM, MDR, or backup vendor) are assessed as Security Protection Assets.</li>
<li>Every in-scope provider must appear in your SSP with a customer responsibility matrix. Missing paperwork is a finding you hand your assessor on day one.</li>
</ul>
</div>

## The answer, and why it is not the relief it sounds like

The December 2023 proposed rule said the quiet part loudly: if a contractor used an external service provider other than a cloud service provider, that ESP needed its own CMMC Level 2 certification. MSPs across the defense industrial base priced out assessments. Contractors braced for provider fees to jump.

Then the final rule, published October 15, 2024 and effective December 16, 2024, removed the requirement. No separate certification for MSPs or MSSPs.

What replaced it matters more than what was removed. Under 32 CFR 170.17, when you use an ESP that is not a CSP to process, store, or transmit CUI, three conditions apply: the relationship and services must be documented in your SSP and described in the ESP's service description and customer responsibility matrix, the ESP services used to meet your requirements are assessed within the scope of your assessment against all Level 2 security requirements, and your own on-premises infrastructure connecting to the ESP's service is in scope and will also be assessed.

Read that middle condition again. The provider's services do not get a lighter look. They get the full 110-requirement examination, inside your assessment, consuming your assessor hours. DoD did not delete the work. It moved the bill from your MSP to you.

## What actually counts as an external service provider

The definition has a gate most coverage skips. Under 32 CFR 170.4, a provider is only an ESP if CUI or Security Protection Data is processed, stored, or transmitted on the provider's assets. No CUI, no SPD, no ESP.

DoD's own Level 2 Scoping Guide makes the point directly: not every company that provides services to a contractor is an ESP. Cloud-based HR and accounting applications typically do not contribute to the security of your environment, hold SPD, or touch CUI. Your payroll SaaS is not in your CMMC scope, and treating it as if it were wastes prep effort you need elsewhere.

Security Protection Data is the term that trips people. Per 170.4, SPD is data stored or processed by Security Protection Assets that is used to protect your assessed environment: configuration data, log files generated or ingested by a security tool, vulnerability status data, and passwords granting access to the in-scope environment. Your MDR provider never sees a contract drawing, but it ingests your logs all day. That is SPD, and it puts the provider in scope.

![CMMC ESP scope decision tree]({{ site.baseurl }}/blog/images/2-cmmc-esp-scope-decision-tree.png)

So the sorting question for every provider on your vendor list is not "do they do IT for us?" It is "does CUI or SPD sit on their assets?" Three outcomes follow:

The provider touches CUI on non-cloud infrastructure: it is an ESP, assessed inside your assessment against all 110 requirements. The provider holds only SPD: its service is treated as a Security Protection Asset and assessed against the requirements relevant to the capabilities it provides. The provider touches neither: it is not an ESP at all, and your SSP should record why it is excluded so the question dies in the first hour of your assessment instead of the last.

## Does my MSP get assessed in my CMMC assessment?

Yes, if it is in scope, and this is where contractor and provider incentives quietly diverge.

When your C3PAO shows up, the assessment team examines, interviews, and tests against NIST SP 800-171A objectives. For every requirement your MSP performs on your behalf (patching, account provisioning, firewall management, log review), the evidence has to come from somewhere, and the responsibility split has to be unambiguous. If your MSP administers your identity provider, the assessor will want to see how MFA is enforced, who holds privileged accounts, and how the MSP's own access into your environment is controlled. The MSP's remote access tooling is a Security Protection Asset. Its technicians are, functionally, your privileged users.

The rule offers providers an off-ramp: 32 CFR 170.19(c)(2) notes an ESP may voluntarily undergo its own CMMC certification assessment to reduce the effort required during the customer's assessment. Some MSPs serving the defense market are doing exactly that, because being re-examined inside every client's assessment does not scale. If your provider has voluntarily certified, your assessment gets simpler. If it has not, plan for your assessor to spend real time on the provider relationship, and plan for your MSP to be available during assessment week.

One prime-facing note: the flow-down letters we covered in [what your prime is actually accepting]({% raw %}{% post_url 2026-06-08-what-your-prime-is-actually-accepting-cmmc %}{% endraw %}) increasingly ask subs how their providers are handled. "Our MSP is dealing with it" is not an answer a prime's supplier risk team accepts anymore.

## The cloud exception: FedRAMP is non-negotiable

Everything above applies to ESPs that are not cloud service providers. The moment CUI sits in a cloud service offering, a different rule takes over.

A CSP that processes, stores, or transmits CUI must hold FedRAMP Moderate authorization or meet equivalency as defined in DoD's December 2023 FedRAMP equivalency memo. This traces to DFARS 252.204-7012(b)(2)(ii)(D) and is carried through the CMMC rule. There is no CMMC certificate a cloud provider can earn that substitutes for it, and equivalency is not a handshake: the memo requires a body of evidence assessed by a FedRAMP-recognized third party.

The practical test: check the FedRAMP Marketplace for your vendor's offering before you sign, and confirm the specific service you use is the one authorized. A CSP holding only your SPD, and no CUI, does not trigger the FedRAMP requirement; it is treated as a Security Protection Asset like any other security tooling.

![ESP and CSP requirements comparison table]({{ site.baseurl }}/blog/images/3-cmmc-esp-csp-requirements-table.png)

## The paperwork: your SSP and the responsibility matrix

Both 170.17 and 170.19(c)(2) converge on the same two documents. Your SSP must document the use of each ESP, its relationship to you, and the services provided. And each provider relationship needs a customer responsibility matrix (CRM), the rule's term for what the market calls a shared responsibility matrix: a requirement-by-requirement statement of who does what, you or the provider.

This is the artifact assessors ask for early, because it is the map for the entire provider portion of the assessment. A CRM that says "MSP handles security" is not a CRM. The usable version walks the 110 requirements and marks each one: contractor, provider, or shared, with the provider's half backed by its service description. If your MSP cannot produce its side of the matrix, you have learned something important about the provider before the assessment did.

## What to do about it this week

Pull your vendor list and sort every provider through the three-outcome test above: CUI on their assets, SPD only, or neither. Document the "neither" exclusions in your SSP in a sentence each. For every cloud service holding CUI, verify FedRAMP Moderate authorization or documented equivalency now, because swapping a non-compliant platform takes months you do not have before the November 10, 2026 Phase 2 date. For your MSP, request its service description and its half of the customer responsibility matrix this week, and ask directly whether it plans to pursue voluntary CMMC certification. The answer changes how much of your assessment budget the provider relationship will consume.

The sorting exercise is exactly what the [CMMC Level 2 Asset Scoping Worksheet for NIST 800-171](https://payhip.com/b/2nzjO?ref=blog) ($47) automates: answer a few questions per asset or provider and it lands each one in the right category under 32 CFR 170.19, flagging what is missing from your SSP. The SSP documentation itself, including where the ESP relationships and CRM references live, is structured in the [CMMC Level 2 System Security Plan (SSP) Template](https://payhip.com/b/gB6oD?ref=blog) ($77).

## FAQ

**Does my MSP need to be CMMC compliant?**
It does not need its own CMMC certification. But if it processes, stores, or transmits CUI or SPD on its assets, its services are assessed inside your assessment, so its practices must hold up against the same requirements.

**What is considered an external service provider in CMMC?**
External people, technology, or facilities you use for IT or cybersecurity services, where CUI or Security Protection Data resides on the provider's assets (32 CFR 170.4). A vendor that touches neither is not an ESP.

**Does my MSP get assessed in my CMMC assessment?**
If in scope, yes. Its services are assessed within your assessment (32 CFR 170.17), your connecting infrastructure is in scope, and the split of duties must be documented in a customer responsibility matrix.

**Does CMMC require FedRAMP?**
Only for cloud service offerings handling CUI: FedRAMP Moderate authorization or equivalency per DoD's December 2023 memo. Non-cloud ESPs and SPD-only cloud tools do not carry the FedRAMP requirement.

**Can my MSP get CMMC certified anyway?**
Yes, voluntarily, and 32 CFR 170.19(c)(2) notes this reduces the effort during your assessment. Many defense-focused MSPs are pursuing it so they are not re-examined inside every client's assessment.

## Sources

- 32 CFR Part 170, Cybersecurity Maturity Model Certification (CMMC) Program, 89 FR 83214 (Oct. 15, 2024): [ecfr.gov](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170)
- 32 CFR 170.17, Level 2 certification assessment requirements (ESP and CSP conditions): [ecfr.gov](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.17)
- 32 CFR 170.19, CMMC scoping (asset categories, ESP table, CRM requirement): [ecfr.gov](https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.19)
- DoD CMMC Scoping Guide, Level 2, v2 (ESP examples, SPA/SPD guidance): [dodcio.defense.gov](https://dodcio.defense.gov/Portals/0/Documents/CMMC/ScopingGuideL2v2.pdf)
- DFARS 252.204-7012, Safeguarding Covered Defense Information (cloud/FedRAMP Moderate requirement)
