---
layout: post
title: "Honeywell's $2M Cybersecurity Settlement: One Network, One Whistleblower, Four Years of Exposure"
date: 2026-09-02
description: "DOJ announced September 1 that Honeywell Aerospace will pay $2,042,518 to settle False Claims Act allegations over NIST SP 800-171 noncompliance on a single network. The whistleblower was a former employee who filed in 2022 and collects $375,823. What the timeline, the scope, and the spin-off wrinkle mean for small defense contractors."
category: CMMC
tags: [False Claims Act, Honeywell, NIST 800-171, DFARS 252.204-7012, whistleblower, qui tam, CMMC pause, DOJ settlement, defense contractors, CUI]
image: /blog/images/1-honeywell-fca-settlement-nist-800-171-hero.png
author: CyberZ
---

*The Justice Department opened September with a name everyone recognizes. Not a 30-person machine shop this time. Honeywell. And the person who reported the gap was not a competitor or an auditor. She worked there.*

**On September 1, 2026, the Department of Justice announced that Honeywell Aerospace Inc. agreed to pay $2,042,518 to resolve False Claims Act allegations that a business unit of Honeywell International failed to comply with NIST SP 800-171 cybersecurity requirements on one of its networks from April 2020 through December 2023, while submitting claims for payment on a U.S. Department of Defense contract. The case began as a whistleblower lawsuit filed in 2022 by Rachel Tenney, a former Honeywell employee, who receives $375,823 as her share of the settlement. There is no breach in the allegations. The noncompliance itself, paired with invoices, was the claim.**

<div class="key-takeaways" style="border-left:4px solid #EE4C48;background:#15151a;padding:18px 24px;margin:28px 0;border-radius:6px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;">
<li>Honeywell Aerospace pays $2,042,518 to settle allegations of NIST SP 800-171 noncompliance on a DoD contract between April 2020 and December 2023. The claims are allegations only, with no determination of liability.</li>
<li>The whistleblower was a former Honeywell employee. She filed under the False Claims Act's qui tam provisions in 2022 and collects $375,823, roughly 18 percent of the settlement.</li>
<li>The allegations involve one network. Not the whole company. A single system that fell short of the contract's cybersecurity requirements was enough to support an FCA case.</li>
<li>Honeywell Aerospace became a standalone public company on June 29, 2026, and is paying for conduct from its time as a Honeywell International business unit. Spinning off did not shed the liability.</li>
<li>This is the second cyber False Claims Act settlement announced during the CMMC pause, after LOGZONE in June. Neither one needed CMMC to exist. DFARS 252.204-7012 and the FCA did the work.</li>
</ul>
</div>

## What DOJ announced on September 1

The press release is short and unusually clean. Honeywell Aerospace Inc., headquartered in Phoenix, agreed to pay $2,042,518 to resolve its False Claims Act liability. The allegations: from April 2020 through December 2023, a business unit of Honeywell International Inc. submitted claims for payment on a Department of Defense contract while failing to comply with cybersecurity requirements specified in NIST Special Publication 800-171, with respect to one of Honeywell's networks, as the contract and regulation required.

Assistant Attorney General Brett Shumate's statement repeats, almost word for word, what the Civil Division said when LOGZONE settled in June: contractors that obtain defense information must follow the required cybersecurity standards, and the Department will keep investigating violations.

The case is captioned *United States ex rel. Rachel Tenney v. Honeywell International Inc.*, No. 3:22-cv-129, in the Western District of North Carolina. The Defense Criminal Investigative Service assisted. As with every FCA settlement, the claims resolved are allegations only, and there has been no determination of liability.

Those are the facts. The lessons for a small contractor are in three details most coverage will skip: the timeline, the phrase "one of Honeywell's networks," and the date June 29, 2026.

## The timeline is the uncomfortable part

![Timeline of the Honeywell False Claims Act case from April 2020 conduct window through the September 2026 settlement](/blog/images/2-honeywell-fca-settlement-timeline-2020-2026.png)

Lay the dates out and the case stops looking like a news item and starts looking like a warning about how this liability actually behaves.

The conduct window opens in April 2020. The whistleblower files suit in 2022, under seal, as the False Claims Act's qui tam procedure requires (31 U.S.C. 3730(b)). Qui tam complaints stay sealed for at least 60 days while the government investigates, and courts routinely extend that seal for years. The conduct window DOJ settled runs through December 2023, which means claims were still being submitted after the lawsuit existed. The settlement arrives September 1, 2026.

