---
layout: post
title: "How Your NIST 800-171 SPRS Score Is Calculated (and What It Legally Commits You To)"
date: 2026-06-20
image: /blog/images/1-sprs-score-legal-statement-hero.png
description: "How the DoD calculates a NIST 800-171 SPRS score, why it ranges from 110 down to minus 203, and what certifying that number legally commits a defense contractor to."
---

*A 104 looks like an A-minus. To the Defense Department, it can read as a misrepresentation. Here is how the SPRS math actually works, and why the number you post is a legal commitment rather than an IT scorecard.*

**Your SPRS score is a self-assessed rating of how completely your organization has implemented the 110 security controls in NIST SP 800-171. You calculate it with the DoD Assessment Methodology by starting at 110 and subtracting weighted points for every control you have not fully implemented, then post it to the Supplier Performance Risk System (SPRS) as required by DFARS clauses 252.204-7019 and 252.204-7020.**

<div style="background:#161618;border-left:4px solid #EE4C48;padding:20px 24px;margin:28px 0;border-radius:4px;">
  <p style="color:#EE4C48;font-weight:700;letter-spacing:0.5px;margin:0 0 12px;">KEY TAKEAWAYS</p>
  <ul style="margin:0;padding-left:20px;line-height:1.6;">
    <li>The score starts at 110 and drops by 1, 3, or 5 points for each unmet control. There is no partial credit.</li>
    <li>The range runs from 110 down to minus 203. A handful of unmet high-weight controls puts you below zero.</li>
    <li>DFARS 252.204-7019 and -7020 require the score in SPRS. A senior official certifies it, and any contracting officer can pull it.</li>
    <li>Under the False Claims Act, the score is a representation to the government. The Department of Justice enforces it, and no breach is required.</li>
    <li>MORSECORP submitted a 104. Its honest score was 57. The gap led to a $4.6 million settlement.</li>
  </ul>
</div>

## The number every defense contractor reports, and few understand

If your company handles Controlled Unclassified Information on a Department of Defense contract, you have an SPRS score whether you have looked at it recently or not. The requirement traces to the DFARS interim rule that took effect in late 2020, which added clauses 252.204-7019 and 252.204-7020. Together they require contractors handling CUI to complete a NIST SP 800-171 self-assessment, calculate a score using the DoD Assessment Methodology, and post that score to the Supplier Performance Risk System.

That score is not buried in an internal spreadsheet. It sits in a government system that contracting officers review during source selection, and since the DFARS clause that governs CMMC took effect on November 10, 2025, officials are actively weighing those scores in award decisions. A current score, meaning one less than three years old, is now a condition of competing for CUI work.

Two details get lost in the day-to-day. First, for most small subcontractors the score is self-assessed. The full third-party C3PAO assessment applies to a specific subset of contracts, but the larger population of the Defense Industrial Base self-reports. Second, the score is certified. A senior company official attests to it. That signature is what converts an arithmetic exercise into a legal statement, a point we return to below.

## How the score is actually calculated

The mechanics are simpler than the regulation around them. You start with a perfect score of 110, one point of headroom for each of the 110 controls in NIST SP 800-171. Then, for every control you have not fully implemented, you subtract that control's assigned weight.

The DoD Assessment Methodology assigns each control a weight of 1, 3, or 5 points based on how much its absence exposes the network. There is no partial credit. A control is either fully implemented or it is not, and a control you are "halfway through" costs you its full weight.

![Infographic showing the SPRS score calculation: start at 110, subtract weighted deductions of 5, 3, or 1 point per unmet control with no partial credit, to arrive at your score; range runs from 110 down to minus 203.](/blog/images/2-how-sprs-score-calculated-110-deductions.png)

*Start at 110, subtract the weighted value of every unmet control, and the result is the number you post to SPRS.*

A concrete example makes the weighting clear. Control 3.13.11 requires FIPS-validated cryptography to protect CUI. If you encrypt but your encryption is not FIPS-validated, you lose 3 points. If you do not encrypt CUI at all, you lose 5. One control, two different gaps, two different penalties, all defined in the methodology rather than left to interpretation.

Here is roughly how the weights distribute across the kinds of controls:

| Weight | What it generally covers | Example areas |
|--------|--------------------------|---------------|
| 5 points | Controls whose absence could lead to significant exploitation or exfiltration | Multi-factor authentication, FIPS-validated encryption, certain access controls |
| 3 points | Controls with a meaningful but more contained security effect | Audit logging, incident response elements, configuration management |
| 1 point | Controls that support overall posture | Documentation and lower-impact administrative requirements |

The exact weight for any given control is fixed in the DoD Assessment Methodology, so two honest assessors scoring the same environment should land in the same place. The judgment is in whether a control is truly met, not in how many points it is worth.

## Why the math is unforgiving, and why negative scores are normal

The lowest possible score is minus 203. That floor surprises people who expect a scale that bottoms out at zero, and it exists because the total weighted value of all 110 controls exceeds 110. Miss enough high-weight controls and the deductions run well past your starting 110 into deep negative territory.

This is why a first honest assessment so often produces a negative number. The 5-point controls are exactly the ones small firms tend to leave for last: enterprise multi-factor authentication across all systems, FIPS-validated encryption everywhere CUI lives, mature audit logging, a tested incident response capability. A company that has done sensible general IT hygiene but none of those heavyweight items can sit far below zero. That is not a sign the assessment is broken. It is the methodology doing its job, pushing you toward the controls that matter most before the ones that matter least.

