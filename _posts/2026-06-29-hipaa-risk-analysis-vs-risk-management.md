---
layout: post
title: "HIPAA Risk Analysis vs Risk Management: Why the Analysis Alone Will Not Save You"
date: 2026-06-29
description: "HIPAA risk analysis and risk management are two separate Security Rule requirements at 45 CFR 164.308(a)(1)(ii)(A) and (B). Here is the difference and why OCR enforces both."
category: hipaa
tags: [HIPAA, Security Rule, Risk Analysis, Risk Management, OCR, ePHI]
image: /blog/images/1-hipaa-risk-analysis-vs-risk-management-hero.png
author: CyberZ
---

*A risk analysis tells you where you are exposed. Risk management is what you do about it. In 2026 the Office for Civil Rights is enforcing the second one as hard as the first.*

**HIPAA risk analysis and risk management are two separate, sequential requirements inside the same Security Rule standard. Risk analysis, at 45 CFR 164.308(a)(1)(ii)(A), is the documented assessment that identifies the risks and vulnerabilities to electronic protected health information (ePHI). Risk management, at 45 CFR 164.308(a)(1)(ii)(B), is the requirement to reduce those risks to a reasonable and appropriate level. Doing the first without the second does not satisfy the rule, and OCR has spent 2026 making that point with money.**

<div style="border:1px solid #EE4C48;border-left:6px solid #EE4C48;background:#0D0D0F;color:#ffffff;border-radius:6px;padding:22px 26px;margin:28px 0;">
  <p style="margin:0 0 14px;font-weight:700;letter-spacing:1px;color:#EE4C48;">KEY TAKEAWAYS</p>
  <ul style="margin:0;padding-left:20px;line-height:1.6;">
    <li>Risk analysis (164.308(a)(1)(ii)(A)) finds the risks. Risk management (164.308(a)(1)(ii)(B)) reduces them. They are two different required specifications, not one task.</li>
    <li>A completed risk analysis that sits in a binder with no documented remediation is the exact gap OCR keeps citing.</li>
    <li>In 2026 OCR resolved settlements squarely on this gap, including $103,000 with Top of the World Ranch Treatment Center, its 11th Risk Analysis Initiative action, and four ransomware settlements totaling about $1.165 million.</li>
    <li>OCR's stated position is that the unaddressed vulnerability is the violation, independent of whether an attacker exploited it.</li>
    <li>The proposed 2026 Security Rule would tighten this further, but it is still a proposed rule, not law, and OCR is not enforcing it yet.</li>
  </ul>
</div>

## Two requirements, one standard

Both obligations live inside a single standard: the Security Management Process at 45 CFR 164.308(a)(1). That standard carries four required implementation specifications: risk analysis, risk management, sanction policy, and information system activity review. The first two are the ones that get conflated, and the order matters. Risk analysis comes first because it produces the findings. Risk management comes second because it acts on them.

This is not a drafting accident. The Security Rule is built so that every safeguard decision you make is supposed to trace back to a documented finding. You identify the risk, then you reduce it, then you can show the connection between the two. If you have read our companion piece on what a [HIPAA security risk assessment](/blog/2026/06/28/hipaa-security-risk-assessment/) has to contain, this is the requirement that sits immediately after it and depends on it.

![Risk analysis versus risk management: two separate, sequential HIPAA Security Rule requirements at 45 CFR 164.308(a)(1)(ii)(A) and (B)](/blog/images/2-hipaa-risk-analysis-vs-risk-management-comparison.png)

The distinction is easy to state and easy to lose in practice. Risk analysis answers a question: where is our ePHI exposed? Risk management answers a different one: what did we do to fix it? A program that can answer the first but not the second is the program OCR has been resolving settlements against.

## What risk management actually requires

The regulatory text for risk management is short. At 164.308(a)(1)(ii)(B), a covered entity or business associate must implement security measures sufficient to reduce risks and vulnerabilities to a reasonable and appropriate level. The operative verb is reduce. Identifying a risk does nothing on its own. The rule wants the risk lowered, and it wants the lowering documented.

In operational terms, risk management is the action layer of your security program. It is the work that turns a list of findings into a set of closed items: prioritizing the findings by severity, assigning an owner to each, setting a target date, tracking the work to completion, and re-checking that the fix held. None of that is exotic. It is ordinary remediation discipline. What makes it a HIPAA obligation, rather than a best practice, is that the Security Rule names it as a required specification and OCR treats the absence of it as a finding.

HHS makes the dependency explicit in its own guidance. In the Office for Civil Rights material on risk analysis and risk management, the analysis is described as the basis for the security measures an organization then implements. The two are designed to operate as a loop, not a single event.

