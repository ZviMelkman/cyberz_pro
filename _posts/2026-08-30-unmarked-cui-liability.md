---
layout: post
title: "Unmarked CUI: Are You Still on the Hook If DoD Never Labeled It?"
date: 2026-08-30
description: "DoD's own Inspector General says DoD components routinely fail to mark CUI. Industry told the CMMC Reform Task Force the same thing. Here is what DFARS 252.204-7012 actually says about unmarked information, why the answer differs for data DoD gives you versus data you create, and how to sort it before it lands in your CMMC scope."
category: CMMC
tags: [CMMC, CUI, unmarked CUI, DFARS 252.204-7012, DoDI 5200.48, 32 CFR 2002, CMMC scoping, CMMC Reform Task Force, CUI marking, defense contractors]
image: /blog/images/1-unmarked-cui-liability-dfars-7012-hero.png
author: CyberZ
---

*The most common CMMC question on r/CMMC this summer was not about controls. It was a subcontractor holding a task order with no CUI markings on anything, asking whether that means they are off the hook. Half the replies said yes. The clause says something more specific than that.*

**Unmarked CUI is information that meets the definition of Controlled Unclassified Information under 32 CFR Part 2002 but arrived, or was created, without the CUI banner and designation indicator block that DoDI 5200.48 requires. Whether you are obligated to protect it depends on which of the two definitions of covered defense information in DFARS 252.204-7012 it falls under. Information DoD provides must be marked or identified in the contract to count. Information you collect, develop, or store in performance of the contract has no marking condition at all, which means a missing label on your own engineering drawings does not take them out of scope.**

<div style="border-left:4px solid #EE4C48;background:#18181c;padding:20px 24px;margin:28px 0;border-radius:4px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;line-height:1.65;color:#e6e6e6;">
<li>DoD's Inspector General found in January 2026 (DODIG-2026-047) that DoD components frequently omit the required CUI designation indicator block and default to overly restrictive dissemination controls. A 2023 audit (DODIG-2023-078) found the same marking failures three years earlier.</li>
<li>Industry comments to the CMMC Reform Task Force, reported August 19, 2026, named CUI identification and marking as the leading cost driver of the program. The SBA Office of Advocacy called it the most frequently cited concern of small contractors.</li>
<li>DFARS 252.204-7012 defines covered defense information in two prongs. Prong 1 (information DoD provides) requires the information be marked or identified in the contract. Prong 2 (information you collect, develop, receive, transmit, use, or store in performance) has no marking requirement.</li>
<li>Under 32 CFR Part 2002 and DoDI 5200.48, only the designating agency decides what is CUI. A contractor cannot promote legacy FOUO material to CUI on its own, and NARA directs status questions back to the contracting activity.</li>
<li>Sorting information into four buckets (marked, government-furnished but unmarked, contractor-created, legacy-marked only) is the step that decides whether your 32 CFR 170.19 scope is defensible or inflated.</li>
</ul>
</div>

## Why DoD's own auditors keep flagging the marking problem

On January 29, 2026, the DoD Office of Inspector General issued Management Advisory DODIG-2026-047 on DoD policy and training for CUI dissemination controls. The advisory grew out of an evaluation of non-DoD messaging systems, but what the evaluators found along the way was broader: DoD components frequently failed to mark CUI documents with the required designation indicator block, and when they did mark them, they often defaulted to the "Federal Employees and Contractors Only" limited dissemination control rather than applying no control at all. The IG issued five recommendations. As of April, DoD said two were closed and three remained open.

This was not a new finding. DODIG-2023-078, issued June 1, 2023, audited DoD's implementation of the CUI program and concluded that components did not ensure CUI documents and emails carried the required markings, had no mechanisms in place to check, and did not consistently track whether DoD and contractor personnel completed required CUI training.

Then came the CMMC Reform Task Force. When the Department of Defense suspended CMMC Phase 2 on July 13, 2026 and opened a request for information on reducing compliance burden, the responses converged on one issue. Federal News Network's August 19 roundup of the comment letters reported that the SBA Office of Advocacy called CUI uncertainty the most frequently cited concern of small businesses, that NDIA documented multiple instances of inconsistent and inaccurate marking, and that the Professional Services Council asked DoD to confirm contractors are not obligated to protect material that was never properly designated by an authorized designating authority. The Alliance for Digital Innovation described primes issuing blanket Level 2 flow-downs to machine shops that never touch CUI, because the primes lack confidence in their own scoping.

The Task Force is expected to take roughly another month to complete its work before reporting to the DoD CIO. Whatever it recommends, the problem it is being asked to fix is the one you are living with now: information arrives without labels, and you have to decide what to do with it.

## What DFARS 252.204-7012 actually says about marking

The clause that puts NIST SP 800-171 on your network is DFARS 252.204-7012. It applies to "covered defense information," and the clause defines that term in two parts. Both start the same way: unclassified controlled technical information or other information described in the CUI Registry that requires safeguarding or dissemination controls under law, regulation, or government-wide policy. Then the definition splits.

