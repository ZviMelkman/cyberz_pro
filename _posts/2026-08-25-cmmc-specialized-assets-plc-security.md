---
layout: post
title: "CMMC Specialized Assets Just Got Tested: What CISA's Siemens PLC Advisory Means for a Small Defense Manufacturer"
date: 2026-08-25
description: "On August 19, 2026, NSA, CISA, FBI, DOE and EPA confirmed threat actors are using AI-generated scripts against internet-exposed Siemens S7 PLCs. Under 32 CFR 170.19 those PLCs are CMMC Specialized Assets, managed under risk-based policy rather than the 110 controls. The advisory is the first federal statement of what that policy has to cover."
category: CMMC
tags: [CMMC, specialized assets, operational technology, OT security, PLC, Siemens S7, CISA advisory, AI-generated exploits, 32 CFR 170.19, NIST 800-171, defense manufacturing, CMMC scoping]
image: /blog/images/1-cmmc-specialized-assets-plc-security-hero.png
author: CyberZ
---

*The CMMC scoping rule gives your shop-floor controllers a light touch. List them, describe them in the SSP, show they are managed under a risk-based policy, and the assessor moves on. Nobody defined what that policy had to contain. On August 19, five federal agencies did, in a joint advisory about AI-generated exploit scripts aimed at the most common PLC family in American manufacturing.*

**Under CMMC Level 2, Specialized Assets are assets that can process, store or transmit CUI but cannot be fully secured, including operational technology (OT), Internet of Things and Industrial IoT devices, government-furnished equipment, restricted information systems and test equipment. Under 32 CFR 170.19(c)(1) Table 3 they are in scope: the contractor documents them in the asset inventory, describes their treatment in the System Security Plan, shows they are managed using its risk-based security policies, procedures and practices, and includes them in the network diagram. The assessor reviews the SSP and does not assess them against the other CMMC security requirements. A PLC on a CNC machine running part programs derived from controlled technical data is the textbook case.**

<div style="border-left:4px solid #EE4C48;background:#18181c;padding:20px 24px;margin:28px 0;border-radius:4px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;line-height:1.65;color:#e6e6e6;">
<li>On August 19, 2026, NSA, CISA, FBI, DOE and EPA published joint advisory AA26-231A: threat actors are using AI-generated exploitation scripts, disguised as OT monitoring tools, against internet-exposed Siemens S7-200, S7-300, S7-400, S7-1200 and S7-1500 PLCs. Critical Manufacturing is the first named target sector.</li>
<li>Under 32 CFR 170.19, a PLC is a CMMC Specialized Asset. It is in scope, it goes in the inventory, the SSP and the network diagram, but it is not assessed against the 110 NIST SP 800-171 controls. The only substantive requirement is that it be managed under the contractor's risk-based security policies.</li>
<li>The advisory's mitigations, inventory, no internet exposure, TCP port 102 blocked at the perimeter, passwords and protection levels set, firmware current, S7comm traffic baselined, are now the practical content of that risk-based policy.</li>
<li>With Phase 2 suspended since July 13, no assessor reviews the Specialized Assets section of your SSP. The annual affirmation under 32 CFR 170.22 still covers it, and DFARS 252.204-7012 still requires adequate security on any system holding CUI.</li>
<li>First job this week: confirm that no PLC in your building answers on TCP port 102 from the internet, then write that position into the SSP where an assessor, or a DOJ attorney, can read it.</li>
</ul>
</div>

## What five agencies said on August 19

Joint Cybersecurity Advisory AA26-231A, "Defending Against an Active Threat to Siemens S7 Series PLCs," is co-signed by the National Security Agency, the Cybersecurity and Infrastructure Security Agency, the FBI, the Department of Energy and the Environmental Protection Agency. Five signatures on one ICS advisory is unusual. The content explains why.

The agencies describe threat actors conducting reconnaissance and capability development against U.S.-based Siemens PLC installations using AI-generated exploitation scripts disguised as legitimate monitoring tools. The attack chain is short. The actors use internet scanning services such as Censys and ZoomEye to find PLCs with TCP port 102, the S7comm port, reachable from the internet, running outdated firmware or otherwise poorly protected. They then use AI to write Python scripts built on the open-source snap7.dll and python-snap7 libraries, the same libraries integrators use legitimately, which give read and write access to PLC memory, configuration data and ladder logic. The scripts are dressed up as OT monitoring or telemetry software so that an operator glancing at a process list sees nothing wrong.