## Why OCR is enforcing the gap in 2026

OCR launched its Risk Analysis Initiative at the end of 2024 with a deliberate bet: that the most common and most provable Security Rule failure is the missing or inadequate risk analysis at 164.308(a)(1)(ii)(A). Eighteen months later that bet has produced one of the most consistent enforcement runs in the agency's history, and in 2026 the campaign has visibly widened from whether you did the analysis to whether you acted on it.

The numbers are concrete. In February 2026 OCR announced a $103,000 settlement with Top of the World Ranch Treatment Center, an Illinois substance use disorder provider, its 11th action under the Risk Analysis Initiative, with a two-year corrective action plan attached. In April 2026 OCR announced four separate settlements resolving ransomware investigations, together totaling roughly $1.165 million and involving about 427,000 individuals. Each of the four turned on the same root finding: the entity had not conducted an accurate and thorough risk analysis of the confidentiality, integrity, and availability of its ePHI.

![OCR Risk Analysis Initiative 2026 enforcement: a $103,000 settlement with Top of the World Ranch and four ransomware settlements totaling about $1.165 million](/blog/images/3-ocr-risk-analysis-initiative-2026-enforcement.png)

The legal theory tying these cases together is the part worth internalizing. OCR's position, stated with increasing clarity across the 2026 record, is that the unaddressed gap is itself the violation. The attacker who encrypted the data did not create the legal exposure. The vulnerability that was identified, or should have been, and then left unmanaged is what created it. That framing is why risk management has moved to the center. A finding you never remediated is not a neutral fact in an investigation. It is the evidence.

## Is a risk analysis enough on its own?

No, and treating it that way is how organizations end up on the wrong side of a settlement. A risk analysis without a remediation plan is a list of findings. It documents that you knew about a problem. If you never managed that problem down, the document you produced to demonstrate diligence becomes the record that you identified a risk and let it sit.

This is also where free tooling gets misunderstood. The HHS and ONC Security Risk Assessment Tool is a genuinely useful, no-cost way to work through and document the analysis itself. It is built to help you produce the assessment at 164.308(a)(1)(ii)(A). What it does not do is run the risk-management program at 164.308(a)(1)(ii)(B) for you. It will help you find the gaps. It will not assign, track, and close them, and it will not hold the remediation record an investigator asks to see. Producing the analysis and stopping there is the single most common way a well-intentioned practice still fails.

## What is coming: the proposed 2026 Security Rule, still proposed

You have probably seen headlines saying the 2026 HIPAA Security Rule now mandates encryption, multi-factor authentication, and annual penetration testing. Read those carefully, because as of mid-2026 that is not the law.

Here is the accurate status. OCR issued a Notice of Proposed Rulemaking on December 27, 2024, published in the Federal Register on January 6, 2025, with the comment period closing March 7, 2025. In its proposed form the rule would remove the longstanding distinction between required and addressable specifications and make nearly all of them required, and it would add specific technical mandates including encryption of ePHI, multi-factor authentication, and regular testing. OCR's regulatory agenda had targeted a final rule in spring 2026. That window has passed with nothing published, more than 4,700 comments are still being worked through, and a coalition of more than 100 hospital and provider organizations has asked HHS to withdraw the proposal over a first-year cost HHS itself estimated near $9 billion. If a final rule does issue, the proposal sets a 240-day window to comply.

None of that is in force. OCR is still enforcing the current Security Rule, the same rule that already requires both the analysis and the management. The direction of the proposed changes, if they survive, is to tighten that duty, not loosen it. So the work you do now under the current rule is not speculative and it is not wasted. It is the foundation the proposed rule would build on.

## What to do about it

Treat the analysis and the management as one connected loop, because that is how the rule reads and how OCR reviews it.

1. Run a documented risk analysis that covers everywhere ePHI actually lives, not just your electronic health record, to satisfy 164.308(a)(1)(ii)(A).
2. Turn every finding into a tracked remediation item with an owner, a target date, and a status, to satisfy 164.308(a)(1)(ii)(B). This is the step that converts a binder into a defensible program.
3. Keep the documentation. The Security Rule requires you to retain this material for six years under 45 CFR 164.316(b)(1), and an investigation will ask for it.
4. Reassess on material change: a new system, a new vendor with ePHI access, a new threat, or after any incident. A static analysis goes stale, and a stale analysis is treated as no analysis.

![From findings to defensible compliance: analyze, remediate, document, reassess, the loop the HIPAA Security Rule requires](/blog/images/4-hipaa-risk-management-remediation-cycle.png)