![Two-column graphic comparing the two prongs of the DFARS 252.204-7012 definition of covered defense information. Prong 1 is information DoD provides, which must be marked or identified in the contract. Prong 2 is information the contractor collects, develops, receives, transmits, uses, or stores in performance of the contract, with no marking condition.](/blog/images/2-dfars-7012-covered-defense-information-two-prongs.png)

Prong 1 covers information that is "marked or otherwise identified in the contract, task order, or delivery order and provided to the contractor by or on behalf of DoD in support of the performance of the contract." Marking is one way to satisfy it. Identification in the contract is the other. If neither happened, DoD did not designate that information as covered defense information under this prong.

Prong 2 covers information "collected, developed, received, transmitted, used, or stored by or on behalf of the contractor in support of the performance of the contract." Read it again and notice what is absent. There is no marking condition. There is no requirement that the contract identify it. If your firm creates engineering drawings, process sheets, test reports, or source code in performance of a DoD contract, and that material fits a CUI Registry category such as Controlled Technical Information, it is covered defense information from the moment you create it.

This is why the Reddit answer "if it's unmarked you're not on the hook" is half right. It holds for prong 1, and it is the basis for the PSC recommendation that contractors should not have to protect what was never designated. It does not hold for prong 2. Michael Lowell of Reed Smith made the point in the Federal News Network piece: a contractor may receive little or no marked CUI from DoD and still create CUI during performance, and if the contract does not say what it expects to be CUI, the contractor is left making difficult judgments about its own work product.

## Who is allowed to decide what is CUI

The next question is whether you can make that judgment yourself, and the answer is narrower than most contractors assume.

The government-wide CUI program at 32 CFR Part 2002 puts designation authority with the designating agency. DoDI 5200.48, which implements the program inside DoD, states in paragraph 3.6.a that the authorized holder of a document is responsible for determining at the time of creation whether the information falls into a CUI category and, if so, for applying CUI markings and dissemination instructions. It also directs that CUI requirements be articulated in the contract. The DoD Procurement Toolbox FAQ on DFARS 252.204-7012 is more concrete about where: marking requirements for contractor-generated covered defense information will typically be found in Block 9 of the Contract Data Requirements List, in Section J of the contract.

Two consequences follow. First, if your contract or CDRL tells you which deliverables are CUI and how to mark them, you are an authorized holder applying instructions, and prong 2 is fully in play. Second, if it does not, you are not authorized to invent a CUI designation. The National Archives' CUI FAQ says questions about the status of information, marked or unmarked, should be directed back to the government contracting activity. And both 32 CFR Part 2002 and DoDI 5200.48 are explicit that legacy markings such as For Official Use Only or Sensitive But Unclassified do not automatically make something CUI. An authorized official at the owning agency has to make that determination. A contractor cannot make it for them.

Kate Growley of Crowell & Moring summarized the practical effect for Federal News Network: CMMC follows the data. If CUI is over-scoped or under-scoped, so is CMMC.

## Why this is a scoping problem before it is a controls problem

Every CMMC Level 2 scope is built on 32 CFR 170.19. CUI Assets, the systems that process, store, or transmit CUI, are assessed against all 110 requirements. Everything else is assessed lighter or not at all. We walked through the five asset categories in [Why Your CMMC Timeline Is a Scoping Decision, Not a Controls Problem]({% post_url 2026-07-19-cmmc-scoping-decision-not-controls %}). The point here is what unmarked information does to that boundary.

The SBA Office of Advocacy described the failure mode in its comment letter: when a contractor cannot confidently determine what information is CUI, they will generally err on the side of including all of it in the compliance boundary. For a 12-person machine shop, that means every workstation, the shared drive, the email tenant, and the CAD license server all become CUI Assets, and the firm prices a full enclave for information that may never have been designated. Advocacy said DoD has in some cases treated publicly available information as CUI.

The opposite failure is quieter and more dangerous. A contractor assumes that because nothing arrived with a banner, nothing in the environment is CUI. Meanwhile its engineers are generating drawings and test data under a statement of work that, on close reading, describes Controlled Technical Information. Prong 2 covers that material. The SPRS score and the annual affirmation under 32 CFR 170.22 both assert a boundary that does not match the data. We covered what that assertion now carries in [CMMC Affirmation and the False Claims Act]({% post_url 2026-08-23-cmmc-affirmation-false-claims-act %}); the short version is that DOJ's cyber fraud cases are built on the gap between what was stated and what was true, not on breaches.

There is also a reporting angle. The 72-hour cyber incident reporting duty in DFARS 252.204-7012(c) is triggered by a compromise affecting covered defense information. If you do not know which files are covered defense information, you cannot know whether an incident on a given system is reportable. Separately, the June 2026 revision of the proposed FAR CUI rule keeps an obligation to notify the contracting officer within 72 hours of discovering unmarked or mismarked CUI, while clarifying that the bad marking alone is not a CUI incident. We covered that revision in [FAR CUI Rule Requirements: What the June 2026 Revision Actually Changed]({% post_url 2026-07-28-far-cui-rule-requirements %}). It is a proposed rule, not a final one, but it tells you where the government's expectation is heading: find it, report it, do not treat it as a breach.

## The four-bucket sort

