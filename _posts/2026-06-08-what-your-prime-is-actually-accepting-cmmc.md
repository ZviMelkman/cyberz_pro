---
layout: post
title: "What Your Prime Is Actually Accepting When They Say 'Be CMMC Certified by November 10'"
date: 2026-06-08
description: "A prime contractor's CMMC demand letter rarely means a full C3PAO audit by the deadline. Here is what a subcontractor actually has to show, and the three questions that decide it."
category: CMMC
tags: [CMMC, NIST 800-171, defense contractors, SPRS, subcontractors]
image: /blog/images/1-cmmc-prime-certified-november-10-2026.png
author: CyberZ
---

![CyberZ title graphic: what your prime is actually accepting by November 10, 2026, with the note that getting certified rarely means a full C3PAO audit](/blog/images/1-cmmc-prime-certified-november-10-2026.png)

*What your prime is actually accepting by November 10, 2026.*

The email lands in a 14-person machine shop's inbox. It is from the prime they have shipped parts to for nine years. The subject line is some version of "CMMC compliance required," and the body says the company needs to "be CMMC certified by November 10, 2026" to stay on the program.

Two reactions follow, and both are expensive.

The first is panic. The owner calls three vendors, hears that a Level 2 assessment runs somewhere between $80,000 and $150,000 and books twelve to eighteen months out, and starts writing checks against a requirement nobody has actually defined yet.

The second is paralysis. The letter goes in a drawer because the number is unthinkable, and the shop quietly drifts toward losing the contract by doing nothing.

Both reactions share the same root mistake: treating "be CMMC certified" as a single, known thing with one price tag and one deadline. It is not. What a prime will actually accept from a subcontractor by November 10 is more specific, more negotiable, and in most cases far less expensive than the panic number. You just have to know which questions to ask before you spend a dollar.

## The first question is not the deadline. It is whether CUI flows to you.

The most common error is assuming that because the prime has a CMMC obligation, you automatically inherit the same one. You do not. Your requirement is driven by the data the prime sends *you*, not by the prime's own status.

Two categories matter here. Federal Contract Information (FCI) is contract data that is not public but is not especially sensitive. If FCI is all you touch, the relevant requirement is the basic safeguarding rule at FAR 52.204-21, which maps to CMMC Level 1 and is self-assessed. Controlled Unclassified Information (CUI) is the sensitive tier, covered by DFARS 252.204-7012, and it is what triggers NIST SP 800-171 and CMMC Level 2.

The practical version of this distinction came up almost word for word in a recent r/CMMC thread. A prime being required to hold Level 2 does not automatically push that requirement onto every sub. Many primes flow Level 2 down anyway, as a blanket risk-management move, because it is the lower-effort path for them. But the real trigger is whether CUI actually reaches you. So the single most valuable question you can send back to the prime is this: *What CUI are you flowing to me, under what circumstances, so I can scope and handle it correctly?*

That one question does two things. It forces the prime to either confirm CUI is in play or admit it is not, which can drop your whole obligation from Level 2 to Level 1. And it puts the scoping conversation on record, which matters later when an assessor or a contracting officer asks how you defined your environment.

## Self-assessment or C3PAO: what November 10 actually changes

Assume CUI does flow and you are looking at Level 2. The next misread is believing that Level 2 always means a third-party audit. Today, it usually does not.

CMMC is rolling out in phases under the program rule at 32 CFR Part 170. Phase 1 began November 10, 2025, and runs through November 9, 2026. During this window, most Level 2 requirements that show up in solicitations are satisfied by a **self-assessment**: you evaluate yourself against all 110 controls, post a score, and the company affirms it. Phase 2 begins November 10, 2026, and that is the shift that has everyone anxious. From that date, contracting officers can require a Level 2 **C3PAO** certification, an assessment performed by a Certified Third-Party Assessment Organization, as a condition of award on prioritized contracts involving CUI. The driver clause is DFARS 252.204-7021.

