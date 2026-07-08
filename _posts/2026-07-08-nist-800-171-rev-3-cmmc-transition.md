---
layout: post
title: "NIST 800-171 Rev 2 or Rev 3 for CMMC? What the July 2026 Interim Rule Changes"
description: "DoD's regulatory agenda shows an interim final rule this month setting the NIST 800-171 Rev 3 transition deadline. Here is what changes for CMMC Level 2, and why your assessment baseline is still Rev 2."
image: /blog/images/1-nist-800-171-rev-3-cmmc-transition-hero.png
---

*DoD is about to put a date on the biggest structural change to CMMC since the program rule was finalized. Here is what the Rev 3 transition actually means for a contractor mid-prep, and why the worst move right now is rebuilding your documentation.*

**CMMC Level 2 is assessed against NIST SP 800-171 Revision 2, the version with 110 security requirements across 14 control families, as specified in 32 CFR Part 170. NIST published Revision 3 in May 2024, but Rev 3 has no effective date inside the CMMC program yet. According to the federal government's Spring 2026 Unified Agenda, as reported by Federal News Network in July 2026, the Department of Defense plans to adopt an interim final rule this month that sets the deadline for shifting CMMC to Rev 3.**

<div class="key-takeaways" style="background:#0D0D0F;border-left:4px solid #EE4C48;padding:1.2em 1.5em;margin:1.5em 0;color:#fff;">
<strong style="color:#EE4C48;">Key Takeaways</strong>
<ul style="margin-top:0.6em;">
<li>DoD's regulatory agenda shows an interim final rule landing in July 2026 that details the deadline for moving CMMC from NIST SP 800-171 Rev 2 to Rev 3.</li>
<li>Until that rule takes effect, every CMMC Level 2 assessment, SPRS submission, and C3PAO certification runs against Rev 2. That is written into 32 CFR Part 170.</li>
<li>Rev 3 restructures the framework: 97 requirements instead of 110, 17 control families instead of 14, and organization-defined parameters whose values DoD already fixed in a 2025 memo.</li>
<li>The right posture is two tracks: keep your SSP, SPRS score, and evidence on Rev 2, and track Rev 3 deltas in a separate planning file.</li>
</ul>
</div>

## The news: a transition deadline is about to exist

For two years, the answer to "when does CMMC move to Rev 3?" has been a shrug. NIST published SP 800-171 Revision 3 on May 14, 2024, and from NIST's perspective it supersedes Revision 2. But the CMMC program rule, 32 CFR Part 170, pins Level 2 to Rev 2, and DoD's class deviation 2023-O0006 keeps DFARS 252.204-7012 assessments pointed at Rev 2 as well. Rev 3 has been the standard on paper at NIST and irrelevant in practice at DoD.

That gap is now scheduled to close. The Spring 2026 Unified Agenda, the government's semiannual public preview of upcoming rulemaking, shows DoD adopting an interim final rule for the CMMC program in July 2026 that details the transition deadline to Rev 3. Federal News Network, which reported the agenda item, quotes the regulatory preview directly: the significant changes between Rev 2 and Rev 3 include "added specificity in the security requirements and introduction of organization-defined parameters (ODP) in select security requirements."

The same agenda shows a second move coming in August 2026: a Notice of Proposed Rulemaking updating DFARS 252.204-7012, the clause that requires contractors to safeguard covered defense information in line with NIST standards. CMMC is the verification layer built on top of that clause, so the two rulemakings travel together.

An interim final rule is worth pausing on. Unlike a proposed rule, an interim final rule takes effect when published, with comments collected afterward. When this one lands, the Rev 3 transition stops being industry speculation and becomes a date on your calendar.

![Rev 2 vs Rev 3 comparison]({{ site.baseurl }}/blog/images/2-cmmc-rev-2-vs-rev-3-comparison.png)

## What actually changes between Rev 2 and Rev 3

Rev 3 is not a light edit. Three structural changes matter most for a contractor planning ahead.

**The count drops, the work does not.** Rev 3 contains 97 security requirements against Rev 2's 110. That sounds like relief until you look at how the reduction happened: many withdrawn Rev 2 requirements were consolidated into other requirements rather than eliminated. The obligations largely survive under new numbering.

**Three new control families appear.** Rev 3 adds Planning (PL), System and Services Acquisition (SA), and Supply Chain Risk Management (SR), bringing the family count from 14 to 17 and aligning the structure with NIST SP 800-53 Rev 5. Supply chain risk management in particular is new territory for many small contractors, and it is the kind of family that requires vendor documentation you cannot produce in a week.

**Organization-defined parameters change how requirements read.** Rev 2 tells you to "limit unsuccessful logon attempts" and leaves the numbers to you. Rev 3 rewrites requirements like that with fill-in-the-blank parameters: how many attempts, over what window, with what lockout action. NIST designed ODPs for organizational flexibility. DoD removed the flexibility: in April 2025, DoD published a memo assigning specific values to the Rev 3 ODPs for defense contractors. When the transition happens, an assessor will not ask what values you chose. They will check whether your environment enforces the values DoD chose.

