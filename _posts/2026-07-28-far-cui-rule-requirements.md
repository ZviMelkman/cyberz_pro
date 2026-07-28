---
layout: post
title: "FAR CUI Rule Requirements: What the June 2026 Revision Actually Changed"
date: 2026-07-28
description: "The FAR CUI proposed rule was rewritten in June 2026. Reporting moved to 72 hours, the training mandate came out, and unmarked CUI stopped being an incident. Verified against 91 FR 37550."
category: CMMC
tags: [CUI, FAR, NIST 800-171, compliance, defense contractors, federal contractors]
image: /blog/images/1-far-cui-rule-changes-hero.png
author: CyberZ
---

*Search the FAR CUI rule today and the first page will tell you that you have eight hours to report an incident and that you must run a specific employee training program. Both statements were true in January 2025. Neither survived the June 2026 rewrite.*

**The FAR CUI rule is a proposed governmentwide framework for safeguarding Controlled Unclassified Information under federal contracts. Its current version was published June 23, 2026 at 91 FR 37550 as part of FAR Case 2026-001, and it would add two new clauses: FAR 52.240-6, a solicitation notice, and FAR 52.240-7, the contract clause carrying the obligations. It replaces the January 15, 2025 proposal at 90 FR 4278. The June version moved CUI incident reporting to 72 hours from discovery, removed the mandated training requirement, removed the contractor liability language, and narrowed what counts as a CUI incident.** It is still a proposal. Comments closed July 23, 2026, and nothing in it binds you until a final rule issues and the clause appears in one of your contracts.

<div class="key-takeaways" style="background:#16161a;border-left:4px solid #EE4C48;padding:20px 24px;margin:24px 0;">
<strong>Key Takeaways</strong>
<ul>
<li>The operative document is FAR Case 2026-001, published at 91 FR 37550 on June 23, 2026. The older FAR Case 2017-016 (90 FR 4278, January 15, 2025) was folded into it, which is why so much published guidance describes requirements that no longer exist.</li>
<li>CUI incident reporting is 72 hours from discovery, not 8. The FAR Council changed it in response to comments and to align with DFARS 252.204-7012 and the Cyber Incident Reporting for Critical Infrastructure Act of 2022.</li>
<li>The specific employee training mandate was removed. So was the contractor liability language, and the separate clause on potentially unmarked CUI, FAR 52.240-YY.</li>
<li>Unmarked or mismarked CUI is no longer a CUI incident by itself. It only becomes one if the mishandling caused unauthorized disclosure, improper modification, or improper destruction.</li>
<li>A cloud provider that stores, processes, or transmits your CUI must meet security requirements equivalent to the FedRAMP Moderate baseline.</li>
<li>The SF XXX identifies organizationally defined parameters for NIST SP 800-171 Revision 3, not Revision 2.</li>
<li>An endpoint running a properly configured virtual desktop client is called an out-of-scope asset in the clause text. That is a scoping decision with real cost consequences.</li>
<li>The CMMC Phase 2 suspension did nothing to this rule. Contractors selling to civilian agencies were never inside CMMC to begin with.</li>
</ul>
</div>

## What is the FAR CUI rule, and what changed on June 23, 2026?

CUI has been an unfinished project for most of two decades. The National Archives and Records Administration runs the CUI program, and the FAR CUI rule is the acquisition system's attempt to implement NARA's final rule as it applies to performance under federal contracts. Until now the FAR has had no consistent way to tell a contractor which sensitive information a contract involves or how to protect it. Defense contractors got DFARS 252.204-7012. Everyone else got whatever their agency improvised.

The FAR Council first proposed a fix on January 15, 2025 at 90 FR 4278. Respondents commented. On June 23, 2026 the Council published a substantially rewritten version as part of the Revolutionary FAR Overhaul, at 91 FR 37550, under FAR Case 2026-001 and RIN 9000-AO86. The notice runs 85 pages, from 37550 to 37634. Comments closed July 23, 2026, and the rule's docket shows 88 of them.

Two things about that history matter more than they should.

