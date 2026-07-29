---
layout: post
title: "AI Chatbot Disclosure Requirements: What US Companies Must Do by August 2, 2026"
date: 2026-07-29
description: "EU AI Act Article 50 applies August 2, 2026. The four-condition test that decides whether your chatbot needs an AI disclosure, and why US companies are in scope."
category: AI Security
tags: [EU AI Act, Article 50, ai disclosure, ai chatbot, ai governance, ai security, small business]
image: /blog/images/1-ai-chatbot-disclosure-requirements-hero.png
author: CyberZ
---

*Most coverage of the EU AI Act this month has been about what got postponed. Something did not get postponed, and it lands on Sunday.*

**AI chatbot disclosure is the requirement in Article 50(1) of the EU AI Act that a provider must design an AI system that interacts directly with people so that those people are informed they are dealing with an AI system, unless that fact is obvious. It applies from August 2, 2026. It is not limited to high-risk systems, and it reaches companies outside the EU whose AI output is used inside the EU. Fines run up to 15 million euros or 3% of total worldwide turnover for the preceding financial year, whichever is higher.**

<div class="key-takeaways" style="background:#16161a;border-left:4px solid #EE4C48;padding:20px 24px;margin:24px 0;">
<strong>Key Takeaways</strong>
<ul>
<li>Article 50 was not delayed. Regulation (EU) 2026/1744, the Digital Omnibus on AI, moved the high-risk obligations to December 2027 and August 2028. It left the transparency obligations on August 2, 2026.</li>
<li>Four conditions must all be true before the disclosure duty applies. A system that only collects data, or only returns canned automated responses, does not meet the second condition.</li>
<li>Provider duties and deployer duties are separate. A deployer cannot satisfy its own labelling duty by pointing at the machine-readable mark the provider embedded.</li>
<li>The penalty figure circulating in US-facing coverage is often wrong. 35 million euros or 7% is the prohibited-practices tier. Transparency breaches sit at 15 million euros or 3%.</li>
<li>The only grace period runs to December 2, 2026, applies only to generative systems already on the market before August 2, and covers only the marking and detection obligation.</li>
</ul>
</div>

There is a reason this one is easy to miss. For most of 2026 the story was whether the EU would push its deadlines, and on July 27 it did. Regulation (EU) 2026/1744 entered into force and moved the obligations for stand-alone high-risk systems from August 2, 2026 to December 2, 2027, with product-embedded high-risk systems going to August 2, 2028. A great deal of published guidance now describes an August 2026 high-risk deadline that no longer exists.

Article 50 sits in a different chapter of the Act, and it did not move. On July 20 the European Commission adopted its final Guidelines on the transparency obligations under Article 50, alongside a Code of Practice on Transparency of AI-Generated Content. Those Guidelines are the first document that tells an operator how to decide whether it is in scope, rather than simply asserting that chatbots must be labelled.

## Does the EU AI Act apply to a US company with no EU office?

It can, and the Commission says so directly. Providers of AI systems established or located outside the EU fall within the Act if the output of their AI system is used in the EU. The trigger is where the output lands, not where the company is incorporated or where the servers sit.

For a 30-person US firm that reads as follows. If your website chat widget answers questions from a prospective customer in Ireland, the output of that system is being used in the EU. If your practice uses an AI intake assistant and one of your patients is a German national receiving care in Frankfurt, same answer. The absence of a European entity does not remove you from scope, in the same way it did not under GDPR.

What does remove you from scope is failing any one of the four conditions below.

## Which four conditions must all be true before Article 50(1) applies?

The Commission's Guidelines set out four cumulative criteria. Cumulative is the operative word. All four have to be satisfied.

![Four numbered conditions from the European Commission Guidelines that must all be true before the Article 50(1) AI disclosure duty applies: the system qualifies as an AI system, it is built for genuine two-way exchange, the interaction is direct, and the other party is a natural person.](/blog/images/2-article-50-four-condition-scoping-test.png)

The second condition is where most small deployments actually fall out. The Guidelines distinguish a system designed for genuine two-way exchange with people from one that merely collects data or provides automated responses. A form that captures a name and email and fires an autoresponder is not having an exchange. A decision-tree phone menu is not having an exchange. A large language model that reads what the customer typed, holds context, and answers is.

The third condition, directness, excludes the case where a human sits between the AI and the person. If your support agent uses an AI tool to draft a reply and then reads, edits and sends it under their own name, the AI is not communicating directly with the customer. Your agent is. Systems that run purely in the background, or communicate machine to machine, are outside this obligation entirely.

That distinction matters more as firms adopt agentic tooling, because an agent that emails a client on its own initiative has crossed from the third condition into scope. We covered the permission side of that problem in [AI agent security risks]({% post_url 2026-07-02-ai-agent-security-risks-small-business %}); this is the disclosure side of the same deployment decision.

