---
layout: post
title: "Your SPRS Score Is Wrong and You Just Found Out. The Next 30 Days Decide Whether It Is a Correction or a False Claim."
date: 2026-09-14
description: "What a defense contractor does the day it discovers a past NIST 800-171 representation was wrong: the False Claims Act knowledge standard after SuperValu, the FAR mandatory disclosure rule at 9.406-2, DOJ cooperation credit under Justice Manual 4-4.112, and a 30-day ladder from discovery to decision."
category: CMMC
tags: [CMMC, NIST 800-171, SPRS, False Claims Act, FAR 52.203-13, mandatory disclosure, DOJ cooperation credit, Justice Manual 4-4.112, SuperValu, LOGZONE, Honeywell, defense contractors]
image: /blog/images/1-sprs-score-wrong-self-disclosure-hero.png
author: CyberZ
---

*Every CMMC guide tells you how to get the score right. Almost none tell you what to do the morning you learn it was wrong. That morning has its own set of rules, and they start running immediately.*

**A wrong SPRS score becomes a False Claims Act problem at the moment the contractor knows it is wrong and keeps invoicing anyway. Under 31 USC 3729(b)(1), "knowingly" covers actual knowledge, deliberate ignorance, and reckless disregard, and the Supreme Court's 2023 SuperValu decision made liability turn on what the contractor subjectively believed when each claim went out. Discovery converts an honest error into knowledge. From that day, a principal's failure to timely disclose credible evidence of a violation is an independent cause for debarment under FAR 9.406-2(b)(1)(vi), while voluntary self-disclosure earns cooperation credit under Justice Manual 4-4.112. The 30 days after discovery are where the outcome is decided.**

<div class="key-takeaways" style="border-left:4px solid #EE4C48;background:#15151a;padding:18px 24px;margin:28px 0;border-radius:6px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;">
<li>An honest wrong score is not fraud. The False Claims Act punishes knowing falsity, and after SuperValu (June 2023) "knowing" means what you actually believed when you submitted the claim. Discovery is the pivot: every invoice after it is the exposure, not the ones before.</li>
<li>The FAR mandatory disclosure rule survived the FAR overhaul. FAR 9.406-2(b)(1)(vi) makes a principal's knowing failure to timely disclose credible evidence of a civil False Claims Act violation a cause for debarment, whether or not FAR 52.203-13 sits in your contract, for three years after final payment.</li>
<li>DOJ pays for candor. Justice Manual 4-4.112 calls voluntary self-disclosure the most valuable form of cooperation. Consolidated Nuclear Security self-disclosed in 2024 and settled at roughly 1.1 times single damages. LOGZONE and Honeywell, both whistleblower cases, paid $507,144 and $2,042,518 with no such credit.</li>
<li>Not every gap is "credible evidence" of a violation. One control that drifted is a correction. A near-perfect score posted over an environment that never resembled it is a different category, and that call belongs to counsel, made on a dated record.</li>
<li>The 30-day ladder: date the discovery, fix the control and re-score, post the corrected score, get counsel's read on credible evidence, brief the affirming official, and disclose if the answer is yes.</li>
</ul>
</div>

## Why the discovery date matters more than the score

The [September 6 walkthrough]({% post_url 2026-09-06-how-to-improve-sprs-score %}) covered how to raise a score legitimately and how to document each regained point. This post starts one step earlier, at the moment a contractor learns that a score already sitting in SPRS, or a statement already signed by the affirming official, does not describe the environment.

That moment arrives in ordinary ways. A new IT hire runs the first real inventory and finds a file server nobody scoped. A vendor audit shows the MFA rollout never reached the shop floor. A prime's questionnaire asks for a FIPS validation certificate that does not exist. None of these is a scandal. Each is a discovery, and the False Claims Act treats discovery as a legal event.

The statute reaches anyone who "knowingly presents, or causes to be presented, a false or fraudulent claim for payment" (31 USC 3729(a)(1)(A)) or knowingly makes a false record material to such a claim. The definition of "knowingly" in 3729(b)(1) is the part contractors need to read twice. It requires no specific intent to defraud. It is satisfied by actual knowledge, by deliberate ignorance of the truth, or by reckless disregard of it.