First, the case number changed. The CUI work was FAR Case 2017-016 for nine years. It is now inside FAR Case 2026-001, alongside revisions to FAR parts 1, 2, 4, 33, 39, 40, 52 and 53. Anyone tracking the old case number saw the trail go cold.

Second, the requirements moved in the direction almost nobody expected. The June version asks less than the January 2025 version did, in several specific and checkable ways.

![Comparison table showing six FAR CUI rule requirements that changed between the January 2025 and June 2026 proposed rules, including reporting moving from 8 hours to 72 hours and the training requirement being removed.](/blog/images/2-far-cui-rule-january-2025-vs-june-2026-changes.png)

## Why does so much FAR CUI rule coverage still say eight hours?

Because it was written about the January 2025 draft and never revised.

This is worth naming plainly, because it is a live problem for anyone researching the topic right now. The eight-hour figure, the mandated training program, and the separate obligation to report potentially unmarked CUI all come from the earlier proposal. The June 2026 revision changed or deleted every one of them. Search engine results, summary articles, vendor explainers and AI-generated overviews are still reproducing the old version, sometimes with confident specificity.

The FAR Council's own explanation of the reporting change is direct. Multiple respondents commented on the timeline. Based on those comments, the Council reset it to 72 hours from discovery, both to align with related requirements like DFARS 252.204-7012 and the Cyber Incident Reporting for Critical Infrastructure Act of 2022, and to give contractors enough time to provide accurate information and work out whether the event even qualifies as a CUI incident.

If you are comparing vendor guidance, that alignment is the tell. Any document describing an eight-hour federal CUI reporting clock predates June 23, 2026.

## Does the FAR CUI rule apply to my contract?

The answer runs through a form, not a revenue threshold or an industry code.

Under the proposal, when a contract involves CUI the contracting officer completes a Standard Form XXX, Controlled Unclassified Information Requirements. The SF XXX identifies whether CUI is involved, which categories, where it will reside, and which safeguarding and reporting requirements apply. The solicitation carries FAR 52.240-6 as notice. The contract carries FAR 52.240-7 as the clause that actually obligates you.

No CUI identified means no SF XXX, and the CUI clauses are not prescribed.

Two boundaries are worth knowing. Both FAR 52.240-6 and 52.240-7 are proposed to apply to commercial products and commercial services, but not to commercially available off-the-shelf items. And the flow-down at FAR 52.240-7(g) was clarified so that you are not required to hand a subcontractor the SF XXX or a modified version of it. You decide how best to pass the requirements down to a subcontractor that will receive the CUI.

![Three-step decision graphic on FAR CUI rule applicability: whether CUI is identified on the SF XXX, whether the acquisition is solely COTS items, and whether a subcontractor will receive the CUI.](/blog/images/3-does-far-cui-rule-apply-to-me.png)

The reason this matters for civilian-agency contractors is that it is the first time the question has had a clean answer. A firm doing work for HHS or GSA that handles sensitive but unclassified government information has spent years guessing at its obligations. Under this framework, the guessing is supposed to end at the form.

## Which NIST standard does the FAR CUI rule require, Revision 2 or Revision 3?

Revision 3.

This is the single most consequential detail in the rule for anyone who has already done NIST SP 800-171 work, and it deserves care because the two revisions are not interchangeable. The proposed rule updated the SF XXX to identify the applicable organizationally defined parameters for NIST SP 800-171 Revision 3. Organizationally defined parameters are the values Revision 3 leaves for the customer to set, and the Council's stated purpose is to fix them centrally so contractors follow one standard across agencies rather than a different set per customer. The rule says those values align to what will be codified in 32 CFR part 170 through DoD rulemaking.

Set that next to CMMC. The CMMC assessment baseline has been Revision 2. We wrote about the transition question in [NIST 800-171 Rev 2 or Rev 3 for CMMC?]({% post_url 2026-07-08-nist-800-171-rev-3-cmmc-transition %}) when it looked like a defense-side timing problem. It is now arriving from a second direction, through the FAR, for a much larger population of contractors.

There is a related provision on enhanced controls. NIST SP 800-172 requirements would apply only where an agency identifies them for a critical program or a high-value asset, aligned with the values at 32 CFR 170.14. That is a narrower trigger than some earlier commentary implied.