## When must the disclosure appear, and what does clear and distinguishable mean?

People must be informed from the start of the first interaction, in a clear and distinguishable manner, and in accordance with accessibility requirements. Three separate constraints sit in that sentence.

Timing is the start of the first interaction, not somewhere later in the conversation and not in a policy page the user would have to go looking for. Clear and distinguishable means the disclosure has to be perceivable as a disclosure rather than blended into decorative interface copy. The accessibility requirement means a purely visual cue is thin if the same information is not available to someone using a screen reader.

The practical version for a website chat widget is a labelled opening state that says what the user is talking to, in the widget itself, before the first exchange, in text a screen reader will read.

## When is it obvious enough that no disclosure is needed?

Article 50(1) does not apply where it is obvious to the person that they are interacting with AI. The Guidelines put a specific test behind that word. The assessment is made from the position of an average person who is reasonably well-informed, reasonably observant and circumspect, and the Commission states the exception should be interpreted restrictively, because it removes transparency the provision exists to create.

Read that as a narrow exit, not a general excuse. An interface named after a well-known assistant product, presented as a machine, in a context where no reasonable user would expect a human, may qualify. A friendly first-name persona with a stock human avatar does not, and arguably points the other way.

## What does the provider owe, and what does the deployer owe?

Article 50 splits duties by role, and one organisation is frequently both at once for different systems. If you built the tool and put it on the market under your own name, you are a provider. If you use somebody else's tool under your own authority in the course of business, you are a deployer.

