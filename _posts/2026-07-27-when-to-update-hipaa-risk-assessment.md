---
layout: post
title: "When to Update Your HIPAA Risk Assessment: The Triggers OCR Actually Names"
date: 2026-07-27
description: "The HIPAA Security Rule sets no interval for risk analysis. It sets a trigger standard. Here is what actually forces an update, straight from 45 CFR 164 and OCR guidance."
category: HIPAA
tags: [HIPAA, Security Rule, risk analysis, OCR, compliance, healthcare]
image: /blog/images/1-hipaa-risk-analysis-update-triggers-hero.png
author: CyberZ
---

*Half of page one on Google will tell you a HIPAA risk assessment is required every twelve months. The regulation says no such thing. Here is the standard that actually applies, and the four triggers OCR names by hand.*

**The HIPAA Security Rule does not require an annual risk assessment. It requires you to update your risk analysis in response to environmental or operational changes affecting the security of electronic protected health information. That phrase, not a calendar date, is the legal standard.** It appears three separate times in 45 CFR Part 164, Subpart C, and it is the language an OCR investigator will hold your documentation against.

<div style="border-left:4px solid #EE4C48;background:#f7f7f8;padding:18px 22px;margin:28px 0;border-radius:4px;">
<strong style="display:block;margin-bottom:10px;font-size:1.05em;">Key Takeaways</strong>
<ul style="margin:0;padding-left:20px;line-height:1.7;">
<li>No provision of the HIPAA Security Rule specifies how often a risk analysis must be performed. OCR states this directly in its own guidance.</li>
<li>The governing standard is "environmental or operational changes," which appears in &sect; 164.308(a)(8), &sect; 164.316(b)(2)(iii), and &sect; 164.306(e).</li>
<li>OCR names four example triggers: a security incident, a change in ownership, turnover in key staff or management, and plans to incorporate new technology.</li>
<li>New technology triggers the analysis at the <em>planning</em> stage, not after go-live.</li>
<li>Documentation must be retained for six years from creation or from the date it was last in effect, whichever is later.</li>
<li>The proposed Security Rule overhaul would change some of this. It is still proposed, and OMB now targets July 2027 for final action.</li>
</ul>
</div>

## Where the annual myth comes from

Search "how often is a HIPAA risk assessment required" and you will get a split decision on page one. Several results state flatly that the Security Rule mandates an assessment at least once per year. Others state, correctly, that it does not.

The confusion has a real source, and it is worth understanding because it explains why so many practices think they are compliant when they are not.

The annual habit comes from adjacent programs, not from HIPAA. CMS attestation requirements under the EHR incentive and Promoting Interoperability programs tied a security risk analysis to a reporting period, which for most participants meant a yearly cycle. Cyber liability insurers ask for a current assessment on renewal, which is annual. Accreditation bodies run yearly. All of that is real, and for many organizations an annual cadence is a perfectly sensible operating decision.

None of it is the Security Rule.

## What the regulation actually says

Three provisions matter, and they work together.

**&sect; 164.308(a)(1)(ii)(A) creates the requirement.** Risk analysis is a required implementation specification under the Security Management Process standard. The text instructs covered entities and business associates to "conduct an accurate and thorough assessment of the potential risks and vulnerabilities to the confidentiality, integrity, and availability of electronic protected health information" they hold. Notice what is absent: any statement of frequency.

**&sect; 164.308(a)(8) creates the trigger.** The Evaluation standard requires a periodic technical and nontechnical evaluation, "based initially upon the standards implemented under this rule and, subsequently, in response to environmental or operational changes affecting the security of electronic protected health information."

**&sect; 164.316(b)(2)(iii) applies the same trigger to your documentation.** The Updates specification, which is required rather than addressable, says to review documentation periodically and update as needed, "in response to environmental or operational changes affecting the security of the electronic protected health information."

A fourth provision, &sect; 164.306(e), ties the knot: you must review and modify your security measures as needed and update the documentation of those measures in accordance with &sect; 164.316(b)(2)(iii).

