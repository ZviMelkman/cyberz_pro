---
layout: post
title: "Do You Need GCC High for CMMC? Three Questions Your Contract Already Answers"
date: 2026-09-23
description: "Commercial Microsoft 365 cannot hold CUI. GCC can hold some of it. GCC High is the only Microsoft 365 tenant Microsoft backs for export-controlled data. What DFARS 252.204-7012, the DoD CMMC FAQs, and Microsoft's own compliance statements say, and the three questions that decide which tenant a small defense contractor actually needs."
category: CMMC
tags: [CMMC, GCC High, Microsoft 365 GCC, Microsoft 365 Commercial, CUI, DFARS 252.204-7012, FedRAMP, ITAR, EAR, NIST 800-171, defense contractors]
image: /blog/images/1-do-i-need-gcc-high-for-cmmc-hero.png
author: CyberZ
---

*Search "do I need GCC High for CMMC" and the top results disagree with each other on basic facts: whether GCC is FedRAMP Moderate or High, whether it satisfies DFARS 7012 at all, whether commercial Microsoft 365 is "fine if configured right." Many of those pages are written by companies that sell GCC High migrations. The answer is shorter than the argument, and most of it is already written into your contract.*

**You need Microsoft 365 GCC High if Controlled Unclassified Information that is export-controlled under ITAR or EAR will be stored, processed, or sent through Microsoft 365. If your CUI is not export-controlled, Microsoft 365 GCC meets the cloud-provider requirements of DFARS 252.204-7012, according to Microsoft's own February 2021 statement, though Microsoft itself says most defense contractors are better aligned with GCC High. Commercial Microsoft 365 cannot hold CUI under DFARS 7012, and the DoD CMMC FAQs state that encrypting CUI does not change that. If you handle only Federal Contract Information and no CUI, commercial Microsoft 365 is acceptable, because FAR 52.204-21 carries no FedRAMP requirement.**

<div class="key-takeaways" style="border-left:4px solid #EE4C48;background:#15151a;padding:18px 24px;margin:28px 0;border-radius:6px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;">
<li>The legal test lives in DFARS 252.204-7012(b)(2)(ii)(D): any cloud service that stores, processes, or transmits CUI must meet the FedRAMP Moderate baseline or its equivalent, and the provider must support the clause's incident reporting and forensics paragraphs (c) through (g).</li>
<li>Commercial Microsoft 365 fails that test. Microsoft's DFARS 7012 commitment names GCC and GCC High only.</li>
<li>GCC passes the DFARS 7012 cloud test, per Microsoft's February 2021 announcement. It does not carry a contractual commitment for export controls, because parts of the service, including the directory, are shared with the commercial cloud.</li>
<li>GCC High is the Microsoft 365 tenant Microsoft built for ITAR and EAR data, run on Azure Government with screened U.S. personnel.</li>
<li>Encryption is not a workaround. DoD CMMC FAQ E-Q2 answers "No" to storing encrypted CUI in a non-FedRAMP Moderate cloud.</li>
<li>Nothing in the Phase 2 suspension or the September 3 class deviation touched DFARS 7012. The cloud rule applies to every contract carrying that clause today.</li>
</ul>
</div>

## The rule that decides this is not CMMC

Most GCC High conversations start with CMMC, which is why they go in circles. The requirement that actually sorts Microsoft tenants comes from DFARS 252.204-7012, the clause that has been in defense contracts handling covered defense information since 2017.

Paragraph (b)(2)(ii)(D) says that if you use an external cloud service provider to store, process, or transmit covered defense information, you must "require and ensure" that the provider meets security requirements equivalent to the FedRAMP Moderate baseline, and that it complies with paragraphs (c) through (g) of the clause. Those paragraphs cover cyber incident reporting, malicious software, media preservation, access for forensic analysis, and damage assessment.

That is two tests, not one. The first is a security baseline. The second is a set of obligations the provider has to be willing to accept, because you cannot preserve images and hand over forensic data for a system someone else runs unless they have agreed to help.