![Comparison of Article 50 provider duties under Articles 50(1), 50(2) and 50(5) against deployer duties under Articles 50(3) and 50(4), with a note that a deployer cannot rely on the provider's machine-readable mark to satisfy its own disclosure obligation.](/blog/images/3-article-50-provider-vs-deployer-duties.png)

Two details in that split are worth more than the rest.

First, the Commission is explicit that a deployer cannot simply rely on the machine-readable marking the provider embedded under Article 50(2) to discharge its own disclosure obligation. The provider's mark is machine-facing provenance. The deployer's disclosure has to be understandable and perceivable by a person, with visible or audible labels, without the person needing special tools or extra steps. Buying a compliant tool does not transfer your duty to you having done nothing.

Second, the deployer definition catches sole operators. Using AI in a personal, non-professional capacity is outside the Act. But where a natural person uses an AI system in an activity through which they gain economic benefit on a regular basis, or otherwise as part of a business, trade, occupational or freelance activity, that person is a deployer. Employees acting under their employer's instruction and control are not separate deployers, and a company remains the deployer even where contractors or freelancers operate the system on its behalf.

## Does AI-drafted text on your company blog need a label?

Only in a narrower band than the headlines suggest. Article 50(4) requires deployers to label AI-generated or manipulated text published to inform the public on matters of public interest. Three things must be true: the text is published, it is informative to the public, and it concerns a matter of public interest.

The Commission's list of public-interest matters includes politics and democratic processes, public administration and services, administration of justice and law enforcement, fundamental rights, public security, public health, environmental protection, consumer safety, and economic, financial, political, scientific or cultural developments that may be a relevant subject of public debate.

Then there is the exemption that most business publishing will actually rely on. Text that has undergone human review or editorial control does not need to be labelled. The Guidelines define that as deliberate examination of the substance by a person with relevant knowledge and professional judgement, or control exercised by a responsible editorial entity with authority to approve, alter or reject the substance. They also say what does not count: superficial, solely formal or procedural checks, and they name spell-checking and grammatical correction specifically.

So an AI-drafted article on public health that a qualified person actually read for substance and stands behind is outside the labelling duty. The same article run through a grammar checker and published is not. Editorial responsibility means somebody holds ultimate legal responsibility for the publication.

Deepfakes are handled separately in the same paragraph, using the definition in Article 3(60), and must be disclosed to a person on first exposure at the latest. If synthetic voice or video is anywhere in your marketing or training material, the labelling analysis is different from the fraud analysis we ran in [deepfake fraud protection]({% post_url 2026-07-20-deepfake-fraud-protection-small-business %}).

## What is the penalty, and why is the 35 million euro figure wrong?

The Commission states that fines for breaching Article 50 can reach up to 15 million euros or 3% of total worldwide turnover for the preceding financial year, and that proportionality can be taken into account for small and medium-sized enterprises and small mid-cap companies.

Several US-facing compliance guides currently quote 35 million euros or 7% for AI Act non-compliance generally. That is the prohibited-practices tier under Article 5, which covers things like the newly inserted bans on AI systems generating non-consensual intimate material and child sexual abuse material. It is not the transparency tier. Using the wrong number is not a harmless exaggeration when a business owner is deciding how much budget to point at this.

Enforcement is mainly national. Market surveillance authorities in the member states carry it. The AI Office has a limited role, competent only for AI systems built on general-purpose AI models where the same entity provides both the system and the model, or where the system is integrated into a very large online platform or search engine designated under the Digital Services Act.

## What actually changes on December 2, 2026?

One narrow thing. The grace period applies only to AI systems placed on the market before August 2, 2026, and only to the marking and detection obligation for AI-generated content in Article 50(2). Providers of those systems must comply from December 2, 2026.

![Timeline of EU AI Act dates after the Digital Omnibus: Article 50 transparency on August 2 2026, Article 50(2) marking catch-up on December 2 2026, Annex III high-risk on December 2 2027, and Annex I high-risk on August 2 2028.](/blog/images/4-eu-ai-act-article-50-timeline-2026.png)

Everything else in Article 50 starts on August 2 with no runway. The chatbot disclosure in 50(1), the emotion recognition and biometric categorisation notice in 50(3), and the deepfake and public-interest text labelling in 50(4) are all live on day one. Content generated before August 2 does not need to be labelled retroactively, although the Commission encourages it where possible. Bird & Bird's reading of the final Guidelines is that for published text the relevant moment is the date of publication rather than the date of generation, which would mean text drafted in July but published in August is in scope.

There is also a voluntary route to demonstrating compliance. The Code of Practice on Transparency of AI-Generated Content has been assessed as adequate by both the Commission and the AI Board, and covers Articles 50(2), 50(4) and 50(5). Signatories get predictability. Operators who decline it have to demonstrate compliance by other adequate means and, in the Commission's words, may be subject to more requests for information.

One thing to hold onto: the Guidelines are not binding law. Only the Court of Justice can give an authoritative interpretation of the Act. In practice, national market surveillance authorities can be expected to work from them, which makes them the best available description of what an enforcement conversation will sound like.

## What to do this week

1. **Inventory every AI system that talks to a human on your behalf.** Website chat, phone assistants, intake forms with a model behind them, agents that send email. One line each: what it is, who built it, whether it reaches anyone in the EU.
2. **Run the four conditions against each one.** Write down which condition fails where you conclude you are out of scope. That note is your evidence if anyone asks later.
3. **Decide your role per system, provider or deployer.** Do not assume one answer covers your whole stack. A tool you built and a tool you licensed put you in different chairs.
4. **Fix the opening state of anything in scope.** Disclosure at first interaction, in the interface, in text a screen reader reads. This is usually a copy change, not an engineering project.
5. **Ask your AI vendors two questions in writing.** Are your generative outputs marked in a machine-readable format under Article 50(2), and have you signed the Code of Practice on Transparency of AI-Generated Content. Keep the answers.
6. **Separate your deployer labelling from the vendor's marking.** If you publish synthetic audio or video, or AI text on a public-interest subject without substantive human review, you owe a human-perceivable label regardless of what the vendor embedded.
7. **Write the review trigger down.** Note who decided scope, on what date, against which version of the Guidelines. That is the cheapest artifact you will ever create and the first one anyone will ask for.

The firms that get caught here will not be the ones that read the regulation and decided they were out of scope. They will be the ones that never ran the test, and cannot say why they thought they were fine.

An [AI acceptable use policy]({% post_url 2026-07-07-ai-acceptable-use-policy-small-business %}) is where the scope decision, the vendor questions and the disclosure standard should live once you have made them, so the next person to deploy a tool does not have to work it out again.

{% include cmmc-signup.html %}

## Sources

- Regulation (EU) 2024/1689 (Artificial Intelligence Act), Article 50, Article 3(3), Article 3(60), Article 99. Official Journal L, 2024/1689, 12.7.2024.
- Regulation (EU) 2026/1744 (Digital Omnibus on AI), amending Regulation (EU) 2024/1689. Official Journal L, 2026/1744, 24.7.2026. In force 27 July 2026.
- European Commission, *Guidelines on the implementation of the transparency obligations for certain AI systems under Article 50 of the AI Act*, adopted 20 July 2026.
- European Commission, *Transparency obligations under Article 50 of the AI Act* (Questions and Answers), Shaping Europe's digital future, last updated 20 July 2026.
- European Commission, *Code of Practice on Transparency of AI-Generated Content*, Shaping Europe's digital future.
- European Commission press release IP/26/1653, *Commission publishes guidelines on transparency obligations for providers and deployers of certain AI systems*, 20 July 2026.
- Bird & Bird, *European Commission adopts final Guidelines on AI Act Article 50 transparency obligations: first impressions*, July 2026.

