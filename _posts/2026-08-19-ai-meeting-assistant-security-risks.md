---
layout: post
title: "AI Meeting Assistant Security Risks: What the Fireflies and Otter.ai Lawsuits Mean for a Small Business"
date: 2026-08-19
description: "On August 12 an AI note-taker's transcript became the core of a discrimination suit against Marathon Engineering. On August 13 a federal judge let wiretap and biometric claims against Otter.ai proceed. What HIPAA, DFARS 252.204-7012, CIPA and BIPA require before the next bot joins your call."
category: AI Security
tags: [AI meeting assistant, AI note taker, Fireflies, Otter.ai, shadow AI, HIPAA, CUI, DFARS 252.204-7012, BIPA, CIPA, AI acceptable use policy, AI governance, NIST AI RMF]
image: /blog/images/1-ai-meeting-assistant-security-risks-hero.png
author: CyberZ
---

*The AI note-taker is the one piece of software in your firm that nobody procured, nobody configured, and everybody uses. Last week two courts explained what that costs.*

**AI meeting assistant security risks are the data, privacy and compliance exposures created when a transcription bot such as Otter, Fireflies, Read AI or Fathom, or a built-in feature such as Zoom AI Companion, Microsoft Teams recap or Gemini in Google Meet, joins a call, captures audio and text from every participant, and stores, shares or trains on that content under the vendor's terms rather than yours. The exposure is different from ordinary cloud risk in one way that matters: the people being recorded include patients, clients, opposing counsel, prime-contractor staff and departing employees who never agreed to anything, and in a growing number of jurisdictions the law is treating the bot as a third party in the room, not as a tool the host is holding.**

<div class="key-takeaways" style="background:#16161a;border-left:4px solid #EE4C48;padding:20px 24px;margin:24px 0;">
<strong>Key Takeaways</strong>
<ul>
<li>On August 12, 2026, a former Marathon Engineering employee sued in New Jersey Superior Court after the company's Fireflies assistant kept transcribing her termination call after she dropped off, then emailed her the link. The transcript allegedly records a supervisor hoping to replace her with a "relatively strapping young man." Law360 reported the filing August 14.</li>
<li>On August 13, 2026, Judge Eumi K. Lee of the Northern District of California ruled on Otter.ai's motion to dismiss in In re Otter.AI Privacy Litigation (No. 5:25-cv-06911). Federal wiretap (ECPA), California CIPA, Illinois BIPA and unfair competition claims survive. CFAA and Washington Privacy Act claims were dismissed, mostly with leave to amend.</li>
<li>The plaintiffs' theory in Otter is that a bot which records non-users and uses the audio to train the vendor's own models is a third-party eavesdropper, not an extension of the meeting host. The court has not decided the merits, but it found the theory adequately pleaded.</li>
<li>Cruz v. Fireflies.AI (C.D. Ill., filed December 18, 2025) alleges the speaker-recognition feature creates and retains a voiceprint for every attendee, including people who never had a Fireflies account, without the notice and retention schedule BIPA requires under 740 ILCS 14/15.</li>
<li>Statutory damages do not require proof of harm: up to $10,000 per violation under 18 U.S.C. 2520, $5,000 per violation under Cal. Penal Code 637.2, and $1,000 to $5,000 per violation under 740 ILCS 14/20.</li>
<li>For a healthcare practice, a note-taker without a business associate agreement that captures a patient call is a disclosure of PHI to an unauthorized party under 45 CFR 164.502(e). For a defense subcontractor, a note-taker on a CUI discussion is a cloud service that must meet FedRAMP Moderate or equivalent under DFARS 252.204-7012(b)(2)(ii)(D). Neither vendor category is designed to meet those bars by default.</li>
<li>Eight controls, one afternoon: inventory the bots, write the decision into the AI acceptable use policy, kill calendar auto-join, give notice at the top of every call, name the prohibited meetings, confirm the bot has left before you keep talking, fix contract and retention settings, and file the vendor for periodic review.</li>
</ul>
</div>

## What happened last week?

Two events, one day apart, involving two different products.

On August 12, 2026, Lindsay Waninger filed suit against Marathon Engineering & Environmental Services in New Jersey Superior Court. According to the complaint as reported by Law360 on August 14 and by employment counsel Mark A. Saloman at Mondaq on August 19, she had been with the company for under three months when she was terminated over video. The meeting was being transcribed by Fireflies. After she left the call, her supervisors stayed on and discussed what their "ideal person" for the role looked like. One allegedly answered: hopefully a relatively strapping young man. Fireflies transcribed that too, then sent Waninger a link to the full transcript. She is suing for gender discrimination, and the transcript is the centerpiece.