![Four-step attack chain from CISA advisory AA26-231A: internet scanning finds PLCs with TCP port 102 exposed, AI generates Python scripts on snap7 libraries, the script is disguised as a monitoring tool, and the actor reads and writes PLC memory and ladder logic over S7comm](/blog/images/3-cisa-siemens-plc-advisory-attack-chain.png)

Three details matter for a defense manufacturer.

The models. The advisory covers every S7 generation still in service: S7-200, S7-300, S7-400, S7-1200 and S7-1500, including the F-series safety controllers. If you bought a machine tool, a press line or a packaging cell in the last twenty years, there is a reasonable chance one of these is inside the cabinet.

The sectors. Critical Manufacturing is listed first among the targeted sectors, ahead of Energy, Water and Wastewater, Chemical, Food and Agriculture, and Commercial Facilities. A machine shop with a DoD subcontract sits squarely inside that first category.

The AI framing. The agencies wrote that using AI to generate exploitation scripts dramatically reduces the technical expertise and time needed to develop working ICS exploitation tools, and that AI lets adversaries adapt quickly to defensive measures. Their summary line: this is not a theoretical risk, it is an active threat. The advisory does not attribute the activity to a named group. It follows an April 2026 warning about Iranian-affiliated actors exploiting Rockwell Automation PLCs, updated in July to add Schneider Electric and Siemens devices, so the pattern of internet-exposed controllers being found and worked is at least four months old.

We covered the broader run of AI agent incidents this summer in [AI-Powered Attacks on Small Businesses]({% post_url 2026-08-24-ai-powered-attacks-small-business %}). This advisory is different in kind. It is not a lab escape or a red-team result. It is five agencies describing adversaries using AI as a force multiplier against physical equipment in American factories.

## Where a PLC sits in CMMC scoping

Now the compliance side. 32 CFR 170.19 sorts every asset in a Level 2 environment into five categories: CUI Assets, Security Protection Assets, Contractor Risk Managed Assets, Specialized Assets and Out-of-Scope Assets. We walked the scoping logic in [Why Your CMMC Timeline Is a Scoping Decision]({% post_url 2026-07-19-cmmc-scoping-decision-not-controls %}). The category that matters here is the fourth one.

Table 3 in 170.19(c)(1) defines Specialized Assets as assets that can process, store or transmit CUI but are unable to be fully secured, and names the types: IoT and IIoT devices, Operational Technology, Government Furnished Equipment, Restricted Information Systems and Test Equipment. The DoD Level 2 Scoping Guide (version 2.13) defines OT as hardware and software that uses direct monitoring and control of industrial equipment. A PLC is the definition.

The contractor's obligations for a Specialized Asset are four sentences long. Document it in the asset inventory. Document its treatment in the SSP. Show it is managed using the contractor's risk-based security policies, procedures and practices. Document it in the network diagram of the CMMC Assessment Scope. The assessor's obligation is shorter still: review the SSP, do not assess against the other CMMC security requirements.

That is a deliberate and sensible design. Nobody expects a 2009 S7-300 to run an endpoint agent or take a password rotation policy. The Scoping Guide even allows for an Enduring Exception where the asset can never meet a given requirement. The rule takes the 110 controls off the PLC and replaces them with one obligation: manage it under a written, risk-based policy.

The problem is that until last week, "risk-based" had no floor. A contractor could write "PLCs are isolated on the production network and managed by our integrator" into the SSP, and that sentence satisfied Table 3 whether or not anyone had ever checked what "isolated" meant.

## What "risk-based" has to say now

AA26-231A does not mention CMMC. It does not need to. It describes, from the federal government's side, the specific exposure that an S7 controller has and the specific things an owner is expected to do about it. When an SSP claims a PLC is managed under risk-based policy, the reasonable reading of "risk-based" after August 19 is a policy that addresses the risk five agencies just documented.

![Two-column map: each of the four 32 CFR 170.19 obligations for a Specialized Asset on the left, and what advisory AA26-231A now implies for that line on the right, covering inventory, SSP exposure statement, passwords and firmware, and the network diagram](/blog/images/4-cmmc-specialized-assets-risk-based-policy-map.png)