That is a six-year arc from first alleged noncompliance to payment, and roughly four years from filing to resolution. For part of that period, the company was accumulating exposure on a case it may not have known existed, because the seal works exactly that way.

Now map that onto the present moment. The CMMC Reform Task Force reports this month. Plenty of contractors have quietly slowed their NIST 800-171 work since the July 13 suspension, reasoning that the rules are in flux. The Honeywell timeline says the invoices you submit during a "wait and see" year are not neutral. Each one is a claim, and a claim paired with a known gap is the raw material of an FCA case that surfaces in 2029 or 2030. The conduct being settled today is from 2020 to 2023. The conduct being generated today gets settled at the end of the decade.

## "One of Honeywell's networks"

The settlement language is specific: the failure was on one network. Honeywell International operated at a scale of hundreds of thousands of employees and, presumably, an enterprise security program that a 12-person machine shop can only dream about. None of that mattered, because FCA exposure does not average across your environment. It attaches to the specific system where covered defense information lived and the specific requirements the contract imposed there.

Small contractors make the mirror-image version of this mistake constantly. The main network gets the attention, and the exceptions accumulate: the engineering workstation that never joined the domain, the file share from the old office, the dev server someone stood up during a deadline crunch, the machine in the shop that runs the CNC software and quietly stores drawings. The reasoning is always that the "real" environment is compliant, so the edge case is noise.

Honeywell's settlement prices the edge case at $2,042,518. If your CUI boundary has systems you have mentally excluded without documenting why, that is not a scoping decision, it is a gap with an invoice attached. We walked through how to make exclusion decisions defensible in [Why Your CMMC Timeline Is a Scoping Decision, Not a Controls Problem]({% post_url 2026-07-19-cmmc-scoping-decision-not-controls %}).

## The whistleblower worked there. They usually do.

Rachel Tenney is a former Honeywell employee. Her share is $375,823, about 18 percent of the settlement, squarely inside the 15 to 25 percent range the statute guarantees relators when the government intervenes (31 U.S.C. 3730(d)).

If that pattern sounds familiar, it should. The MORSECORP settlement in March 2025, still the reference case for SPRS score liability, was filed by MORSE's own Head of Security, who collected roughly $851,000 of the $4.6 million settlement, a nearly identical 18.5 percent cut. DOJ officials said in January 2026 that whistleblower-driven cyber cases keep climbing, with $52 million recovered across nine cybersecurity FCA settlements in fiscal year 2025 alone.

![Recent cybersecurity False Claims Act settlements compared: Raytheon and Nightwing 8.4 million, MORSECORP 4.6 million, Honeywell 2 million, LOGZONE 507 thousand](/blog/images/3-cyber-fca-settlements-2025-2026-comparison.png)

The operational lesson is blunt. The person most likely to end your company's FCA innocence already has a badge to your building. They sat in the meeting where the MFA rollout got deferred again. They wrote the ticket about the unpatched server that got closed as "won't fix." Every internal security complaint your company shrugs off is a draft of a qui tam complaint with a six-figure incentive attached to finishing it.

That does not mean treating employees as threats. It means the opposite: treating internal security concerns as legal events that get logged, investigated, answered in writing, and either fixed or formally risk-accepted by someone with authority. Whistleblowers file when they are ignored. The paper trail that protects you and the culture that keeps people from needing the statute are the same thing.

## The spin-off wrinkle: liability travels

One line in the DOJ release deserves more attention than it will get. Honeywell Aerospace became a standalone public company on June 29, 2026. The conduct settled is from its years as a business unit of Honeywell International. The new entity pays anyway.

This echoes the Raytheon settlement, where Raytheon companies and Nightwing Group, the buyer of the relevant business, together paid $8.4 million for pre-acquisition cybersecurity failures. The FCA does not care about your org chart's revision history. Noncompliance travels through spin-offs, carve-outs, and acquisitions, and it surfaces years later on the successor's books.

For a small contractor, this cuts two ways. If you are hoping an acquisition or restructuring puts distance between you and old compliance gaps, it will not. And if you are the buyer of a defense business, the target's NIST 800-171 history, its SPRS score record, and the honesty of its past attestations belong in due diligence next to the financials, because you may be purchasing a sealed qui tam complaint along with the customer list.

## Second settlement of the pause, and CMMC appears nowhere

Read the Honeywell release again and notice what is missing: any mention of CMMC. Same with LOGZONE in June, where a DCMA assessment found a score of -170 on the -203 to 110 scale and the company paid $507,144.