CMMC inherits the same test. 32 CFR 170.17(c)(5) lets an organization use a cloud offering for CUI only if it is FedRAMP Authorized at Moderate or higher or meets equivalency under DoD policy. The mechanics of what "equivalent" means, and why the December 21, 2023 DoD CIO memo made it a 3PAO-assessed, zero-open-findings standard, are covered in the [external service provider guide]({% post_url 2026-07-12-cmmc-external-service-provider-requirements %}). For the Microsoft question, the useful point is simpler: the decision turns on 7012, and 7012 is in force whether or not a CMMC assessment is.

That matters right now. The July 13 memo suspended Phase 2, and the [September 3 class deviation]({% post_url 2026-09-10-cmmc-phase-2-class-deviation %}) directed contracting officers to remove third-party CMMC assessment requirements from contracts. Neither instrument amends DFARS 7012. A contractor that paused its GCC High migration because "CMMC is on hold" paused the wrong thing.

## What each Microsoft 365 tenant actually is

Microsoft sells three Microsoft 365 environments that matter to a defense contractor. A fourth, the DoD tenant, is only for DoD itself and approved entities, so it is out of this discussion.

**Microsoft 365 Commercial** is the tenant nearly every small business starts on. Microsoft's own public-sector compliance explainer, written by its aerospace and defense lead on the Microsoft Tech Community blog, marks Commercial as "No" for CUI and describes support for the 7012 (c) through (g) paragraphs as "much less tenable" there, citing differences in log retention, incident response times, and a global support model. When Microsoft announced DFARS 7012 support in February 2021, the announcement covered GCC and GCC High. Commercial was not on it.

**Microsoft 365 GCC** (Government Community Cloud) is a U.S.-resident data enclave of the commercial cloud. Core workloads such as Exchange Online, SharePoint, OneDrive, and Teams keep customer data in the continental U.S. and are administered by screened personnel. In its February 2021 announcement, Microsoft stated that GCC and GCC High "both meet the applicable requirements" of DFARS 252.204-7012 for cloud providers and that it will accept the flow-down terms that apply to CSPs. The same announcement adds a caution in Microsoft's own words: meeting the CSP requirements "will not be the decision factor" by itself, and most defense contractors are best aligned with GCC High for CUI.

The reason is structural. Some services in GCC, including the directory, are shared with the commercial cloud and can be processed outside the U.S. and supported by global staff. For that reason, Microsoft's explainer states, it will not contractually commit to export controls in GCC.

**Microsoft 365 GCC High** runs on Azure Government, a separate sovereign cloud with its own directory, U.S.-only data centers, and screened U.S. personnel. It is the environment Microsoft built for ITAR and EAR data, and Microsoft's public-sector blog documents its DFARS 7012 support there as well.

![Which Microsoft 365 tenant can hold CUI under DFARS 252.204-7012: Commercial cannot hold CUI, GCC can hold CUI that is not export-controlled, GCC High can hold CUI including ITAR and EAR data](/blog/images/2-microsoft-365-commercial-gcc-gcc-high-cui.png)

## Why the search results contradict each other

A reader comparing vendor pages will find GCC described as FedRAMP Moderate on one and FedRAMP High on the next, and "not DFARS compliant" on a third. Three things explain most of it.

First, pages age badly. Microsoft's GCC DFARS announcement is from February 2021. Content written before it, or copied from content written before it, still says GCC cannot meet 7012.

Second, "FedRAMP High" is not the deciding fact. DFARS 7012 asks for Moderate or equivalent. A tenant can clear that bar and still be the wrong choice because of what your data is, which is the export-control question below.

Third, a lot of the ranking content is published by resellers and MSPs whose business is GCC High licensing and migration. That does not make them wrong. Microsoft's own position leans the same way. It does mean the "everyone needs GCC High" framing deserves a check against your actual contract before you sign a multi-year license.

## The three questions, in order