Line up the four Table 3 obligations against the advisory's mitigations and the mapping is direct.

Asset inventory. The advisory's first mitigation is to inventory every Siemens S7 PLC. For CMMC purposes the inventory entry needs the model, the firmware version, the IP address and every path that can reach it, because the attack begins with a path to port 102.

SSP treatment. The advisory's central mitigation is that PLCs must not be reachable from the internet, with TCP port 102 blocked at the perimeter firewall. Your SSP should state that position in a sentence a stranger can verify: no controller responds on port 102 from outside the production segment, and here is how we know.

Risk-based management. The advisory calls for password protection on all controllers, protection levels configured to limit what an unauthenticated or low-privilege session can read or write, firmware updates with internet-facing units first, and ICS-aware monitoring that baselines normal S7comm behavior. It also gives hunt criteria: sequential scanning on port 102, snap7 library use outside approved engineering workstations, S7comm activity during off-hours, configuration changes with no matching work order, and connections from unexpected countries. A risk-based policy for a Specialized Asset should now name which of these it does, which it does not, and why.

Network diagram. The advisory assumes an engineering workstation, a production segment and a perimeter. If your diagram does not show which host is allowed to talk S7comm to the controllers, and by which route the integrator gets in, it does not show the thing the adversary is looking for.

None of this makes the PLC a CUI Asset subject to the full 110 controls. The category does not change. What changes is that the one sentence the category does require now has a public benchmark, written by NSA and CISA, that anyone reviewing your SSP can hold it against.

## Why this lands harder after the pause

On July 13, 2026, DoD suspended CMMC Phase 2 and the third-party assessments that would have started in November. The mechanics are in [Is CMMC Still Required?]({% post_url 2026-07-19-is-cmmc-still-required %}). Two consequences follow for the Specialized Assets section of your SSP.

First, nobody outside the company reviews it. Table 3 says the assessor reviews the SSP for Specialized Assets. There is no assessor. The section exists, it is part of the document you affirm against, and the only person who will ever read it critically is one you did not invite.

Second, the affirmation still covers it. As we laid out in [CMMC Affirmation and the False Claims Act]({% post_url 2026-08-23-cmmc-affirmation-false-claims-act %}), 32 CFR 170.22 requires a named Affirming Official to attest annually that the organization has implemented and will maintain all applicable CMMC security requirements. The Specialized Assets treatment in the SSP is one of those requirements. If the SSP says controllers are isolated and a Censys query returns your public IP with port 102 open, the affirmation and the observable facts disagree. DOJ's cyber fraud cases are built on that kind of disagreement, and its Deputy Assistant Attorney General has said publicly that they are premised on misrepresentations, not breaches.

Separately, DFARS 252.204-7012 still requires adequate security on any covered contractor information system. A controller holding part programs derived from ITAR drawings is handling CUI. The 7012 obligation never depended on CMMC phasing at all.

## What this looks like in a 30-person shop

Picture a precision machining subcontractor with twelve CNC machines, a press line and a small assembly cell, doing about $4 million a year in defense work. The machine tools were bought over fifteen years from three builders. Two run S7-1200 controllers, the press line runs an S7-300 in the main cabinet, and the assembly cell was integrated by a regional firm that put an S7-1500 in with a cellular modem for remote support.

The IT side is reasonably tidy. Office network, managed by an MSP, SPRS score posted, SSP written eighteen months ago for the Level 2 self-assessment. The Specialized Assets section is a paragraph. It lists "production machine controllers" as OT, says they are on a separate VLAN and are supported by the equipment vendors, and moves on.

Here is what the advisory turns that paragraph into. Nobody in the building knows which firmware the S7-300 is running. The cellular modem on the assembly cell has a public IP and was set up by the integrator, who has never been asked how it is secured. The "separate VLAN" exists but the MSP allowed the CAM workstation to reach it so that programs could be pushed, which means the workstation that holds the drawings and the controllers that run them are one hop apart. And the shop's public IP range has never been searched for port 102, because nobody knew that was a thing to search for.

None of that is negligent by 2025 standards. All of it is the exact situation AA26-231A describes, and all of it sits behind a sentence in the SSP that the Affirming Official signed against.

