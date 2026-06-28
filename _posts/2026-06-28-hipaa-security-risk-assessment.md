---
layout: post
title: "HIPAA Security Risk Assessment: What the Rule Requires and Why OCR Keeps Citing It"
date: 2026-06-28
description: "A HIPAA security risk assessment is a required Security Rule specification at 45 CFR 164.308(a)(1)(ii)(A). Here is what it must cover and why OCR enforces it most."
category: hipaa
tags: [HIPAA, Security Rule, Risk Analysis, OCR, ePHI]
image: /blog/images/1-hipaa-security-risk-assessment-hero.png
author: CyberZ
---

*The Office for Civil Rights built an entire enforcement initiative around one missing document. Here is what that document has to contain, and why so many practices get it wrong.*

**A HIPAA security risk assessment, called a risk analysis in the regulation, is a documented evaluation of the risks and vulnerabilities to all electronic protected health information (ePHI) a covered entity or business associate holds. It is a required implementation specification under the HIPAA Security Rule at 45 CFR 164.308(a)(1)(ii)(A), not an optional or addressable one. Since late 2024 it has been the single failure the HHS Office for Civil Rights enforces most often.**

<div style="border:1px solid #EE4C48;border-left:6px solid #EE4C48;background:#0D0D0F;color:#ffffff;border-radius:6px;padding:22px 26px;margin:28px 0;">
  <p style="margin:0 0 14px;font-weight:700;letter-spacing:1px;color:#EE4C48;">KEY TAKEAWAYS</p>
  <ul style="margin:0;padding-left:20px;line-height:1.6;">
    <li>The risk analysis is a <strong>required</strong> implementation specification at 45 CFR 164.308(a)(1)(ii)(A). It is not addressable, and there is no documented exception that lets you skip it.</li>
    <li>OCR's Risk Analysis Initiative, launched in late 2024, has produced 12 announced enforcement actions through February 2026. Each one rests on this single failure.</li>
    <li>The analysis must cover every place ePHI lives, not just your electronic health record. Partial scope is one of the most common findings.</li>
    <li>As of 2026, OCR expects the analysis to drive documented remediation. A binder no one acts on does not satisfy the rule.</li>
    <li>Business associates are on the hook for the same requirement, word for word, as covered entities.</li>
  </ul>
</div>

## What a HIPAA security risk assessment actually is

The terms get used loosely, so start with the language in the regulation. The HIPAA Security Rule does not use the phrase "risk assessment." It uses "risk analysis," and it sits inside the Security Management Process standard at 45 CFR 164.308(a)(1). That standard has four required implementation specifications: risk analysis, risk management, sanction policy, and information system activity review. Risk analysis is the first of the four, and it is the one everything else depends on.

The regulatory text is short. It directs a covered entity or business associate to conduct an accurate and thorough assessment of the potential risks and vulnerabilities to the confidentiality, integrity, and availability of the electronic protected health information it holds. That is the whole obligation in one sentence, and the weight is carried by two words: "accurate" and "thorough."

In its own guidance, OCR calls the risk analysis foundational. Its reasoning is plain. You cannot decide which safeguards are reasonable and appropriate for your environment until you know what ePHI you have, where it lives, and what could happen to it. Every later decision in the Security Rule, from access controls to encryption to audit logging, is supposed to flow from the findings of the analysis. Skip the analysis and the rest of your program is built on a guess.

## Required, not addressable: the distinction most checklists miss

This is where generic compliance content goes wrong, and where an assessor's attention goes first.

The Security Rule sorts its implementation specifications into two buckets. Required specifications must be implemented, full stop. Addressable specifications give you a decision: implement the safeguard, or, if you reasonably determine it is not reasonable and appropriate for your situation, document why and put an equivalent measure in place. Addressable does not mean optional. It means you owe a documented decision.

Encryption is the famous example. The encryption of ePHI at rest, at 45 CFR 164.312(a)(2)(iv), is addressable. A small practice can, in theory, document a reasoned decision not to encrypt a particular system and substitute another control. People hear that and assume the same flexibility runs through the whole rule.