The tenant decision is a scoping decision first and a licensing decision second. Ask these three questions in order and stop at the first one that settles it.

### 1. Will CUI ever touch Microsoft 365?

Not "do we have CUI." Will it be in email, Teams chats, SharePoint, or OneDrive, including as an attachment someone forwards without thinking.

If you hold only Federal Contract Information under FAR 52.204-21 and your contracts carry no 7012 obligation for CUI, commercial Microsoft 365 is acceptable. FAR 52.204-21 lists 15 basic safeguarding requirements and says nothing about FedRAMP. That is the CMMC Level 1 population, and it is a large share of small suppliers.

If you do hold CUI, there is a legitimate option that keeps it out of Microsoft 365 entirely: a separate, FedRAMP-authorized CUI enclave for the files and communications that need protection, with the rest of the business staying on commercial. It only works with discipline, because the moment a drawing goes out through commercial Exchange, your commercial tenant is holding CUI. The [scoping guide]({% post_url 2026-07-19-cmmc-scoping-decision-not-controls %}) covers how enclaves shrink assessment scope, and how they fail. If you cannot say with confidence where CUI flows today, answer that before you answer the licensing question. The [unmarked CUI piece]({% post_url 2026-08-30-unmarked-cui-liability %}) explains why "we don't think we have any" is a weak position.

### 2. Is any of that CUI export-controlled?

This is the question that separates GCC from GCC High. Technical data covered by ITAR (22 CFR Parts 120 to 130) or by EAR is a category of CUI with an additional rule attached: who can access it, and where it is stored, is itself regulated.

Microsoft will commit contractually to export controls in GCC High. It will not in GCC. So if drawings, specifications, or technical data your prime sends you are marked with an ITAR or EAR notice, and that data will sit in Microsoft 365, GCC High is the Microsoft answer.

Two nuances are worth knowing. The ITAR end-to-end encryption rule at 22 CFR 120.54(a)(5) says that sending or storing unclassified technical data is not an export if it is end-to-end encrypted with FIPS 140-2 validated modules (or comparable 128-bit strength) and not sent to or stored in a proscribed country. That rule is about exports. It does not make CUI stop being CUI. The DoD CMMC FAQs address this directly: B-Q8 states that encrypted CUI is still CUI, and E-Q2 answers "No" to the question of whether a non-FedRAMP Moderate cloud can store encrypted CUI. An encrypted enclave can work, but the enclave service itself still needs FedRAMP Moderate or equivalency.

The second nuance: many small contractors do not know whether they hold export-controlled data. Read the markings on what your prime actually sends you and ask the prime's contracts or export compliance contact directly. The answer is usually on the document.

### 3. What does your prime's flow-down actually say?

The regulation sets a floor. Your subcontract can set a higher one. Some primes specify the environment they expect their suppliers to use, or require a GCC High tenant for specific programs. Others accept GCC or a FedRAMP-authorized enclave. Read the cybersecurity and export-control sections of the subcontract and the supplier portal requirements before you decide, not after.

If the flow-down is silent and your CUI is not export-controlled, GCC is a defensible choice under 7012. If the flow-down names GCC High, the question is closed.