## What counts as a CUI incident now, and what no longer does?

The definition was narrowed, and the narrowing is specific.

A CUI incident means unauthorized disclosure, improper modification, or improper destruction of CUI in any form or medium, or unauthorized access to the information system on which the CUI resides. The rule then adds a clarification that improper handling of CUI, and it names unmarked or mismarked CUI as the example, is not a CUI incident unless that improper handling actually resulted in unauthorized disclosure, improper modification, or improper destruction.

The related clause has been deleted outright. FAR 52.240-YY, Identifying and Reporting Information That Is Potentially Controlled Unclassified Information, is gone from the June version. Reporting unmarked or mismarked CUI still exists as an obligation, and its timeframe was extended to 72 hours from discovery, but finding a badly marked document is no longer an incident report waiting to happen.

Two more removals belong in the same list, because both were sources of real anxiety in the 2025 draft. The language specifying contractor liability for CUI incidents was removed. So were the compliance and validation provisions that addressed government access to contractor facilities and systems, on the reasoning that normal contract administration procedures are enough to validate compliance.

For defense contractors, note the asymmetry. Government access to your systems still exists on the DFARS side, which we covered in [How to Prepare for a DIBCAC Assessment]({% post_url 2026-07-26-dibcac-assessment-preparation %}). It is the FAR version that came out.

## Where does a 72-hour CUI incident report actually go?

Three different places, depending on the contract and on who else already reported.

For Department of Defense contracts, the reporting location is dibnet.dod.mil. For non-DoD contracts it is CISA, at cisa.gov/reporting-cyber-incident. In both cases you also notify the contracting officer that a report has been submitted.

There is a genuine exception for cloud. If a CUI incident involves a FedRAMP authorized cloud computing service provider that has reported the incident under the FedRAMP Incident Communication Procedures, you are not required to submit any additional report beyond following those procedures.

Subcontractor reporting was rewritten. A subcontractor reports directly to the government, then notifies the contracting officer and the next higher tier contractor, under FAR 52.240-7(e)(2).

And the first report is explicitly allowed to be incomplete. You submit as many of the applicable data elements as you have at the time. If the first report is missing elements, or information changes once the investigation is substantially complete, you submit a subsequent report with the updates.

![Flow graphic showing the FAR CUI 72-hour reporting clock from discovery, with three destinations: DIBNet for DoD contracts, CISA for non-DoD contracts, and no second report where a FedRAMP authorized provider already reported.](/blog/images/4-far-cui-incident-reporting-72-hours.png)

One more provision is easy to miss and useful to know. A new paragraph (f) in FAR 52.240-7 would require you to notify the contracting officer within 72 hours of determining that you cannot comply with a requirement in the clause because it conflicts with another law or regulation. That is a route to alternative controls rather than a violation, which matters for firms operating under foreign data laws.

## What does the rule require of a cloud provider holding your CUI?

If you use a cloud service provider to store, process, or transmit any CUI identified in the SF XXX, that provider must meet security requirements equivalent to those the government has established for the FedRAMP Moderate baseline.

Read the word equivalent carefully. It is not the same as requiring a FedRAMP authorization, and the Council describes the choice as giving contractors more flexibility while still getting the controls implemented. In practice it moves the question from a marketplace listing to a documentation exercise, and it is the kind of question small firms tend to answer optimistically about tools they already pay for.

The scoping consequences are where the money is. The clause text at FAR 52.240-7(d)(3)(ii)(A) treats an endpoint hosting a virtual desktop infrastructure client as an out-of-scope asset, provided the client is configured to prevent any processing, storage, or transmission of CUI beyond the keyboard, video and mouse traffic sent to it. The same paragraph exempts commercial communications networks that carry government and non-government information using the same equipment, protocols and methods without regard to source or recipient.