![Calendar versus trigger: what online sources claim about HIPAA risk assessment frequency compared with the actual text of the Security Rule](/blog/images/3-hipaa-risk-analysis-annual-myth-vs-rule-text.png)

Read those together and the architecture is clear. The rule is deliberately indifferent to your calendar. It cares whether something changed in your environment or your operations, and whether you responded to it.

OCR removes any remaining ambiguity in its *Guidance on Risk Analysis*: the Security Rule does not specify how frequently to perform risk analysis, the frequency will vary among covered entities, and some entities may perform the process annually or as needed, with bi-annual or every three years given as acceptable examples depending on the circumstances of their environment.

That is the agency that enforces the rule, saying every three years can be fine.

## The four triggers OCR names by hand

The same guidance document does something more useful than state the standard abstractly. It gives examples. OCR writes that if a covered entity has experienced a security incident, has had a change in ownership, has had turnover in key staff or management, or is planning to incorporate new technology to make operations more efficient, the potential risk should be analyzed.

![The four risk analysis triggers named in OCR guidance: security incident, change in ownership, turnover in key staff or management, and planning to incorporate new technology](/blog/images/2-ocr-named-risk-analysis-triggers.png)

Each of these carries more weight than it first appears.

**A security incident, not a breach.** The trigger is the incident, not the reportable breach. A phishing email that a staff member clicked and reported, a laptop that went missing and was recovered, a misconfigured share that was open for two days: these are security incidents. Most practices document them in an incident log and never revisit the risk analysis. The guidance does not draw the line at breach notification thresholds.

**A change in ownership.** Practice acquisitions, mergers, private equity roll-ups, and the sale of a single location all qualify. In an acquisition the risk analysis question is not theoretical. You have inherited someone else's systems, someone else's business associate agreements, and someone else's unaddressed findings.

**Turnover in key staff or management.** This is the trigger most often ignored, and the one most likely to be embarrassing in an investigation. When the office manager who set up the EHR permissions leaves, the risk posture changes even if no system changed. Institutional knowledge about who has access to what is itself a control.

**Planning to incorporate new technology.** Read the tense. OCR does not say "after implementing new technology." It says planning to. The guidance is explicit on the point: an integrated risk analysis process is performed as new technologies and business operations are planned, which reduces the effort required to address risks identified after implementation.

That distinction matters enormously in 2026. If a practice is evaluating an AI scribe, a patient messaging platform, a new telehealth vendor, or a cloud backup provider, the trigger fires during evaluation. Running the analysis after the contract is signed and the tool is live means you have already accepted whatever risk it carries.

## A practical trigger list for a small practice

The regulation gives you a standard. Here is what that standard tends to mean in a fifteen-person clinic or a forty-person specialty group.

| Event | Trigger basis | Typical scope of update |
|---|---|---|
| New EHR, PM system, or major version upgrade | New technology, planned | Full re-analysis |
| Adding an AI scribe, chatbot, or transcription tool | New technology, planned | Full re-analysis of that data flow |
| New business associate touching ePHI | Operational change | Targeted, plus BAA review |
| Opening or closing a location | Environmental change | Full re-analysis |
| Practice sale, merger, or acquisition | Ownership change | Full re-analysis |
| Departure of IT lead, privacy officer, or office manager | Key staff turnover | Targeted access and permissions review |
| Ransomware, phishing click, lost device, misdirected ePHI | Security incident | Targeted, tied to the incident findings |
| Moving on-prem systems to cloud hosting | Environmental change | Full re-analysis |
| Remote work or telehealth expansion | Operational change | Targeted, endpoints and transmission |
| Nothing changed in eighteen months | None fired | Document the review, note no material change |

That last row is the one people miss. If nothing triggered, you still perform a periodic review and you still write down that you performed it and found no material change. A quiet year is not an excuse for a silent file. It is a short memo.

## What OCR asks for when it comes looking

Risk analysis findings are among the most commonly cited issues in OCR enforcement, and the reason is usually not that the practice never did one. It is that the practice cannot prove what it did or when.

![What OCR asks for when it requests your risk analysis: the analysis, the date, the trigger, the risk decisions, and the actions taken](/blog/images/4-hipaa-risk-analysis-documentation-evidence.png)