In June 2023 the Supreme Court decided *United States ex rel. Schutte v. SuperValu Inc.* unanimously, and held that FCA scienter refers to the defendant's own knowledge and subjective beliefs at the time the claim was submitted, not to what a hypothetical reasonable person could have known. Two consequences follow for a contractor with a wrong SPRS score. First, a score posted in good faith, on the basis of a self-assessment the company believed at the time, is not a knowing false statement, even if it was wrong. Second, the day the company learns the score is wrong, its subjective belief changes, and every invoice submitted after that day under a contract that requires the score is submitted with knowledge.

That is why the discovery date is the single most important fact in the file. It draws the line between invoices submitted in honest error and invoices submitted knowing the representation behind them was false.

![Three rules that begin operating on the day a contractor learns its NIST 800-171 representation was wrong: the False Claims Act knowledge standard, the FAR debarment cause for failing to disclose, and DOJ's cooperation credit policy](/blog/images/2-sprs-score-wrong-three-rules-fca-far-doj.png)

## The two settlements that show both sides of the line

The Department of Justice spent this summer demonstrating what the wrong side of the line costs. In June 2026, LOGZONE Inc., an Alabama defense contractor, agreed to pay $507,144 to resolve allegations that it posted a self-assessed score of 110 in October 2021 and left it standing while DIBCAC's own assessment in 2024 produced a score of negative 170. On September 1, 2026, Honeywell Aerospace agreed to pay $2,042,518 over NIST SP 800-171 noncompliance on a single network between April 2020 and December 2023, in a case brought by a former employee who collects $375,823 as her share. The [Honeywell breakdown]({% post_url 2026-09-02-honeywell-fca-cybersecurity-settlement %}) walks the mechanics.

Neither case involved a breach. Both ran on the gap between a representation and reality, sustained over time, with claims for payment flowing throughout. In both, the government learned about the gap from someone other than the contractor.

Compare Consolidated Nuclear Security. In April 2024, CNS agreed to pay $18.4 million to resolve allegations that technicians at the Pantex plant billed hours they had not worked. The conduct was not cybersecurity, but the procedural posture is the lesson. CNS discovered the problem internally, disclosed it to the government, terminated the personnel involved, and cooperated with the investigation. The settlement agreement credited CNS under DOJ's disclosure, cooperation, and remediation guidelines. Of the $18.4 million, roughly $16.6 million was restitution, meaning single damages. DOJ applied a multiplier of about 1.1 to a statute that authorizes treble damages and to a settlement practice that routinely lands at double.

Same statute. One contractor waited to be found and paid the whistleblower's share on top. Another found itself first and paid something close to what it owed.

## What the FAR requires once you know

The False Claims Act sets the penalty for silence. The Federal Acquisition Regulation sets a separate, affirmative obligation to speak, and it has been on the books since December 2008.

FAR 52.203-13, Contractor Code of Business Ethics and Conduct, requires a contractor to timely disclose to the agency Office of Inspector General, in writing, whenever it has credible evidence that a principal, employee, agent, or subcontractor has committed a violation of the civil False Claims Act in connection with the award, performance, or closeout of the contract. Under FAR 3.1004 the clause is prescribed for contracts above a dollar threshold in the $6 million range with a performance period over 120 days, which means a good number of small-contractor awards do not carry the clause text at all. That is exactly why the next paragraph matters.

Contractors without the clause are not off the hook. FAR 3.1003(a)(2) states that whether or not 52.203-13 applies, a contractor may be suspended or debarred for a principal's knowing failure to timely disclose credible evidence of a civil FCA violation, and FAR 9.406-2(b)(1)(vi) lists that failure as a cause for debarment that persists until three years after final payment on the contract. Wiley's analysis of the Revolutionary FAR Overhaul class deviations notes the disclosure obligation in 52.203-13 was retained with only a slight tweak, and the current acquisition.gov text of 9.406-2, effective under FAC 2026-01, still carries the failure-to-disclose cause.

Two terms in that rule are undefined, and the HHS Office of Inspector General's contractor self-disclosure FAQ, which applies the same FAR language, is candid about both. "Credible evidence" is not defined, though the FAR Council's rulemaking discussion described it as a higher standard than "reasonable grounds to believe," implying the contractor may take some time for a preliminary examination before deciding to disclose. "Timely" is not defined either; what counts as timely is ultimately decided by the suspension and debarment official. A contractor is therefore expected to look before it reports, and expected not to look forever.

For the Department of War, disclosures go to the DoD Office of Inspector General's Contractor Disclosure Program, which accepts written submissions from an authorized representative of the contractor. A disclosure from someone not authorized to speak for the company is treated as a tip.

## What DOJ gives back for disclosure

On May 6, 2019, the Civil Division added section 4-4.112 to the Justice Manual, formalizing how FCA defendants earn credit. The section names three routes: voluntary self-disclosure, cooperation with an investigation, and remedial measures. The press release announcing the policy quoted the Assistant Attorney General calling voluntary disclosure "the most valuable form of cooperation."

The mechanics matter to a small contractor because the credit is expressed in the multiplier. The statute permits three times the government's damages plus per-claim civil penalties. Under 4-4.112, DOJ attorneys may exercise discretion to reduce the penalties or the damages multiple sought when a defendant discloses proactively, identifies the individuals involved, preserves and turns over documents, makes people available, and fixes the underlying problem. Partial credit is available for partial cooperation. Maximum credit generally requires timely self-disclosure, full cooperation, and remedial steps designed to prevent and detect the same conduct going forward.

Two features of the section deserve attention from anyone who signs a CMMC affirmation. The first is that disclosure of misconduct discovered during an internal investigation, beyond what the government already knew, also qualifies for credit. If a review prompted by one wrong control turns up three more, disclosing all four is credited; disclosing one and hoping is not. The second is a footnote: the Department may take into account the prior existence of a compliance program in evaluating whether a violation was committed knowingly. A contractor that can show a documented self-assessment process, a dated SSP, and a running evidence trail is not only better positioned on damages. It is better positioned on the question of whether there was a knowing violation at all.

## Not every gap is credible evidence of a violation

Nothing above means a contractor should run to the Inspector General every time a control drifts. The FAR rule is triggered by credible evidence of an FCA violation, and an FCA violation requires a knowing false claim that is material to payment. A single control that lapsed between self-assessments, discovered and fixed within the normal maintenance cycle, is a correction, not a disclosure event. DFARS 252.204-7019 has always allowed a contractor to post an updated score at any time, and the [affirmation liability analysis]({% post_url 2026-08-23-cmmc-affirmation-false-claims-act %}) made the point that a current, honest, lower score is far safer than a stale high one.

The question changes character when the discovery reveals that the score never described the environment. A 110 posted over a network that had no MFA, no FIPS-validated encryption, and no incident response capability is not a control that drifted. It is a representation that was wrong when made, and the contractor now has to ask whether the person who made it knew, deliberately avoided knowing, or recklessly disregarded the truth. If the answer to any of those is plausibly yes, and invoices went out under contracts requiring the score, the contractor is now holding what a suspension and debarment official may well consider credible evidence.

That judgment is a legal one and should be made by government contracts counsel, on a record that shows when the company learned what. Counsel will also handle a second question this post does not answer: whether the prime contractor's flow-down or the contract's own terms create a separate notification duty, independent of the FAR rule.

![A 30-day sequence from the date of discovery through fixing the control, posting a corrected SPRS score, obtaining counsel's assessment of credible evidence, and briefing the affirming official](/blog/images/3-sprs-score-wrong-30-day-correction-ladder.png)

## The 30-day ladder

The following sequence is written for a 15-to-50 person contractor with CUI on its network and no in-house lawyer. It is a sequence, not a menu, because the order is what protects the discovery date.

**Day 0: write down what you found and when.** A dated memo, even an email to yourself and the affirming official, that describes the gap in plain terms. This document is the foundation of everything that follows. It fixes the discovery date, and it is the first item counsel will ask for.

**Week 1: fix the control, or start.** Some gaps close in a day; a missing MFA enforcement policy can be turned on. Some take months; FIPS-validated encryption across a fleet of laptops is a procurement project. Either way, the remediation starts now, with tickets, configuration screenshots, and purchase orders dated after the discovery memo. This is the remediation prong of 4-4.112, and it is also the fastest way to shorten the window of knowing noncompliance.

**Week 2: re-run the self-assessment and post the corrected score.** Use the DoD Assessment Methodology exactly as written, including the 5-3-1 point weights and the partial credit rules for 3.5.3 and 3.13.11. Post the number the methodology produces, even if it is embarrassingly lower than the one it replaces. A contractor that posts a corrected score two weeks after discovery has a very different story than one that waited a year. MORSECORP's $4.6 million settlement in March 2025 was, according to DOJ's press release, the first built on a failure to promptly update the SPRS score after a lower third-party result.

**Week 3: get counsel's read on credible evidence.** Bring the discovery memo, the old and new scores, the SSP as it stood at the time of the old score, and a list of every contract and invoice that required the score during the gap. Ask two questions. Does this rise to credible evidence of a knowing false claim? If it does, which OIG, and in what form? If the answer is that this was an honest error corrected promptly, get that conclusion in writing and file it with the discovery memo.

**Week 4: brief the affirming official, and disclose if the answer was yes.** Whoever signs the annual affirmation under 32 CFR 170.22 needs to see the discovery memo, the corrected score, and counsel's conclusion before signing anything else. If counsel concluded disclosure is warranted, the submission goes to the DoD OIG Contractor Disclosure Program from an authorized officer, in writing, with the remediation already underway. A disclosure that arrives with a corrected score and a fix in progress reads very differently from one that arrives with a problem and a promise.

## The bottom line

The False Claims Act does not punish being wrong. It punishes knowing and continuing. That line runs through the discovery date, and the Supreme Court has made clear that the contractor's own knowledge at the time of each claim is what counts. On one side of the line, a wrong score is an error with a fix. On the other side, it is a series of knowing false claims, each invoice a fresh one, with a FAR rule that makes silence its own offense and a DOJ policy that rewards the contractor who speaks first. CNS paid something close to single damages. LOGZONE and Honeywell paid a multiple and a whistleblower's share. The only difference in posture was who told the government, and when.

If the immediate job is producing a corrected score you can defend, the [NIST 800-171 SPRS Score Workbook for CMMC Level 2](https://payhip.com/b/R5g4Y) ($87) applies the DoD Assessment Methodology control by control, with the weights and partial-credit rules built in. If the discovery has exposed a wider gap, and counsel is going to ask for the SSP, the scoping decisions, the POA&M, and the evidence behind each control as they stood at each date, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) builds that record in one place. It is the file a contractor wants to have already when the question becomes what it knew and when.

## Sources

- 31 U.S.C. § 3729(a)(1) and (b)(1), False Claims Act liability and definition of "knowingly"
- *United States ex rel. Schutte v. SuperValu Inc.*, 598 U.S. 739 (2023), decided June 1, 2023
- FAR 52.203-13, Contractor Code of Business Ethics and Conduct; FAR 3.1003; FAR 9.406-2(b)(1)(vi) and 9.407-2(a)(8), acquisition.gov, FAC 2026-01
- Wiley Rein LLP, "FAR Overhaul Class Deviations," analysis of retained disclosure obligation under 52.203-13
- U.S. Department of Justice, Justice Manual § 4-4.112, "Guidelines for Taking Disclosure, Cooperation, and Remediation into Account in False Claims Act Matters," May 6, 2019, and accompanying press release
- HHS Office of Inspector General, Contractor Self-Disclosure FAQs (interpreting "credible evidence" and "timely" under the FAR rule)
- U.S. Department of Justice, press release, Consolidated Nuclear Security LLC False Claims Act settlement ($18.4 million), April 23, 2024; settlement agreement crediting disclosure, cooperation, and remediation
- U.S. Department of Justice, press release, LOGZONE Inc. False Claims Act settlement ($507,144), June 2026
- U.S. Department of Justice, press release, Honeywell Aerospace Inc. False Claims Act settlement ($2,042,518), September 1, 2026
- U.S. Department of Justice, press release, MORSECORP Inc. False Claims Act settlement ($4.6 million), March 26, 2025
- DFARS 252.204-7012 and 252.204-7019; DoD Assessment Methodology for NIST SP 800-171; 32 CFR 170.22