Nobody at Marathon decided to record that conversation. Nobody decided to send it to her. The tool did what it was configured to do, which is capture everything until the meeting closes and share the output with everyone on the invite.

On August 13, 2026, Judge Eumi K. Lee issued her order on Otter.ai's motion to dismiss in In re Otter.AI Privacy Litigation, a consolidated class action in the Northern District of California that bundles four suits filed between August and September 2025. The lead case, Brewer v. Otter.ai, was brought by a California resident who says his February 2025 sales call was recorded because someone else on the call had Otter's Notetaker running. He never signed up for Otter, was never asked for consent, and alleges his conversation was used to train Otter's speech recognition models.

![Timeline of four AI meeting assistant lawsuits from August 2025 to August 2026: Brewer v. Otter.ai filed, Cruz v. Fireflies.AI filed, Waninger v. Marathon Engineering filed, and the Otter.AI motion to dismiss ruling](/blog/images/2-ai-meeting-assistant-lawsuit-timeline.png)

The court let the core claims proceed. Under the federal Electronic Communications Privacy Act, the California Invasion of Privacy Act, the Illinois Biometric Information Privacy Act and California's Unfair Competition Law, the plaintiffs had pleaded enough. Claims under the Computer Fraud and Abuse Act, California's computer-access statute and the Washington Privacy Act were dismissed, most with leave to amend, and the plaintiffs have fourteen days to try again.

A motion-to-dismiss ruling is not a finding that Otter broke the law. It is a finding that the plaintiffs' theory is legally coherent enough to go to discovery. That theory is the part small businesses should read twice.

## Why does it matter whether the bot is a "tool" or a "third party"?

Because the whole consent model for meeting assistants rests on it.

Under federal law and in the majority of states, one-party consent is enough to record a conversation. 18 U.S.C. 2511(2)(d) says a participant can record without telling anyone else. Vendors have built on that assumption: the host consented by turning the bot on, so the recording is lawful. Otter's terms of service tell account holders to make sure they have the necessary permissions, which pushes the question back onto the customer.

The plaintiffs argue something different. The bot is not the host's notebook. It is a separate company's software, joining as its own participant, transmitting the audio to that company's servers, and using the content for that company's commercial purposes, including model training. If that is right, then in California, Illinois, Florida, Pennsylvania, Washington and the other all-party-consent states, every attendee had to agree, and none of them did. Even in one-party states, a third party who was never invited and never consented is intercepting a communication under the federal statute.

Judge Lee found that theory sufficiently pleaded to survive. It is now the working assumption for every plaintiff's lawyer who reads the order, and it applies to any product that fits the pattern, not to Otter specifically.

The Fireflies case adds a layer. Cruz v. Fireflies.AI, filed December 18, 2025 in the Central District of Illinois, is not about recording at all. It is about what the tool builds from the recording. Fireflies' speaker-recognition feature, the complaint alleges, generates a voiceprint for each participant so it can label who said what. A voiceprint is a biometric identifier under 740 ILCS 14/10. BIPA requires written notice, written consent, and a public retention and destruction schedule before a private entity collects one, and the complaint says none of that happened for people who never created a Fireflies account.

## What does the bot actually do with your call?

The Marathon facts are worth walking through mechanically, because the failure was not exotic. It was default behavior.

![Data flow diagram showing a meeting on Zoom, Teams or Meet captured by an AI note-taker bot and sent to the vendor cloud for transcript storage, voiceprint creation, model training and automatic sharing, with the compliance consequences for PHI, CUI, client confidences and all-party-consent states](/blog/images/3-ai-meeting-assistant-data-flow-diagram.png)

A note-taker typically arrives one of two ways. Someone connects it to their calendar and it auto-joins anything with a video link, or the platform's built-in assistant is enabled at the account level. Either way, it joins as a participant. Attendees who did not set it up may see a small tile with the bot's name and may not.

It captures audio and produces a live transcript. Most products also identify speakers, which is where speaker recognition and voiceprints come in. When the meeting closes, it generates a summary and, depending on settings, distributes the transcript and summary to attendees, to the host's team, or to a shared workspace. It does not stop when the substantive part of the meeting ends. It stops when the meeting is closed.