If you want both halves in one place, the [HIPAA Security Risk Assessment Tool: Excel + Guide](https://payhip.com/b/vXmYA) ($57) runs the analysis and the remediation tracking in the same workbook, so the findings and the actions live exactly where an investigator would ask to see them.

## The bottom line

Risk analysis and risk management are not interchangeable, and in 2026 OCR is treating the space between them as the violation. Find the risks, reduce them, and keep the record that shows you did both. The organizations getting cited are rarely the ones who did nothing. They are the ones who did the analysis and then stopped.

## Frequently asked questions

### Does HIPAA require risk management, or just a risk analysis?

Both. They are two separate required implementation specifications inside the same standard. Risk analysis is at 45 CFR 164.308(a)(1)(ii)(A) and risk management is at 45 CFR 164.308(a)(1)(ii)(B). Satisfying one does not satisfy the other.

### Is a HIPAA risk analysis enough on its own?

No. A risk analysis with no documented remediation is a list of findings. Failure to act on identified risks is the deficiency OCR has cited most often, and it is the basis for multiple 2026 settlements.

### What happens if you do not act on your risk analysis findings?

The unremediated finding becomes evidence. OCR's stated position in 2026 is that the unaddressed vulnerability is itself the violation, independent of whether a breach occurred, which means the gap can support a settlement on its own.

### How often is a HIPAA risk analysis required?

The current Security Rule does not set a fixed calendar. It requires the analysis to be accurate and thorough, which in practice means it must be reviewed and updated whenever your environment changes materially, such as a new system, a new vendor with ePHI access, or an incident. The proposed 2026 rule would add a defined cadence, but that rule is not final.

### Is the free HHS SRA Tool enough for HIPAA compliance?

The HHS and ONC Security Risk Assessment Tool helps you produce and document the risk analysis, but it is not a complete compliance program. On its own it does not run the risk-management and remediation tracking that 164.308(a)(1)(ii)(B) requires.

### What is the 2026 HIPAA Security Rule update?

It is a Notice of Proposed Rulemaking issued in late 2024 and published in the Federal Register in January 2025. As of mid-2026 it remains a proposed rule, not final law, and OCR is not enforcing it.

## Sources

- HHS Office for Civil Rights, HIPAA Security Rule NPRM fact sheet, December 27, 2024, and the Notice of Proposed Rulemaking published in the Federal Register, January 6, 2025.
- HHS Office for Civil Rights, Guidance on Risk Analysis Requirements under the HIPAA Security Rule.
- 45 CFR 164.308(a)(1)(ii)(A) and 164.308(a)(1)(ii)(B); 45 CFR 164.316(b)(1) (eCFR).
- HHS Office for Civil Rights enforcement announcement, Top of the World Ranch Treatment Center settlement, February 19, 2026.
- HHS Office for Civil Rights enforcement announcements, four ransomware settlements, April 23, 2026.

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Does HIPAA require risk management, or just a risk analysis?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Both. They are two separate required implementation specifications inside the same standard. Risk analysis is at 45 CFR 164.308(a)(1)(ii)(A) and risk management is at 45 CFR 164.308(a)(1)(ii)(B). Satisfying one does not satisfy the other."
      }
    },
    {
      "@type": "Question",
      "name": "Is a HIPAA risk analysis enough on its own?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. A risk analysis with no documented remediation is a list of findings. Failure to act on identified risks is the deficiency OCR has cited most often, and it is the basis for multiple 2026 settlements."
      }
    },
    {
      "@type": "Question",
      "name": "What happens if you do not act on your risk analysis findings?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The unremediated finding becomes evidence. OCR's stated position in 2026 is that the unaddressed vulnerability is itself the violation, independent of whether a breach occurred."
      }
    },
    {
      "@type": "Question",
      "name": "How often is a HIPAA risk analysis required?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The current Security Rule does not set a fixed calendar. It requires the analysis to be accurate and thorough, which means it must be reviewed and updated whenever the environment changes materially. The proposed 2026 rule would add a defined cadence, but that rule is not final."
      }
    },
    {
      "@type": "Question",
      "name": "Is the free HHS SRA Tool enough for HIPAA compliance?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The HHS and ONC Security Risk Assessment Tool helps you produce and document the risk analysis, but it is not a complete compliance program. On its own it does not run the risk-management and remediation tracking that 164.308(a)(1)(ii)(B) requires."
      }
    },
    {
      "@type": "Question",
      "name": "What is the 2026 HIPAA Security Rule update?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "It is a Notice of Proposed Rulemaking issued in late 2024 and published in the Federal Register in January 2025. As of mid-2026 it remains a proposed rule, not final law, and OCR is not enforcing it."
      }
    }
  ]
}
</script>