It does not reach the risk analysis. The risk analysis is required. There is no documented-exception path, no equivalent-measure substitute, no reasonable-and-appropriate off-ramp. You either conducted an accurate and thorough analysis of the risks to all your ePHI, or you did not. When OCR opens an investigation, the absence of a defensible risk analysis is not a gray area it has to argue. It is a yes-or-no fact.

![CyberZ graphic on a dark background titled "Required, not addressable," listing the four required implementation specifications under the Security Management Process at 45 CFR 164.308(a)(1): risk analysis, risk management, sanction policy, and information system activity review, with a note that encryption at 164.312(a)(2)(iv) is addressable while risk analysis is not.](/blog/images/2-hipaa-risk-analysis-required-spec.png)

## Why OCR is enforcing this one on its own

At the end of 2024, OCR launched what it calls the Risk Analysis Initiative. The premise was a calculated bet: the most common, most consequential, and most provable Security Rule failure is the one written into the rule's very first requirement. So rather than wait for a large breach to surface a missing analysis, OCR began pursuing the risk-analysis failure as the headline finding on its own.

The bet has held up. Through February 2026, OCR has announced 12 enforcement actions under the initiative, a run of resolution agreements that began in January 2025 and continued into 2026. They span the full range of regulated entities, from a small dental software vendor to substance use disorder treatment providers to ransomware-hit business associates. The dollar figures vary widely, from a five-figure settlement up into the six figures, but the financial penalty was never the real cost. Every one of these resolutions carried a corrective action plan, typically monitored for two to three years. That ongoing federal oversight, not the check, is what reshapes how a practice operates.

A few named examples make the pattern concrete. OCR settled with Behavioral Health Solutions of Deer Oaks for $225,000 in July 2025 over a failure to conduct a sufficient risk analysis and to put appropriate safeguards in place. It settled with Syracuse ASC for $250,000 the same month, with a two-year corrective action plan requiring a full risk analysis, policy updates, and workforce training. The initiative's very first action, in October 2024, resolved a ransomware investigation against an Oklahoma emergency medical services provider for $90,000. Different organizations, different incidents, same root finding.

![CyberZ graphic on a dark background reading "12 enforcement actions announced through February 2026" under the heading "OCR Risk Analysis Initiative," listing the Behavioral Health Solutions of Deer Oaks settlement at $225,000, Syracuse ASC at $250,000, and the first Oklahoma EMS action at $90,000, with a note that each carried a two- to three-year corrective action plan.](/blog/images/3-ocr-risk-analysis-initiative-enforcement.png)

There is also a 2026 shift worth flagging, because it raises the bar. OCR has signaled, including in its January 2026 cybersecurity newsletter, that it now expects the risk analysis to connect to real risk management. It is no longer enough to identify that you run unpatched software or have firmware gaps. The agency wants to see that you acted on what the analysis found, with documented remediation tied back to the specific risks. The analysis and the risk management specification at 164.308(a)(1)(ii)(B) are meant to work as a loop, and OCR is starting to grade the loop, not just the first half of it.

One more point of accuracy. OCR did publish a notice of proposed rulemaking in January 2025 that would clarify and expand the risk analysis requirement, among other Security Rule changes. That proposal is not final, and several major industry groups have asked OCR to withdraw or narrow it. The requirement described in this article is the one in force today, independent of whatever the proposed update eventually becomes. Treat the existing rule as the standard you are held to, because it is.

## What a compliant risk analysis has to cover

"Accurate and thorough" is the test, and scope is where it is won or lost. A risk analysis has to account for every place ePHI is created, received, maintained, or transmitted. Not the electronic health record alone. The billing system, the practice management software, the scheduling tool, the backups, the cloud storage, the email that carries an attached chart, the laptops and phones that connect from home, the medical devices that store readings, the vendor portals. If ePHI touches it, it is in scope.

A defensible analysis works through a recognizable set of elements. OCR's own guidance points to the methodology in NIST Special Publication 800-66 as a reasonable approach, and the through-line is consistent:

- An inventory of where all ePHI lives and how it moves, system by system and vendor by vendor.
- The reasonably anticipated threats to that information, from ransomware and phishing to lost devices and insider misuse.
- The vulnerabilities a threat could exploit, paired with the controls already in place.
- An assessment of the likelihood and the potential impact of each risk, producing a risk level you can rank and act on.
- Documentation of all of it, retained and dated, because under 45 CFR 164.316 you must keep this record and make it available.