Everything it captures rests on the vendor's infrastructure under the vendor's retention terms. Whether the vendor trains models on it depends on the plan tier and the settings, and in the Otter case whether customers were told is part of what is being litigated.

Three of those steps produced the Marathon lawsuit: capture continued after the subject of the meeting left, the content included an unguarded management conversation, and auto-distribution sent it to the one person who could use it. Every one of those is a setting or a habit, and none of them requires an attacker.

## What does this mean for a healthcare practice, a defense subcontractor, or a law firm?

The wiretap and biometric exposure applies to any business with a Zoom account. Regulated firms have a second layer, and it does not depend on how the litigation comes out.

For a covered entity or business associate under HIPAA, a note-taker that captures a call where a patient is present, or where staff discuss an identifiable patient, has received protected health information. Under 45 CFR 164.502(e) and 164.308(b), that is permitted only if the vendor is a business associate under a signed agreement. Some vendors offer a BAA on specific enterprise tiers. The free or team plan someone connected to their calendar almost certainly is not one of them. Absent a BAA, the disclosure is impermissible, and the risk analysis required by 164.308(a)(1)(ii)(A) has to reflect a new location where ePHI now lives. Our post on [whether ChatGPT is HIPAA compliant]({% post_url 2026-07-23-is-chatgpt-hipaa-compliant %}) walks through the same logic for chat tools; the meeting assistant version is stricter because the capture is passive and covers everyone on the line.

For a defense subcontractor, the question is where CUI goes. DFARS 252.204-7012(b)(2)(ii)(D) requires that any external cloud service provider used to store, process or transmit covered defense information meet the FedRAMP Moderate baseline or equivalent. A consumer note-taker on a call where a prime's technical requirements, drawings or delivery schedules are discussed is a cloud service processing CUI. It was not scoped, it is not in the SSP, and it almost certainly does not carry FedRAMP Moderate. That is a 7012 problem today, regardless of the CMMC Phase 2 pause. The framework in our post on [using AI tools with CUI]({% post_url 2026-08-04-ai-tools-cui-compliance %}) applies directly.

For a law firm, ABA Formal Opinion 512, issued July 29, 2024, says the duties of competence under Model Rule 1.1 and confidentiality under Rule 1.6 reach generative AI tools, including an obligation to understand how the tool handles client information before using it. A transcript of a privileged call sitting on a third-party vendor's servers, with training and retention terms the lawyer never read, is a Rule 1.6 question. Whether the presence of a third-party bot affects privilege in a given jurisdiction is a question for litigation counsel, and it is a better question to answer before a court asks it.

For CPA firms, tax preparers and anyone else under the FTC Safeguards Rule, 16 CFR 314.4(f) requires oversight of service providers that touch customer information. A note-taker on client calls is a service provider. It belongs in the same file as the rest of them, which is the argument of our post on [AI vendor due diligence]({% post_url 2026-08-09-ai-vendor-due-diligence %}).

## What are the eight controls?

None of this requires banning the tools. It requires deciding, in writing, how they are used, and closing the defaults that produced the Marathon transcript.

![Eight-item AI meeting assistant checklist for a firm under 50 people: inventory, decide and document, kill auto-join, consent at the top of the call, prohibited meetings, end recording before continuing, contract and settings, review the vendor](/blog/images/4-ai-meeting-assistant-policy-checklist.png)

1. **Inventory.** List every note-taker in use, both standalone bots and built-in platform features. Check the OAuth grants in Google Workspace and Microsoft 365 for calendar and meeting scopes; that is where the auto-join connections live. NIST AI RMF GOVERN 1.6 asks for a mechanism to inventory AI systems, and this is the AI system your firm is least likely to have on the list.
2. **Decide, then write it down.** One approved tool, or none. Put the decision in the AI acceptable use policy so it survives the person who made it.
3. **Kill the auto-join.** Disconnect calendar integrations that let a bot join every meeting. A bot that appears everywhere is a consent problem everywhere.
4. **Consent at the top of the call.** Verbal notice that the meeting is being transcribed, captured on the recording, plus a line in the invite. This is what all-party states require and it costs nothing in the states that do not.
5. **Prohibited meetings.** Name them in the policy: terminations, HR investigations, patient encounters, privileged calls, CUI discussions, board deliberations. No AI capture, no exceptions.
6. **End the recording, then keep talking.** Confirm the bot has left, or the meeting is closed, before any post-meeting conversation. This is the entire Marathon lesson in one sentence.
7. **Contract and settings.** BAA if PHI is possible. FedRAMP status if CUI is possible. Training opt-out where the vendor offers one. Retention set to the shortest workable window. Distribution set to the host only, not to all attendees.
8. **Review the vendor, not just the user.** Add the tool to the vendor due diligence file and re-check when it ships a new feature, because these products change fast.

