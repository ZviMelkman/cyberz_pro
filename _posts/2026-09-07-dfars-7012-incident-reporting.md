---
layout: post
title: "DFARS 252.204-7012 Incident Reporting: 72 Hours, One Certificate, and a Portal That No Longer Exists"
date: 2026-09-07
description: "DFARS 252.204-7012 gives you 72 hours from discovery to report a cyber incident to DoD. The certificate you need to file cannot be obtained inside that window, and DIBNet, the portal your incident response plan probably names, was decommissioned in June 2025. What the clause actually requires, where the report goes now, and what has to exist before anything happens."
category: cmmc
tags: [CMMC, NIST 800-171, DFARS, Incident Reporting, DCISE]
image: /blog/images/1-dfars-7012-incident-reporting-72-hour-clock-hero.png
author: CyberZ
---

*The reporting obligation survived the CMMC pause untouched. The portal it points to did not.*

**DFARS 252.204-7012 incident reporting requires a defense contractor to report any cyber incident affecting covered defense information, the systems that handle it, or the contractor's ability to provide operationally critical support to the Department of Defense within 72 hours of discovery. Filing requires a DoD-approved medium assurance certificate obtained before the incident, the report now goes through the DC3 DCISE Incident Collection Format portal rather than the decommissioned DIBNet, and the contractor must preserve images of affected systems and monitoring data for at least 90 days after submission.**

<div style="border:1px solid #EE4C48;border-left:6px solid #EE4C48;background:#0D0D0F;color:#ffffff;border-radius:6px;padding:22px 26px;margin:28px 0;">
  <p style="margin:0 0 14px;font-weight:700;letter-spacing:1px;color:#EE4C48;">KEY TAKEAWAYS</p>
  <ul style="margin:0;padding-left:20px;line-height:1.6;">
    <li>The 72-hour clock in DFARS 252.204-7012(c) starts at discovery of any cyber incident, not at confirmation. Weekends and holidays count.</li>
    <li>Filing requires a DoD-approved medium assurance certificate under 7012(c)(3). Provisioning involves identity verification through an External Certification Authority and takes days, so a contractor without one cannot physically file inside the window.</li>
    <li>DIBNet was decommissioned on June 6, 2025. Reports now go through the DC3 DCISE Incident Collection Format portal, which generates an .xml file you transmit to DC3 via encrypted email or DoD SAFE. An incident response plan that still says "report at dibnet.dod.mil" points at a redirect.</li>
    <li>After filing, 7012(e) requires preserving images of all known affected systems and relevant monitoring data for at least 90 days. Wiping and rebuilding before imaging destroys evidence DoD is entitled to inspect.</li>
    <li>The obligation flows down to subcontractors under 7012(m). A sub reports directly to DoD and provides the incident report number to the prime, so the prime learns something happened, but not necessarily everything.</li>
  </ul>
</div>

The July 13, 2026 suspension of CMMC Phase 2 removed the third-party assessment calendar. It did not touch DFARS 252.204-7012, which sits in the contract itself and activates the moment something goes wrong in your environment. While most CMMC coverage this month is watching the Reform Task Force, whose findings go to the DoW CIO around September 13, the reporting clause keeps running on its own clock. It is the one obligation in the whole framework that is triggered by an attacker's schedule rather than a rulemaking calendar.

That would matter less if the mechanics had stayed stable. They have not. The reporting portal changed in mid-2025, the filing process now involves an .xml artifact and a secure transmission step, and the access credential is something you must already hold. Most incident response plans in the small end of the defense industrial base were written before any of that, which means the first time many contractors test their plan against the real process is during an actual incident, with roughly three days on the clock.

## What Counts as a Reportable Cyber Incident Under DFARS 7012?

The clause defines a cyber incident as actions taken through the use of computer networks that result in a compromise or an actual or potentially adverse effect on a covered contractor information system or the covered defense information residing on it. The trigger is broad on purpose. It covers three situations:

1. **Covered defense information is affected.** Unauthorized access to CUI, exfiltration, or potential exposure.
2. **The system handling it is affected.** Ransomware on a file server that stores contract technical data is reportable even if you cannot yet prove the CUI itself was touched.
3. **Your ability to provide operationally critical support is affected.** An outage that stops you from performing on a contract designated as operationally critical support is reportable on its own.

Notice what is not in the definition: confirmation. "Potentially adverse effect" means the reporting question is not "did they get the CUI" but "could this have affected the system or the information." If your EDR flags activity consistent with unauthorized access to an in-scope system, you are inside the definition while you are still investigating.

## The 72-Hour Clock Starts at Discovery, Not Confirmation

DFARS 252.204-7012(c)(1)(ii) requires the contractor to rapidly report, and the clause defines "rapidly report" as within 72 hours of discovery. Discovery is when you become aware the incident occurred or may have occurred. The window includes weekends and federal holidays, and there is no extension mechanism for "we were still doing forensics."

This is the piece that inverts most commercial incident response instincts. A commercial IR process investigates first and notifies when the picture is clear. The DFARS process reports on partial information and supplements later. Filing early with incomplete facts is expected. Under DFARS 204.7302, a reported incident is not, by itself, interpreted as evidence of failure to provide adequate security. The regulation is explicitly built so that reporting is safe and silence is not.

The risk calculus follows directly. An unnecessary report costs you a form. A missed 72-hour deadline on a real incident is a contract compliance failure that a contracting officer, a DCMA reviewer, or a future whistleblower can date to the hour. In an enforcement environment where DOJ settled with [Honeywell Aerospace for just over $2 million on September 1]({% post_url 2026-09-02-honeywell-fca-cybersecurity-settlement %}) over one network's NIST 800-171 posture, "we knew and did not report on time" is not a sentence you want in anyone's timeline.

## The Certificate You Cannot Get During an Incident

Here is the requirement that turns a reporting rule into a preparation rule. DFARS 252.204-7012(c)(3) states that in order to report cyber incidents, the contractor or subcontractor shall have or acquire a DoD-approved medium assurance certificate.

That certificate is a PKI credential, typically issued through an External Certification Authority such as IdenTrust or DigiCert (a Common Access Card also works, but small subcontractors rarely have one). Getting it involves identity verification of a named person, payment, and provisioning time measured in days. None of that is doable inside a 72-hour window that opened at 4pm on a Friday because a hospital of servers started encrypting themselves.

The practical rule: the certificate exists before the incident or the deadline is missed. It should be assigned to a named individual in your incident response plan, with a second credentialed person as backup, and its expiration date should sit in the same renewal tracker as your insurance policies. A certificate that expired eight months ago is functionally identical to no certificate.

![Timeline of the DFARS 7012 incident reporting sequence: certificate in hand before day zero, discovery starts the 72-hour clock, ICF filed at the DCISE portal, xml transmitted to DC3, incident number received, 90-day preservation window follows](/blog/images/2-dfars-7012-incident-reporting-timeline.png)

## DIBNet Is Gone. Where Does the Report Actually Go Now?

For years, the answer to "where do I report" was DIBNet at dibnet.dod.mil, and that is still the answer written into most incident response plans, many MSP runbooks, and even the text people remember from the clause. It is out of date. On June 5, 2025, the DoD Cyber Crime Center (DC3) announced that DIBNet would be decommissioned the following day, June 6, 2025, as part of a cost-reduction and modernization effort.

The current path:

1. The old URL redirects to the DC3 DIB Cybersecurity DCISE page.
2. From there, "Report a Cyber Incident" leads to the Incident Collection Format (ICF) portal at icf.dcise.cert.org. Logging in requires the medium assurance certificate from the previous section.
3. You complete the ICF with the incident details: date and time of discovery, affected contract numbers, contracting agency, type of incident, type of covered defense information involved, points of contact, and a narrative description.
4. The process generates a standardized .xml file, which you transmit securely to DC3 via encrypted email or DoD SAFE.
5. DC3 confirms receipt and issues an incident report number. That number anchors everything that follows, including what a subcontractor hands to its prime.