![The three questions that decide whether a defense contractor needs GCC High: will CUI touch Microsoft 365, is any of it ITAR or EAR export-controlled, and what does the prime's flow-down require](/blog/images/3-gcc-high-cmmc-three-questions.png)

## What the choice costs you beyond the license

The license price is the number people argue about. The operational costs are the ones that surprise them.

**It is a new tenant, not an upgrade.** GCC High lives in Azure Government, so moving there means a tenant migration: mailboxes, SharePoint sites, OneDrive, Teams, identities, and devices. Microsoft also validates eligibility before it sells a government tenant, which adds time up front.

**Features lag.** Some commercial features arrive later in GCC High or arrive reduced. The [AI tools and CUI post]({% post_url 2026-08-04-ai-tools-cui-compliance %}) covered one example: Microsoft 365 Copilot in a commercial tenant is not a CUI answer, and the GCC High version is a separate offering with a separate timeline. Check that the apps and integrations your team depends on exist in the target environment before you commit.

**Being on GCC High is not compliance.** The tenant covers Microsoft's side of the shared responsibility model. Your side, configuration, access control, logging, MFA, device management, and the SSP that describes all of it, is still yours. A contractor on GCC High with a thin SSP is in the same position as one on GCC with a thin SSP. The [SSP template post]({% post_url 2026-06-09-cmmc-ssp-template %}) covers what an assessor reads for the cloud boundary.

**Whatever you pick goes in your SSP.** The tenant, the services in use, and the FedRAMP status you are relying on belong in your system boundary description and asset inventory. If you are using GCC, the SSP should say why, which usually means stating that your CUI does not include export-controlled data and how you know.

## What a 20-person subcontractor should do this month

1. **List every place CUI lands today.** Email, file shares, Teams, laptops, the engineering workstation, the MSP's tools. Mark each one as holding CUI, holding security data only, or neither.
2. **Pull the markings on the last ten technical documents your prime sent.** If any carry an ITAR or EAR notice, you have export-controlled CUI and question two is answered.
3. **Find the tenant type you are on now.** Your Microsoft 365 admin center or your MSP can tell you in minutes. If it is Commercial and CUI is in it, that is a current 7012 problem, not a CMMC-future problem.
4. **Read the subcontract's cybersecurity and export sections.** Write down any environment the prime names.
5. **Decide between three paths,** stated in one sentence each in your SSP: commercial plus a FedRAMP-authorized CUI enclave, GCC for non-export-controlled CUI, or GCC High for everything. Then scope and price the migration, not the other way around.

## The bottom line

Commercial Microsoft 365 is out the moment CUI touches it. GCC is a legitimate DFARS 7012 answer for CUI that is not export-controlled, and Microsoft has said so in writing since 2021. GCC High is the answer when ITAR or EAR data is in the mix, or when your prime says so. The Phase 2 suspension did not move any of this, because the rule was never CMMC's to begin with.

The expensive mistake is not picking the wrong tenant. It is picking one before you know where your CUI goes. If that map does not exist yet, the [CMMC Level 2 Asset Scoping Worksheet for NIST 800-171](https://payhip.com/b/2nzjO) ($47) sorts each asset into the 32 CFR 170.19 categories and gives you the scope summary this decision depends on. If the tenant decision is going to rewrite your SSP boundary, your asset inventory, and your SPRS score in the same quarter, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) keeps the scoping worksheet, SSP, evidence tracker, POA&M, and score workbook pointed at one set of facts.

## Sources

- DFARS 252.204-7012, Safeguarding Covered Defense Information and Cyber Incident Reporting, paragraph (b)(2)(ii)(D) and paragraphs (c) through (g)
- 32 CFR § 170.17(c)(5) and § 170.19, CMMC Program (eCFR)
- FAR 52.204-21, Basic Safeguarding of Covered Contractor Information Systems
- DoD CIO, Memorandum, "Federal Risk and Authorization Management Program (FedRAMP) Moderate Equivalency for Cloud Service Provider's (CSP) Cloud Service Offerings (CSO)," December 21, 2023
- DoD CIO, CMMC Frequently Asked Questions, B-Q8 and E-Q2
- 22 CFR § 120.54(a)(5), ITAR, activities that are not exports (end-to-end encryption)
- Microsoft Tech Community, Public Sector Blog, "Microsoft Expands Support for the DIB: Announcing Support for DFARS in Microsoft 365 Government," February 2021
- Microsoft Tech Community, Public Sector Blog, "Understanding Compliance Between Microsoft 365 Commercial, GCC, GCC-High and DoD Offerings"
- Microsoft Tech Community, Public Sector Blog, "Support for DFARS in Microsoft 365 Government (GCC High)," 2024
- Class Deviation 2026-O0025, Revision 3, September 3, 2026 (as covered in the September 10 CyberZ post)