Both cases run entirely on the machinery that predates CMMC and survives every pause, review, and task force: DFARS 252.204-7012 putting NIST SP 800-171 into the contract, the invoices you submit against that contract, and the False Claims Act connecting the two. The July 13 suspension paused third-party assessments. It did not pause a single word of the clause in your contract, and it visibly did not pause the Civil Division.

This is the same concentration of risk we mapped in [CMMC Affirmation and the False Claims Act: The Pause Left One Signature Holding All the Risk]({% post_url 2026-08-23-cmmc-affirmation-false-claims-act %}). Whatever the Task Force recommends this month, the Honeywell case was filed in 2022 and settled in 2026 without CMMC playing any role. The enforcement layer is not waiting for the reform. It is not even watching it.

## What a small contractor does with this, this week

None of this calls for panic. It calls for four specific pieces of hygiene, all cheaper than the smallest settlement on the board above.

**Inventory the exceptions, not the environment.** List every system that touches, stores, or could plausibly receive CUI and is not fully inside your protected boundary. For each one, either bring it in scope or write down, dated and signed, why it is out. "One of Honeywell's networks" is what an undocumented exception looks like after DOJ finds it.

**Make your score match reality.** Your SPRS score is a representation to the government, and MORSECORP established that letting a stale or inflated score sit there is itself the false claim. If you have not re-scored since your environment changed, do it against the actual DoD methodology. Our walkthrough of the math is in [How Your NIST 800-171 SPRS Score Is Calculated]({% post_url 2026-06-19-how-nist-800-171-sprs-score-calculated %}).

**Attach evidence to every "implemented."** A control you cannot prove was implemented in 2024 is, in a 2028 deposition, a control that was not implemented. Screenshots, configs, tickets, and dates, organized per control, are what turn your self-assessment from an opinion into a record. The approach is in [NIST 800-171 Self-Assessment Evidence: What Backs Your Score Now That No Assessor Is Coming]({% post_url 2026-07-22-nist-800-171-self-assessment-evidence %}), and the [CMMC Level 2 Evidence Tracker for NIST 800-171 Audit](https://payhip.com/b/LN2UB) ($67) is the tool I use to keep that record per control and per objective.

**Treat internal complaints as legal events.** Log every security concern an employee raises, respond in writing, and close it with a fix or a documented risk acceptance. If you are starting from scratch on the whole stack, scope, score, plan, and evidence together, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) bundles the SSP template, SPRS workbook, POA&M tracker, scoping worksheet, and evidence tracker into one working set, which is the difference between answering a DCMA request in an afternoon and answering it in a very bad month.

## The bottom line

Honeywell Aerospace paid $2,042,518 because one network allegedly fell short of NIST SP 800-171 while the invoices kept going out, and because an employee who saw it had a statute that pays. The company's size did not protect it, the spin-off did not shed it, and the CMMC pause was irrelevant to it. The case took four years from filing to settlement, which means the equivalent case against a contractor relaxing right now is already scheduled. It just has not been filed yet.

## Sources

- U.S. Department of Justice, [Honeywell Aerospace Inc. Agrees to Pay Over $2M to Settle False Claims Act Allegations of Failing to Comply with Cybersecurity Requirements in a U.S. Department of Defense Contract](https://www.justice.gov/opa/pr/honeywell-aerospace-inc-agrees-pay-over-2m-settle-false-claims-act-allegations-failing), September 1, 2026
- U.S. Department of Justice, [Alabama Defense Contractor Agrees to Pay $507,144 to Resolve False Claims Act Liability Relating to Cybersecurity Violations](https://www.justice.gov/opa/pr/alabama-defense-contractor-agrees-pay-507144-resolve-false-claims-act-liability-relating), June 18, 2026
- U.S. Department of Justice, [Defense Contractor MORSECORP Inc. Agrees to Pay $4.6 Million to Settle Cybersecurity Fraud Allegations](https://www.justice.gov/usao-ma/pr/defense-contractor-morsecorp-inc-agrees-pay-46-million-settle-cybersecurity-fraud), March 2025
- U.S. Department of Justice, [Raytheon Companies and Nightwing Group Pay $8.4M to Resolve False Claims Act Allegations](https://www.justice.gov/opa/pr/raytheon-companies-and-nightwing-group-pay-84m-resolve-false-claims-act-allegations-relating)
- 31 U.S.C. 3730, False Claims Act qui tam provisions (filing under seal, relator share)
- DFARS 252.204-7012, Safeguarding Covered Defense Information and Cyber Incident Reporting
- NIST Special Publication 800-171 Rev 2, Protecting Controlled Unclassified Information in Nonfederal Systems