One more consequence worth knowing in advance: under DFARS PGI 204.7303-3, once you report, DC3 sends the cyber incident report to the contracting officers identified on the ICF. Your customer finds out through official channels, promptly. Plan your prime and contracting officer communications with that in mind rather than being surprised by it.

If your incident response plan predates June 2025 and names DIBNet, this is the cheapest finding you will ever remediate. Update the plan, walk the two credentialed people through the DCISE flow on paper, and note the revision in the plan's change log. That change log entry is itself evidence for requirement 3.6.1.

## After You File: 90 Days of Preservation and the Malware Rule

Two obligations continue after submission, and both run against the natural urge to clean up and move on.

**Preservation, 7012(e).** You must preserve and protect images of all known affected information systems and all relevant monitoring and packet capture data for at least 90 days from submission of the report, so DoD can decide whether it wants to conduct a damage assessment. The most common real-world failure is exactly the responsible-looking move: contain, wipe, reimage, restore from backup, get people working again. Do the forensic imaging first. Hash the images, store them off the affected environment, and let the rebuild proceed from copies. Recovery speed is a business metric; preserved evidence is a contract term.

**Malware, 7012(d).** If you discover and isolate malicious software in connection with the incident, you submit it to DC3 in accordance with their instructions. Not to your antivirus vendor's portal, and never as an email attachment to the contracting officer.

There is also a quieter dynamic here. The incident report describes your environment at its worst moment, in writing, to the government. If your SPRS score says 110 and your ICF narrative describes flat networks and shared admin passwords, you have just handed an investigator the gap. This is the same distance that produced the LOGZONE settlement, and it is why the [annual affirmation]({% post_url 2026-08-23-cmmc-affirmation-false-claims-act %}) and an [honestly scored SPRS posture]({% post_url 2026-09-06-how-to-improve-sprs-score %}) are the other half of incident readiness. Report fast, and make sure the rest of your paper trail can survive being read next to the report.

## Subcontractors: The Flow-Down Works Both Ways

Under 7012(m), primes must include the clause in subcontracts for operationally critical support or where performance involves covered defense information. If you are the sub, the reporting duty is yours directly: you report to DoD through the same DCISE process, which means you need your own medium assurance certificate, not a promise that the prime will handle it.

You also provide the incident report number to the prime (or the next higher tier) as soon as practicable. Note the design: the prime gets the number, not automatically the full report. In practice, primes respond to that gap contractually, and many supplier agreements now demand faster and fuller notification than the DFARS baseline. Read your subcontract's incident clause next to the regulation, because the tighter of the two is your real obligation.

## What Has to Exist Before Anything Happens

Requirement 3.6.1 of NIST SP 800-171 requires an operational incident-handling capability, 3.6.2 requires tracking, documenting, and reporting incidents to designated officials and authorities, and 3.6.3 requires testing the capability. DFARS 7012 reporting is where those three requirements stop being paperwork. The pre-incident checklist:

![Checklist of what must exist before a DFARS 7012 reportable incident: active medium assurance certificate with named holder and backup, IR plan naming the DCISE ICF portal, reportable-incident decision criteria, forensic imaging step before remediation, subcontract clause comparison, annual tabletop test](/blog/images/3-dfars-7012-reporting-readiness-checklist.png)

1. **An active medium assurance certificate**, assigned to a named person with a credentialed backup, expiration tracked.
2. **An IR plan that names the current process**: DCISE ICF portal, .xml generation, DoD SAFE transmission, and the DC3 hotline as fallback.
3. **Decision criteria for "reportable"** written down, so the 2am judgment call about whether the clock has started is made against pre-agreed rules rather than adrenaline.
4. **A forensic imaging step sequenced before remediation** in the plan, with the 90-day retention spelled out.
5. **Your subcontract incident clauses** compared against the DFARS baseline, with the stricter terms flagged.
6. **A dated tabletop test** of the whole sequence, at minimum annually, which is also your 3.6.3 evidence.