Two scope traps deserve their own mention. First, business associates. The regulation names them directly: the risk analysis requirement applies to a covered entity or business associate. A billing company, an IT vendor, a cloud EHR host, a release-of-information service, all of them owe their own analysis, and several of the initiative's settlements were with business associates. Second, the analysis is not a one-time artifact. It has to be reviewed and updated as your environment changes, and at least periodically. A risk analysis dated three years ago, describing systems you no longer run, is closer to evidence against you than evidence for you.

## The most common ways it fails

The settlements rhyme because the mistakes do. A handful of failure patterns show up again and again.

The first is partial scope, the one already named. A practice runs a careful analysis of its EHR and calls the job done, while the billing platform, the backups, and a half-dozen SaaS tools go unexamined. OCR reads that as not accurate and not thorough, which is the exact statutory language it needs.

The second is the one-and-done. An analysis was performed once, often years ago, and never refreshed through a server migration, a new cloud vendor, or a shift to remote work. The document exists, but it no longer describes the organization.

The third is the template with no substance. A blank or boilerplate form gets filled in to produce a file, but it reflects no real evaluation of this specific environment. It looks like a risk analysis and functions like a placeholder.

The fourth, and increasingly the one OCR cares about, is the analysis that leads nowhere. Risks were identified and then nothing was remediated, with no risk management plan and no documented follow-through. After 2026, expect that disconnect to be treated as a finding in its own right.

The fifth is a definitional mix-up. A security gap assessment, a SOC 2 readiness check, or a vendor questionnaire is not a HIPAA risk analysis. They can feed it, but none of them satisfies 164.308(a)(1)(ii)(A) on its own. The rule asks a specific question about risks to ePHI, and only an analysis built to answer that question counts.

## What to do this quarter

You do not need a consultant to start. You need to do the work in the right order.

Inventory first. List every system, device, application, and vendor that creates, receives, maintains, or transmits ePHI. This single step surfaces the scope gaps that drive most findings, because almost everyone underestimates how many places their patient data actually lives.

Run or refresh the analysis across that full inventory. For each system, document the threats, the vulnerabilities, the controls you have, and the resulting risk level. Be honest about the gaps. An analysis that finds real problems is worth far more than one that pronounces you perfect.

Then close the loop. Tie each identified risk to a risk management action with an owner and a target date, and keep a record as you remediate. That is the part OCR is now grading, and it is the part a blank template can never produce for you.

Finally, date it, retain it, and put a recurring calendar entry to review it at least annually and after any major change. The retention obligation is real, and a current analysis is the difference between a short OCR inquiry and a multi-year corrective action plan.

If you would rather not build the workbook from scratch, the [HIPAA Security Risk Assessment Tool: Excel + Guide](https://payhip.com/b/vXmYA) ($57) walks you through every ePHI location and produces the documented analysis and risk-management log OCR asks to see.

## The bottom line

The HIPAA risk analysis is the most basic obligation in the Security Rule and the one regulated entities most reliably skip, shortcut, or let go stale. OCR has noticed, built a standing enforcement initiative around it, and started grading whether the analysis actually drives remediation. The fix is not complicated, but it is not optional either. Inventory all your ePHI, evaluate the risks to every system honestly, act on what you find, and keep the record current. Required means required.

## Sources

- 45 CFR 164.308 (Administrative safeguards), Security Management Process standard and the Risk Analysis required implementation specification: [eCFR, 45 CFR 164.308](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-C/part-164/subpart-C/section-164.308)
- HHS Office for Civil Rights, Guidance on Risk Analysis Requirements under the HIPAA Security Rule: [HHS.gov, Guidance on Risk Analysis](https://www.hhs.gov/hipaa/for-professionals/security/guidance/guidance-risk-analysis/index.html)
- HHS Office for Civil Rights HIPAA enforcement and Risk Analysis Initiative settlements and newsroom: [HHS.gov, HIPAA Enforcement](https://www.hhs.gov/hipaa/for-professionals/compliance-enforcement/index.html)
- 45 CFR 164.312 (Technical safeguards), encryption as an addressable implementation specification: [eCFR, 45 CFR 164.312](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-C/part-164/subpart-C/section-164.312)