## Why your assessment baseline is still Rev 2

Here is the part that gets lost every time Rev 3 makes news: nothing about this month's expected rule changes what a C3PAO will assess you against tomorrow, or what SPRS will accept.

Today, per 32 CFR Part 170:

- CMMC Level 2 self-assessments are scored against Rev 2's 110 requirements.
- C3PAO certification assessments use NIST SP 800-171A, the assessment procedures companion to Rev 2, with its examine, interview, and test methods.
- SPRS scoring uses the DoD Assessment Methodology built on Rev 2. SPRS does not accept Rev 3-based scores.

That creates a real trap for well-intentioned teams. Rev 3 sounds like progress, leadership wants to be ahead of the curve, and someone proposes rewriting the SSP around the new structure. Do that, and your documentation stops matching the framework your assessor is required to use. Controls that are actually implemented can read as unmet because the SSP narrates them against the wrong baseline. With Phase 2 mandatory C3PAO assessments beginning November 10, 2026, a self-inflicted documentation mismatch is an expensive way to be forward-looking.

The transition itself will also not be a light switch. DoD signaled in its CMMC alignment guidance that contractors will get transition runway, and the interim final rule is expected to define exactly that: the deadline and the mechanics. Until the rule is published and its dates are public, any specific transition timeline you read is a guess.

![Rev 3 rulemaking timeline]({{ site.baseurl }}/blog/images/3-cmmc-rev-3-rulemaking-timeline.png)

## The two-track posture: prep Rev 2, track Rev 3

The practical answer is to run two tracks with a hard wall between them.

**Track one is your live compliance program, and it stays on Rev 2.** Your System Security Plan, your SPRS score, your POA&M, your evidence folders, and your assessment scheduling all reference Rev 2 and 800-171A. This is the track that determines whether you keep bidding after November 10, 2026.

**Track two is a Rev 3 planning file, kept separate.** This is where forward-looking work goes without contaminating the live program:

1. **Build a crosswalk.** Map each Rev 2 requirement to its Rev 3 equivalent. NIST publishes the analysis of changes with Rev 3, so this is a documentation exercise, not detective work. The crosswalk is what makes the eventual transition a re-mapping project instead of a rebuild.
2. **Read the DoD ODP values now.** Where a Rev 3 ODP value is compatible with your current Rev 2 implementation, adopting it early costs nothing and removes a future change. Setting your lockout threshold to the DoD-defined value today does not conflict with Rev 2; Rev 2 simply left the number to you.
3. **Scope the three new families.** Planning, System and Services Acquisition, and Supply Chain Risk Management are where genuinely new work lives. You do not need to implement them yet. You need a rough inventory of what they would demand from your environment and your vendors, so the eventual deadline is a project plan, not a surprise.
4. **Watch for two documents.** The interim final rule itself, expected this month, and any rescission of class deviation 2023-O0006. Those are the official signals. Everything else is commentary.

## What this looks like for a 15-person machine shop

Take a small precision parts supplier with CUI on a handful of Army subcontracts, currently at maybe 70 of 110 requirements implemented and aiming for a C3PAO slot in early 2027. The Rev 3 news changes almost nothing about their next six months. Their gap remediation, their SSP, and their SPRS submission all continue on Rev 2, because that is what the assessor will use.

What changes is one afternoon of planning work: download Rev 3, skim the analysis of changes, note that SR (supply chain) will eventually require supplier risk documentation they do not currently keep, and set the ODP-driven configuration values to DoD's numbers while configuring systems they were fixing anyway. Total cost: hours. Value: the transition, whenever the new rule says it happens, starts from a map instead of from zero.

## The bottom line

The July 2026 interim final rule will answer the question the defense industrial base has been asking since May 2024: when does Rev 3 become real for CMMC? Until it is published, the only baseline that can pass or fail you is Rev 2. Keep the live program there, put Rev 3 work in a separate planning track, and treat the rule's publication as the trigger to turn that planning file into a scheduled project.

If you are mid-prep against the November 10 window, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) keeps the whole package on the Rev 2 baseline your assessor will actually use: scoping, SPRS scoring, SSP, evidence tracking, and POA&M in one set. If the documentation piece is the gap, the [CMMC Level 2 System Security Plan (SSP) Template](https://payhip.com/b/gB6oD) ($77) is structured around Rev 2 and 800-171A the way an assessor reads it.

## Sources

- Federal News Network, "CIRCIA, other big cyber rules expected to get finalized this fall," July 2026 (reporting the Spring 2026 Unified Agenda)
- Unified Agenda of Regulatory and Deregulatory Actions, reginfo.gov
- 32 CFR Part 170, CMMC Program (eCFR)
- NIST SP 800-171 Revision 3, May 2024 (csrc.nist.gov)
- NIST SP 800-171 Revision 2 and NIST SP 800-171A (csrc.nist.gov)
- DoD CIO, "CMMC Alignment to NIST Standards" (dodcio.defense.gov)
- DoD Class Deviation 2023-O0006 and DoD memo on NIST SP 800-171 Rev 3 organization-defined parameters, April 2025