"Can require" is not "always requires." Whether your specific contract demands a third-party assessment or accepts a self-assessment depends on the solicitation language and what the prime negotiates. A large share of subcontractors will continue to self-assess Level 2 for some time. The contractors who need a C3PAO are those on the prioritized, CUI-heavy work where the government wrote that requirement into the deal.

This is why the demand letter alone tells you almost nothing. "Be certified" could mean a self-assessment you can complete in-house, or a third-party audit that needs to be on a calendar now. You cannot price the requirement until you know which one applies, and you find that out by asking, not by guessing at the top of the range.

## What the prime will actually accept: scoped, scored, scheduled, and moving

![Two-column comparison: what the demand letter says, be CMMC certified by November 10, 2026, versus what the prime will actually accept, a defined scope, an honest SPRS score, a System Security Plan on file, and conditional certification or a booked C3PAO date plus a POA&M](/blog/images/2-cmmc-demand-letter-vs-prime-requirements.png)

*The gap that costs subs money: the letter reads as a full audit; the prime will accept documented progress.*

Here is the part that defuses the panic. Most primes are not waiting by the mailbox for a certificate on November 10. They are managing supply-chain risk. What they need to see from a sub is credible, documented evidence that you are on a real path, not a vague promise.

In the language defense subs are actually using in these threads, the acceptable posture is **scoped, scored, scheduled, and moving**:

![Four-step flow of what in progress has to mean for a CMMC subcontractor: scoped, assets touching CUI identified; scored, an honest SPRS number posted; scheduled, self-assessed or a C3PAO date booked; moving, a POA&M with real close dates](/blog/images/3-cmmc-scoped-scored-scheduled-moving.png)

*Scoped, scored, scheduled, and moving. "We're working on it" is not on the list.*

- **Scoped.** You have identified which of your assets actually store, process, or transmit CUI, using the five asset categories in 32 CFR 170.19. A tightly scoped environment is smaller, cheaper, and faster to certify than a sprawling one.
- **Scored.** You have run an honest NIST 800-171 self-assessment and posted a real score to the Supplier Performance Risk System (SPRS). Not an aspirational number. The number that reflects what is actually implemented today.
- **Scheduled.** You have either completed your self-assessment, or, if a C3PAO is required, you have booked an assessment date. With fewer than 100 authorized C3PAOs serving roughly 80,000 contractors who will need Level 2, the booked date is itself a scarce, credible signal.
- **Moving.** You have a Plan of Action and Milestones (POA&M) with real close dates for the gaps that remain.

The artifact that proves all of this is your **System Security Plan (SSP)**. The SSP is the document a prime's compliance officer reads, and the document a C3PAO opens first. It states your scope, describes how each control is implemented, and references your POA&M. A contractor who can hand over a current SSP and a posted SPRS score is demonstrably "moving" in a way the prime can put in their own risk file. A contractor who says "we're working on it" with nothing on paper is not.

If you are building that SSP from a blank page, our [CMMC SSP template](/cmmc-ssp-template/) gives you the structure assessors expect, with the control-by-control implementation language already laid out so you are editing rather than inventing. It is $77, in Word and Excel.

## Conditional certification is the safety valve. Read the fine print.

![CMMC conditional certification facts: a minimum score of 88 of 110, which is 80 percent, to qualify; a 180-day window to close every POA&M item before status expires; and the rule that only one-point controls are POA&M-eligible while three- and five-point controls must be met at assessment](/blog/images/4-cmmc-conditional-certification-poam-rules.png)

*Conditional certification, and the gaps you cannot defer.*

You do not need a perfect score to get over the line. CMMC Level 2 allows a **conditional** status, and understanding it is what lets you make a realistic plan instead of an impossible one.

Level 2 is scored out of 110, one point per control implemented (some controls carry more weight in the DoD methodology, but the count is what matters here). To earn conditional certification you need at least **88 of 110**, an 80 percent threshold, with only eligible gaps left open. From the date that conditional status posts, you have **180 days** to close every open item, after which a closeout assessment confirms remediation. Miss the window and the conditional status expires, taking your eligibility with it.