The absence of partial credit is the part that catches teams off guard. "We have multi-factor authentication rolled out to about 80 percent of users" earns nothing toward that control. The methodology treats it as unmet until it is fully in place. Honest scoring means resisting the urge to round up.

## The part that turns a score into a legal exposure

For most of its life, the SPRS score was treated as an IT artifact, something the security team produced and the rest of the business ignored. That framing is now expensive.

When you post a score under DFARS 252.204-7019, you are not filing paperwork. You are making a representation to the federal government about the state of your security, and a senior official is certifying that it is accurate. The False Claims Act attaches liability to false or misleading representations made to obtain or keep government money. An inflated SPRS score is precisely that kind of representation.

The Department of Justice has spent the last few years making the point with settlements. In the fiscal year ending September 2025, DOJ recovered more than $52 million across nine cybersecurity-related False Claims Act settlements, part of a record $6.8 billion in total FCA recoveries that year. The department has noted that cybersecurity fraud recoveries more than tripled in each of the past two years.

The framing matters as much as the dollars. In January 2026, a senior DOJ official described these cases as not about data breaches but about misrepresentation. You do not need to have been hacked. You need only to have told the government your posture was better than it was. The gap between the score you claimed and the score you could defend is the violation.

## What an inflated score actually costs: MORSECORP

The clearest illustration is the MORSECORP case, the ninth settlement under DOJ's cyber-fraud enforcement push.

![Timeline of the MORSECORP SPRS score: a claimed score of 104 in January 2021, a first honest third-party score of 57 in June 2023, then 82 in October 2023 and 110 in May 2024, ending in a 4.6 million dollar False Claims Act settlement.](/blog/images/3-morsecorp-sprs-score-timeline-fca-settlement.png)

*Claimed 104. The honest number, once a third party scored it, was 57. The gap is what DOJ pursued.*

In January 2021, MORSECORP submitted an SPRS score of 104 to the Defense Department. Against a perfect 110, that reads as nearly full compliance. The problem was that it did not reflect reality. After the company engaged a third-party consultant to actually assess its environment, the first honest score it later posted to SPRS was 57, in June 2023. It climbed to 82 that October and reached 110 in May 2024 as the company finally implemented the controls it had long claimed.

In March 2025, MORSECORP agreed to pay $4.6 million to resolve False Claims Act allegations tied to its Army and Air Force contracts. The case was not triggered by a breach. It was triggered by a whistleblower, specifically the company's own head of security and facility security officer, who filed a qui tam complaint alleging the company had posted inflated scores and had not implemented the controls required by DFARS 252.204-7012, -7019, and -7020. The whistleblower received roughly $851,000 of the settlement.

The lesson for a small subcontractor is not "do not get caught." It is that the score you cannot defend is a standing liability, sitting in a government system, signed by one of your senior people, waiting for anyone with knowledge of the gap to act on it.

## What to do this weekend

You do not need a consultant to take the first useful steps. You need a few hours and honesty.

1. **Pull your current score.** Log in to SPRS through PIEE and confirm what is posted, and confirm it is not older than three years. Plenty of firms discover a stale or forgotten number here.
2. **Re-score yourself control by control, with no partial credit.** Go down the 110 controls and mark each one met or unmet as it stands today, not as it will stand once the project finishes. Subtract the weights and see where you actually land.
3. **Document the basis for each answer.** The record of how you scored each control is your defense if the number is ever questioned. A score with no supporting evidence is a score you cannot stand behind.
4. **Brief the person who signs.** Make sure the senior official certifying the score understands they are making a representation to the government, not approving an IT report.
5. **Attack the 5-point controls first.** They move your number the fastest and they are the ones DOJ cases keep circling back to.

Steps two and three are where most firms stall, because doing them by hand across 110 controls is tedious and easy to fumble. The [NIST 800-171 SPRS Score Workbook for CMMC Level 2](https://payhip.com/b/R5g4Y) ($87) walks the full 110 controls with the correct weights built in, calculates your score as you go, and gives you a documented assessment record you can hand to a contracting officer or a C3PAO. If you want the surrounding pieces as well, the System Security Plan, evidence tracking, and asset scoping, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) bundles the workbook with the rest of the prep set for a firm building toward an assessment.

## The bottom line

The SPRS score is simple arithmetic carrying serious legal weight. Start at 110, subtract honestly, and the number that comes out is a statement your company is making to the federal government. Get the arithmetic right, document how you got there, and make sure the person signing it knows what they are signing. The contractors who run into trouble are almost never the ones with a low score. They are the ones whose score was higher than the truth.

## Sources

- U.S. Department of Justice, Office of Public Affairs, "Defense Contractor MORSECORP Inc. Agrees to Pay $4.6 Million to Settle Cybersecurity Fraud Allegations" (2025).
- U.S. Department of Justice, fiscal year 2025 False Claims Act statistics and accompanying statements (January 2026).
- DoD NIST SP 800-171 Assessment Methodology (scoring weights and the 110-to-minus-203 range).
- DFARS 252.204-7012, 252.204-7019, and 252.204-7020 (Acquisition.gov).
- NIST Special Publication 800-171 (the 110 security requirements).