Before anything goes into scope, put every category of information you hold under a DoD contract into one of four buckets.

![Four-row decision graphic for sorting unmarked CUI: marked CUI, unmarked information from DoD or a prime where the contract names CUI, information the contractor created in performance, and legacy FOUO or SBU material with no CUI designation, each with the action to take.](/blog/images/3-unmarked-cui-decision-sort-what-to-do.png)

**Marked CUI.** Banner present, designation indicator block present. Protect it as CUI and scope the systems that touch it. No judgment call required.

**Unmarked, but from DoD or your prime, and the contract says CUI is involved.** The contract, DD Form 254, SOW, or CDRL names CUI categories or describes deliverables that plainly fit one, but the specific documents arrived bare. This is the case the IG advisory describes. Treat it as CUI in the interim and write to the contracting officer, through your prime if you are a sub, asking which category and marking apply. Keep the written exchange. It is evidence of good faith, and it is the paper trail the PSC recommendation would protect.

**You created it in performance.** Drawings, reports, code, test data, process documentation generated to deliver the contract. This is prong 2. Check the SOW and CDRL Block 9 for marking instructions. If the deliverable fits a Registry category such as Controlled Technical Information, it is covered defense information whether or not anyone has marked it yet, and you are the authorized holder responsible for marking it under DoDI 5200.48. If the contract is silent, ask, in writing, before you either exclude it or build an enclave around it.

**Legacy FOUO or SBU only.** Old documents with pre-2020 markings and no CUI designation. Under 32 CFR Part 2002 these are not automatically CUI. The owning agency has to re-examine and designate them. Do not scope them in on your own authority, and do not scope them out without asking. A one-line email to the contracting activity settles it.

The sort takes an afternoon for most small firms. What it produces is a defensible answer to the first question any assessor, DIBCAC reviewer, or prime supplier-assurance team will ask: how did you decide what was in scope?

## What to do this week

Pull every active DoD contract and subcontract and read three things: the clause list for 252.204-7012, the SOW for language describing technical data or deliverables, and Section J for a CDRL with a Block 9 marking instruction. That tells you what DoD has actually identified.

Inventory where information from each bucket lives. Not where policy says it lives. Email, file shares, engineering workstations, the cloud tool someone signed up for, the prime's portal. This is the asset list your scope is built from.

For every item in bucket two or bucket four, send one written question to the contracting officer or your prime's compliance contact. Save the reply, or the absence of one, with the date.

Reconcile the result against your SSP and your SPRS score. If the boundary moved, the score and the affirmation need to move with it.

If you are a prime or a higher-tier sub, do the same exercise before you flow Level 2 down. Blanket flow-downs to shops that never touch CUI are exactly what ADI complained about to the Task Force, and they cost your suppliers real money.

The bucket sort and the asset inventory are what the [CMMC Level 2 Asset Scoping Worksheet for NIST 800-171](https://payhip.com/b/2nzjO) ($47) is built to produce: a categorized asset list under 32 CFR 170.19 with the scope summary an assessor expects to see. If the exercise moves your boundary, the [CMMC Level 2 System Security Plan (SSP) Template](https://payhip.com/b/gB6oD) ($77) is structured so the boundary description, the CUI flow, and the control implementation statements are updated together rather than drifting apart.

## The bottom line

DoD marks CUI badly, its own Inspector General has said so twice, and the CMMC Reform Task Force has been told it is the program's leading cost driver. None of that changes the clause you signed. DFARS 252.204-7012 attaches the marking test to information DoD gives you and attaches no marking test to information you create in performance. You cannot designate CUI yourself, but you also cannot assume a missing label means a missing obligation. Sort what you hold into four buckets, ask the contracting officer in writing about the two that are ambiguous, and build your scope on the answer.

### Sources

- DFARS 252.204-7012, Safeguarding Covered Defense Information and Cyber Incident Reporting, 48 CFR 252.204-7012, definition of "covered defense information" (eCFR)
- DoD Office of Inspector General, Management Advisory DODIG-2026-047, DoD Policy and Training on Dissemination Controls for Controlled Unclassified Information, January 29, 2026
- DoD Office of Inspector General, DODIG-2023-078, Audit of the DoD's Implementation and Oversight of the Controlled Unclassified Information Program, June 1, 2023
- DoD Instruction 5200.48, Controlled Unclassified Information (CUI), March 6, 2020
- 32 CFR Part 2002, Controlled Unclassified Information (eCFR)
- 32 CFR 170.19, CMMC Scoping (eCFR)
- National Archives and Records Administration, CUI Frequently Asked Questions
- DoD Procurement Toolbox, Cybersecurity FAQs on DFARS 252.204-7012, Q24
- SBA Office of Advocacy, comment letter to the CMMC Reform Task Force, August 14, 2026
- Federal News Network, "CMMC review: DoD's inconsistent CUI marking continues to plague program," August 19, 2026
- Federal News Network, "DoD still failing to properly mark CUI data years after initial audit," April 8, 2026
- Federal Register, Federal Acquisition Regulation: Controlled Unclassified Information, revised proposed rule, 91 FR 37550, June 23, 2026