The trap is assuming any gap can wait. It cannot. Only the lower-weighted, one-point controls are eligible to sit on a POA&M. The heavier three- and five-point controls have to be fully implemented at the time of assessment, with a single narrow exception for CUI encryption that is in use but not yet FIPS-validated. So the planning move is not "we'll POA&M whatever we miss." It is "we have to land the heavy controls first, and we can buy 180 days only on the light ones."

Mapping which gaps are deferrable and which are not, and keeping your SPRS score current as you close them, is exactly the work the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) is built for. It walks the full scoped, scored, scheduled, moving path with the scoping worksheet, SPRS workbook, SSP template, POA&M tracker, and evidence tracker in one place, so the artifacts a prime and an assessor ask for are all consistent with each other.

## The real exposure is the gap between what you said and what is true

There is a quieter reason an honest score matters more than a flattering one, and it is the most important thing in this article for an owner or CFO to understand.

In January 2026, the Department of Justice reported recovering about $52 million across nine cybersecurity-related False Claims Act settlements in fiscal year 2025. A senior DOJ official has been explicit that these cases are not fundamentally about whether a breach occurred. They are about misrepresentation: telling the government you met cybersecurity requirements when you had not. A whistleblower, often an insider, flags the gap, and the false statement itself is the violation.

The template case is MORSECORP, which settled for $4.6 million in 2025 over allegations that included false SPRS scores. The pattern that exposes a contractor is the one this whole article is trying to prevent: a self-reported score that does not match the implemented reality, left uncorrected. The settlements span well beyond primes. In December 2025, a precision machining subcontractor in the defense supply chain settled FCA allegations tied to DFARS 252.204-7012, in a case a former quality control manager set in motion.

This is why "scored" means *honestly* scored. An inflated SPRS number does not just risk a failed assessment later. It is, on its own, the thing the False Claims Act punishes. The safest posture is also the cheapest one: report the real number, document the plan to improve it, and you have converted a legal liability into an ordinary remediation project.

## What to do this quarter

1. **Get the CUI determination in writing.** Ask the prime exactly what CUI flows to you and under what circumstances. If none does, you may be a Level 1, self-assessed requirement, not Level 2.
2. **Scope tightly.** Use the 32 CFR 170.19 categories to draw the smallest defensible boundary around the assets that touch CUI. Scope is the single biggest lever on cost and timeline.
3. **Score honestly in SPRS.** Run the self-assessment against all 110 controls and post the real number. Treat it as a legal statement, because it is one.
4. **Write the SSP.** Document scope and per-control implementation. This is the artifact the prime and the assessor actually read.
5. **Decide self-assessment versus C3PAO, then schedule.** Confirm which your contract requires. If it is a C3PAO, book the date now, before remediation is finished. The queue is the constraint, not your readiness.
6. **Build a POA&M on the eligible gaps.** Land the three- and five-point controls first. Use the 180-day window only for the one-point items that qualify.

If you want the plain-English version to hand to a non-technical owner first, the [CMMC 2.0 Compliance Survival Guide](https://cyberzvi.gumroad.com/l/cmmc-workbook) ($39) is the low-cost entry point that frames the whole program before you invest in the working tools.

## The bottom line

"Be CMMC certified by November 10" is a headline, not a specification. Before it can cost you anything, it has to resolve into three answers: does CUI actually flow to you, does your contract require a self-assessment or a C3PAO, and can you show a prime that you are scoped, scored, scheduled, and moving. Get those answers and the requirement usually shrinks from an unthinkable number into a manageable project. Skip them, and you either overpay for a certification you may not need or lose a contract you could have kept.

---

**Sources:** 32 CFR Part 170 (CMMC Program); 32 CFR 170.19 (asset categories); NIST SP 800-171 Rev. 2; FAR 52.204-21; DFARS 252.204-7012 and 252.204-7021; DoD CMMC scoring and conditional certification guidance; U.S. Department of Justice False Claims Act settlement announcements (2025 to January 2026), including MORSECORP, Inc. ($4.6M, 2025).