## What to do this week

![Six-item checklist for a small defense manufacturer running Siemens PLCs: inventory every PLC, check external exposure on port 102, block port 102 at the perimeter, set passwords and protection levels then update firmware, ask the integrator how they connect, and write the result into the SSP and network diagram](/blog/images/5-plc-security-checklist-small-defense-manufacturer.png)

**Inventory every controller.** Walk the floor with a clipboard. For each cabinet: PLC model, firmware version, IP address, which network it sits on, who supports it and how they connect. This is the advisory's first mitigation and the first Table 3 obligation in one pass. The [CMMC Level 2 Asset Scoping Worksheet for NIST 800-171](https://payhip.com/b/2nzjO) ($47) sorts each asset into its 32 CFR 170.19 category as you go and flags what is missing from the SSP and network diagram.

**Check your own exposure.** Ask your MSP to search your public IP range for TCP port 102, or run the query yourself on Shodan or Censys. If anything answers, that is the finding you fix before anything else. If nothing answers, record the date and the method, because that record is the evidence behind your SSP sentence.

**Block port 102 at the perimeter and separate OT.** No controller should be reachable from the internet, and the production segment should sit behind a firewall that only permits the engineering workstation to talk S7comm. If the CAM workstation needs to push programs, that is one allowed host, one direction, logged.

**Set passwords and protection levels, then patch.** Every S7 controller should have password protection enabled and its protection level configured so that a session without credentials cannot write. Then bring firmware current, starting with any unit that has ever been internet-facing.

**Ask the integrator the direct question.** For any cell with remote support: how do you connect, from where, through what, and who else can. A cellular modem with a default configuration is the internet exposure the advisory describes, installed by a vendor you trust.

**Write it down.** Update the Specialized Assets section of the SSP so it states the exposure position, the controls you apply, the monitoring you do or do not have, and the review date. Update the network diagram to show the OT segment, the engineering host and every remote route. If the SSP, the scoring and the evidence behind it were built for the self-assessment and have not been touched since, the [CMMC Level 2 Readiness Kit: 5 NIST 800-171 Tools](https://payhip.com/b/LutGC) ($147) bundles the scoping worksheet, SSP template, SPRS workbook, evidence tracker and POA&M tracker into one set built for a small contractor doing this without a consultant.

## The bottom line

The CMMC scoping rule was written to keep old controllers from sinking a Level 2 assessment, and it does that job. What it asked in return was a written, risk-based policy, and for two years nobody defined the floor. On August 19, NSA, CISA, FBI, DOE and EPA defined it, not for CMMC but for anyone who owns a Siemens S7 PLC and does not want an AI-written script rewriting its logic. A small defense manufacturer now has a public benchmark for the one sentence in the SSP that no assessor is currently reading and one signature is currently standing behind. The fix is a week of inventory, a firewall rule, a firmware pass and a rewritten paragraph. The alternative is finding out from a port scan that the paragraph was fiction.

### Sources

- NSA, CISA, FBI, DOE, EPA, Joint Cybersecurity Advisory AA26-231A, "Defending Against an Active Threat to Siemens S7 Series PLCs," August 19, 2026: https://www.cisa.gov/news-events/cybersecurity-advisories/aa26-231a
- CISA, "Iranian-Affiliated Cyber Actors Exploit Programmable Logic Controllers," updated July 22, 2026
- 32 CFR 170.19, CMMC Scoping, Table 3 (Level 2 asset categories): https://www.law.cornell.edu/cfr/text/32/170.19
- DoD CIO, CMMC Level 2 Scoping Guide, version 2.13, September 2024: https://dodcio.defense.gov/Portals/0/Documents/CMMC/ScopingGuideL2v2.pdf
- 32 CFR 170.22, Affirmation
- DFARS 252.204-7012, Safeguarding Covered Defense Information and Cyber Incident Reporting
- Department of Defense, CMMC Phase 2 suspension memorandum and press release, July 13, 2026
- Mayer Brown, "False Claims Act Enforcement: Record-Breaking Year Signals Continued Attention to Cybersecurity," March 11, 2026 (DAAG Brenna Jenny remarks, January 2026)
- Help Net Security, "US agencies warn of AI-powered attacks on Siemens industrial controllers," August 20, 2026