Those are not footnotes. They are the difference between a handful of in-scope assets and an enterprise-wide problem, which is the argument we made in [Why Your CMMC Timeline Is a Scoping Decision, Not a Controls Problem]({% post_url 2026-07-19-cmmc-scoping-decision-not-controls %}). Getting an asset inventory and a boundary written down before a clause arrives is the cheapest work available. Our [CMMC Level 2 Asset Scoping Worksheet for NIST 800-171](https://payhip.com/b/2nzjO) ($47) walks that categorization with the CUI, security protection, contractor risk managed, specialized and out-of-scope buckets.

## Did the CMMC pause change any of this?

No, and the two events are unrelated in a way that is easy to get wrong.

The Department suspended CMMC Phase 2 on July 13, 2026, which paused third-party certification. We covered what did and did not change in [Is CMMC Still Required?]({% post_url 2026-07-19-is-cmmc-still-required %}). That suspension is a Department of Defense action about who assesses defense contractors.

The FAR CUI rule is a FAR Council action about what every federal contractor handling CUI must do. It was published ten days before the CMMC suspension and is unaffected by it. A firm with both defense and civilian work gets no relief on the civilian side from anything the Department did in July.

If you follow FAR clause numbering, this all sits inside the same reorganization that renumbered FAR 52.204-21 to 52.240-93 and moved the DFARS assessment clause, which we unpacked in [DFARS 7019 Is Gone. Do You Still Need an SPRS Score?]({% post_url 2026-06-16-dfars-7019-deleted-sprs-score %}). FAR Part 40 is being reorganized into three subparts: Processing Supply Chain Risk Information, Security Prohibitions and Exclusions, and Safeguarding Information. CUI lives in the third.

## What should a small contractor do before a final rule lands?

The rule does not state an implementation timeline, and it is worth being honest that nobody outside the Council knows the date. Hunton Andrews Kurth reads the Council's schedule as aiming to finalize the Revolutionary FAR Overhaul rules, CUI included, before the end of 2026. Treat that as a law firm's estimate, not a government commitment.

Four pieces of work hold their value regardless of what the final rule says.

Write down where CUI actually lives, not where policy says it lives. Email, file shares, laptops, the cloud tools people signed up for themselves. Applicability turns on identified CUI, and you cannot answer a contracting officer's SF XXX intelligently without knowing your own footprint.

Check your cloud stack against FedRAMP Moderate equivalence, in writing, per tool. For most small firms the answer will be uncomfortable for at least one tool they rely on.

Read Revision 3 rather than assuming Revision 2 carries forward. If you scoped and scored against Revision 2, the gap is real work.

Know your reporting path before you need it. DIBNet or CISA, who notifies the contracting officer, and what goes in a first report when you have almost nothing. Seventy-two hours is generous next to eight and short next to how long it takes to reach the right person on a Friday.

For firms doing the Revision 2 to Revision 3 gap work with an assessment or a customer questionnaire in front of them, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) bundles the scoping, scoring, SSP and evidence pieces in one place. It is built for the moment a prime or a contracting officer asks for documentation you have not written yet.

## Sources

- Federal Acquisition Regulation: Revolutionary Federal Acquisition Regulation Overhaul Parts 1, 2, 4, 33, 39, 40, and 53 — 91 FR 37550, FAR Case 2026-001, Docket No. FAR-2026-0001, RIN 9000-AO86, proposed rule published June 23, 2026, federalregister.gov
- Federal Acquisition Regulation: Controlled Unclassified Information — 90 FR 4278, FAR Case 2017-016, proposed rule published January 15, 2025, federalregister.gov
- NIST SP 800-171 Revision 3, Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations — csrc.nist.gov
- NIST SP 800-172, Enhanced Security Requirements for Protecting Controlled Unclassified Information — csrc.nist.gov
- 32 CFR Part 170, Cybersecurity Maturity Model Certification Program — ecfr.gov
- DFARS 252.204-7012, Safeguarding Covered Defense Information and Cyber Incident Reporting — acquisition.gov
- Cyber Incident Reporting for Critical Infrastructure Act of 2022 — cisa.gov
- FAR Council Releases Updated CUI Proposed Rule as Part of the Revolutionary FAR Overhaul — Hunton Andrews Kurth LLP, hunton.com (cited for the finalization estimate only)