Every item on that list doubles as an assessment artifact. The [CMMC Level 2 Evidence Tracker for NIST 800-171 Audit](https://payhip.com/b/LN2UB) ($67) maps each 3.6 requirement to the evidence that proves it, including the incident log and test records this section describes. And the IR roles, reporting path, and responsible parties all belong in your System Security Plan; the [CMMC Level 2 System Security Plan (SSP) Template](https://payhip.com/b/gB6oD) ($77) has the incident response sections pre-structured so the plan and the SSP say the same thing.

## Frequently Asked Questions

**Does the CMMC Phase 2 suspension change any of this?**
No. The suspension paused the third-party assessment rollout under the CMMC Program rule. DFARS 252.204-7012 is a contract clause that has been in effect since 2017, and DoD confirmed in the July 13 announcement that existing DFARS obligations remain in force. If the clause is in your contract, the 72-hour requirement applies today.

**We only hold Federal Contract Information, not CUI. Do we report under 7012?**
The clause's reporting trigger is built around covered defense information and operationally critical support. If you genuinely hold only FCI, the 7012 reporting machinery generally is not your obligation, but check whether the clause appears in your contract anyway and whether your prime's flow-down imposes its own notification duty. Many do. If you are unsure which category your data falls in, [sorting that scope question]({% post_url 2026-07-26-dibcac-assessment-preparation %}) comes before everything else.

**The 72 hours passed and we did not report. Now what?**
Report immediately anyway. A late report starts the preservation clock, gets DC3 engaged, and is defensible in a way that continued silence is not. Document why the deadline was missed and what you changed. The pattern DOJ has punished in every cyber False Claims Act settlement to date is the sustained gap between what the contractor knew and what it told the government, not the imperfect-but-honest filing.

**Does reporting mean DoD will conclude our security failed?**
DFARS 204.7302 says a cyber incident that is properly reported shall not, by itself, be interpreted as evidence of failure to provide adequate security. What creates exposure is the surrounding record: an SPRS score that overstated reality, an affirmation signed over known gaps, or evidence destroyed in the rebuild.

## The Bottom Line

Incident reporting under DFARS 252.204-7012 is a preparation problem wearing an emergency's clothes. The 72-hour clock is survivable for any contractor who set up the certificate, pointed the plan at the right portal, and sequenced imaging before cleanup. It is nearly impossible for a contractor meeting the process for the first time on day zero, and the process quietly changed in June 2025, so "we set this up years ago" is its own risk.

If you are building the full readiness picture rather than patching one gap at a time, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) bundles the SSP template, evidence tracker, scoping worksheet, SPRS workbook, and POA&M tools into one working set. It is built for the contractor who wants the incident report, the SSP, and the posted score to tell the same story when someone eventually reads all three together.

## Sources

- DFARS 252.204-7012, Safeguarding Covered Defense Information and Cyber Incident Reporting, acquisition.gov
- DFARS 204.7302, Policy (cyber incident reporting), acquisition.gov
- DFARS PGI 204.7303-3, Cyber incident and compromise reporting, acquisition.gov
- DoD Cyber Crime Center (DC3), DIB Cybersecurity DCISE program pages and ICF reporting portal, dc3.mil
- NIST SP 800-171 Rev 2, requirements 3.6.1, 3.6.2, 3.6.3, csrc.nist.gov
- DoW CIO memorandum suspending CMMC Phase 2, July 13, 2026
- U.S. Department of Justice, LOGZONE Inc. settlement press release, June 18, 2026
- U.S. Department of Justice, Honeywell Aerospace Inc. settlement announcement, September 1, 2026