If you need the governing document rather than a one-off sweep, the [AI Acceptable Use Policy Kit](https://payhip.com/b/AKSw2) ($47) covers meeting and recording tools alongside the chat, vendor and subprocessor sections. Our post on [building an AI acceptable use policy]({% post_url 2026-07-07-ai-acceptable-use-policy-small-business %}) explains what a small business actually needs in it.

## What this looks like at a 30-person firm

A 30-person engineering firm with two DoD subcontracts runs Teams for internal meetings and whatever the client uses for external ones. In April, a project manager connected Fireflies to her calendar for the summaries. Since then it has joined every meeting on her calendar, including two prime-contractor design reviews and a call with HR about a performance issue.

The sweep takes an hour. The OAuth grant shows up in the Microsoft 365 admin center. The Fireflies workspace has forty-one transcripts, eleven of them from external calls, and the retention setting is the default. Two of the transcripts contain drawing numbers and delivery dates from a CUI-marked statement of work.

The remediation is not dramatic. Revoke the grant. Export and delete the transcripts, and document that you did. Decide whether the firm wants a note-taker at all; if yes, choose one, put it on the approved list with the settings locked, and confirm in writing what it does with CUI. Add the prohibited-meeting list to the AI policy. Tell everyone that meetings end when the host closes them, not when the agenda does. Then write a dated note into the SSP and the risk register describing what was found and what was fixed.

Total effort is an afternoon. What it buys is that the next Fireflies transcript, if there is one, was authorized, scoped and configured by someone who decided it should exist.

## The bottom line

The AI note-taker was the easiest tool in the building to adopt and the hardest one to see. Two courts spent last week explaining what that costs: a transcript that becomes Exhibit A, and a legal theory that treats the bot as a stranger who was never invited to the call. The regulated version of the same problem is already settled law. HIPAA wants a BAA. DFARS 7012 wants FedRAMP Moderate. BIPA wants notice and a retention schedule. None of them care that nobody meant to turn it on.

## Sources

- Law360, "Ex-Marathon Worker Says AI Caught Her Bosses' Gender Bias," August 14, 2026, reporting Waninger v. Marathon Engineering & Environmental Services Inc., N.J. Superior Court, filed August 12, 2026.
- Mark A. Saloman, "Virtual Termination Meetings and AI: When Skynet Does Not Stop," Mondaq, August 19, 2026.
- In re Otter.AI Privacy Litigation, No. 5:25-cv-06911-EKL (N.D. Cal.), Order on Motion to Dismiss, Dkt. 68, August 13, 2026 (Lee, J.). Consolidates Brewer v. Otter.ai Inc. (filed August 15, 2025) and three related actions.
- Cruz v. Fireflies.AI Corp., No. 3:25-cv-03399 (C.D. Ill.), complaint filed December 18, 2025.
- 18 U.S.C. 2511(2)(d) (one-party consent) and 18 U.S.C. 2520(c)(2) (civil damages), Electronic Communications Privacy Act.
- Cal. Penal Code 632 (confidential communications) and 637.2 (civil action), California Invasion of Privacy Act.
- 740 ILCS 14/10, 14/15 and 14/20, Illinois Biometric Information Privacy Act.
- 45 CFR 164.502(e), 164.308(a)(1)(ii)(A) and 164.308(b), HIPAA Privacy and Security Rules, Electronic Code of Federal Regulations.
- DFARS 252.204-7012(b)(2)(ii)(D), Safeguarding Covered Defense Information and Cyber Incident Reporting, cloud service provider requirements.
- 16 CFR 314.4(f), FTC Standards for Safeguarding Customer Information, service provider oversight.
- ABA Standing Committee on Ethics and Professional Responsibility, Formal Opinion 512, Generative Artificial Intelligence Tools, July 29, 2024.
- NIST AI 100-1, Artificial Intelligence Risk Management Framework (AI RMF 1.0), GOVERN 1.6 and GOVERN 6.1, January 2023.