The Security Rule requires the risk analysis to be documented but does not require a specific format (&sect; 164.316(b)(1)). That flexibility is often misread as permission to be vague. In practice, the absence of a mandated format means the burden of demonstrating adequacy falls entirely on you.

Three failures show up repeatedly:

- **The undated analysis.** A spreadsheet with no date, no version, and no author. If you cannot establish when it was performed, you cannot establish that it was current at the time of an incident.
- **The overwritten file.** Each year's review saved over the last one. &sect; 164.316(b)(2)(i) requires retention for six years from the date of creation or the date the document was last in effect, whichever is later. Overwriting destroys the record you are required to keep.
- **The orphaned analysis.** Risks identified, rated, and never connected to anything. Risk analysis feeds risk management under &sect; 164.308(a)(1)(ii)(B). An analysis with no corresponding remediation record invites the obvious question.

The fix is unglamorous. Date every version, keep every version, and write one line recording what triggered the revision. A file named `risk-analysis-2026-07-27-new-telehealth-vendor.xlsx` answers three questions before anyone opens it.

If you want that structure already built, the [HIPAA Security Risk Assessment Tool: Excel + Guide](https://payhip.com/b/vXmYA) is $57 and includes the asset inventory, threat and vulnerability pairing, risk scoring, and a dated revision log set up to survive exactly this kind of request.

## One thing that could change: the proposed Security Rule

You have probably seen coverage suggesting an annual risk analysis is about to become mandatory. That coverage is describing a proposed rule, and some of it is describing it as though it were already law.

HHS published the Notice of Proposed Rulemaking to strengthen the Security Rule at 90 FR 800 on January 6, 2025, under RIN 0945-AA22. The comment period closed March 7, 2025. The proposal would remove the "addressable" designation and make implementation specifications required, among other significant changes.

It has not been finalized. OCR's regulatory agenda originally pointed at a May 2026 final action, that date passed without publication, and OMB's Unified Agenda now shows final action targeted for July 2027. More than a hundred hospital systems and provider associations have formally asked HHS to withdraw or narrow the proposal. Whether it is finalized as written, modified, delayed again, or withdrawn is not knowable right now.

Two practical implications. First, do not restructure your program around requirements that do not exist yet. Second, do not treat the delay as a reprieve, because the current rule is being enforced today and the trigger standard has been in force since 2003.

## What to do this week

1. **Find your most recent risk analysis and check whether it is dated.** If it is not, that is the first finding anyone will make.
2. **List every change since that date.** New systems, new vendors, new locations, staff departures, security incidents, ownership changes. Use the table above as a prompt.
3. **Match each change to a trigger.** If any of them touch ePHI, the update is already overdue and has been since the change occurred.
4. **Check what is in planning right now.** Any technology under evaluation triggers the analysis before you sign, not after.
5. **Confirm you still hold six years of prior versions.** If you have been overwriting one file, start versioning today and note the gap honestly.
6. **Write the trigger down.** One line per revision recording what prompted it. This is the single cheapest piece of evidence you can create.

The organizations that struggle in an OCR review are rarely the ones that skipped the analysis. They are the ones who did the work and cannot prove when, or why, or what happened next.

## Sources

- 45 CFR 164.308, Administrative safeguards. Electronic Code of Federal Regulations. [68 FR 8376, Feb. 20, 2003, as amended at 78 FR 5695, Jan. 25, 2013]
- 45 CFR 164.316, Policies and procedures and documentation requirements. Electronic Code of Federal Regulations.
- 45 CFR 164.306, Security standards: General rules. Electronic Code of Federal Regulations.
- HHS Office for Civil Rights, *Guidance on Risk Analysis*. Content last reviewed September 26, 2025.
- HHS, *HIPAA Security Rule To Strengthen the Cybersecurity of Electronic Protected Health Information*, Notice of Proposed Rulemaking, 90 FR 800, January 6, 2025 (RIN 0945-AA22).
- Office of Management and Budget, Unified Agenda of Regulatory and Deregulatory Actions, RIN 0945-AA22.
