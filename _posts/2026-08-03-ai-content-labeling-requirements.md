---
layout: post
title: "AI Content Labeling Requirements: The Two Rules That Went Live on August 2, 2026"
date: 2026-08-03
description: "EU AI Act Article 50 and California's AI Transparency Act both became enforceable on August 2, 2026. What each one requires, and the third role that catches small firms."
category: AI Security
tags: [AI content labeling, EU AI Act, Article 50, California AI Transparency Act, SB 942, AB 853, ai governance, ai security, small business]
image: /blog/images/1-ai-content-labeling-requirements-hero.png
author: CyberZ
---
 
*The compliance press spent July watching Brussels. The rule that reaches further into a small American company was signed in Sacramento.*
 
**Two AI content labeling regimes became enforceable on August 2, 2026. The first is Article 50 of the EU AI Act, Regulation (EU) 2024/1689, which requires providers to mark synthetic output in a machine-readable format and requires deployers to disclose deepfakes and AI-generated text published to inform the public on matters of public interest. The second is the California AI Transparency Act, Business and Professions Code section 22757 and following, which requires covered providers of generative AI systems to publish a free AI detection tool, offer a visible manifest disclosure, and embed a latent disclosure in AI-generated image, video and audio content. California originally set its own start date at January 1, 2026, then moved it to August 2, 2026 to line up with the European timetable.**
 
<div class="key-takeaways" style="border-left:4px solid #EE4C48;background:#15151a;padding:18px 24px;margin:28px 0;border-radius:6px;">
<strong style="color:#EE4C48;letter-spacing:.04em;">KEY TAKEAWAYS</strong>
<ul style="margin:12px 0 0;padding-left:20px;">
<li>Two rules, one date. AB 853 moved California's operative date from January 1, 2026 to August 2, 2026, deliberately matching the EU Article 50 date.</li>
<li>California's core duties bind a narrow class: a person who creates, codes or otherwise produces a GenAI system with over 1,000,000 monthly visitors or users that is publicly accessible in the state. A firm that merely uses ChatGPT is not a covered provider.</li>
<li>There is a third role after provider and deployer. A third-party licensee of a covered provider's GenAI system carries a duty of its own under section 22757.3(c).</li>
<li>If a covered provider learns a licensee modified the system so it can no longer carry the latent disclosure, the provider must revoke the license within 96 hours. The licensee must then stop using it.</li>
<li>The civil penalty is $5,000 per violation, and for covered providers, platforms and device makers each day in violation counts separately. A city attorney or county counsel can sue, not only the Attorney General.</li>
<li>The EU granted exactly one grace period, running to December 2, 2026, and it covers only the machine-readable marking duty for generative systems already on the market. California granted none.</li>
</ul>
</div>
 
## Do you have to label AI-generated content in the United States?
 
There is still no federal statute that requires a general label on AI-generated content. What exists instead is a patchwork, and as of August 2 two pieces of that patchwork are live and enforceable at the same time.
 
Neither of them is a blanket rule that every AI-assisted email needs a badge. Both are narrower and stranger than the headlines suggest, and the practical answer for most small firms depends less on what you publish than on which role you occupy when the content is created.
 
We covered the interactive side of this in [AI chatbot disclosure requirements]({% post_url 2026-07-29-ai-chatbot-disclosure-requirements %}). That piece dealt with Article 50(1), the duty to tell a person they are talking to a machine. This one deals with the content itself, and with the American rule that landed the same morning.
 
![Side-by-side comparison of EU AI Act Article 50 and the California AI Transparency Act as of August 2, 2026, covering who each rule binds, the core duty, what pulls in a US firm, penalties, and grace periods.](/blog/images/2-ai-content-labeling-eu-vs-california.png)
 
## What does EU AI Act Article 50 require you to label?
 
Article 50 splits into duties that attach to different actors, and reading it as a single labeling rule is the most common way to get it wrong.
 
Article 50(2) sits on providers, including providers of general-purpose AI models. Their systems must mark generated audio, image, video and text output in a machine-readable format so that the output is detectable as artificially generated or manipulated. This is the invisible layer: watermarking, embedded metadata, provenance credentials. A person reading the content does not see it. A verifier does.
 
Article 50(4) sits on deployers, and this is the layer people do see. A deployer that uses an AI system to generate or manipulate image, audio or video content constituting a deep fake has to disclose that the content is artificially generated or manipulated. A separate duty in the same paragraph covers text: a deployer that publishes AI-generated or AI-manipulated text in order to inform the public on matters of public interest has to disclose that too.
 
That text duty carries the exception most business publishers will land in. It does not apply where the content went through human review or editorial control and a natural or legal person holds editorial responsibility for the publication. A marketing blog post drafted with AI, then read, edited and signed off by a named human, is a different object from an unreviewed automated feed.
 
Under Article 50(5), all of these disclosures have to reach the person clearly and distinguishably, at the latest at the time of first interaction or exposure, and in line with applicable accessibility requirements. A label that only appears after someone has already watched the video is not a label.
 
Penalties for transparency breaches sit at up to 15 million euros or 3 percent of worldwide annual turnover under Article 99(4). The 35 million euro figure that circulates in US coverage belongs to the prohibited-practices tier and is not the number here.
 
## Does the EU rule reach a company with no European entity?
 
It can. The Act applies to providers and deployers outside the Union where the output of the AI system is used in the Union, and the Digital Omnibus that amended the Act in July did not narrow that reach. Regulation (EU) 2026/1744 was published in the Official Journal on July 24, 2026 and entered into force on July 27. It deferred the high-risk regime. It left Article 50 where it was.
 
That distinction is doing real damage right now. A great deal of published guidance describes an August 2026 high-risk deadline that no longer exists, and some organizations stood their programs down on the strength of the delay headlines. Stand-alone Annex III high-risk obligations now apply from December 2, 2027, and product-embedded Annex I systems from August 2, 2028. Article 50 applied on schedule.
 
## Who counts as a covered provider under the California AI Transparency Act?
 
California's definition is narrow and worth reading literally. Section 22757.1(d) defines a covered provider as a person that creates, codes or otherwise produces a generative AI system that has over 1,000,000 monthly visitors or users and is publicly accessible within the geographic boundaries of the state.
 
Three elements have to line up. You have to produce the system, not merely use it. It has to clear a million monthly visitors or users. It has to be publicly accessible in California.
 
A 30-person accounting practice that runs client correspondence through a commercial chat assistant produces nothing. It is not a covered provider, and none of the three core duties below land on it directly.
 
For those who are covered, the duties are concrete:
 
- **Section 22757.2** requires a free AI detection tool that lets any user upload content or submit a URL, outputs any system provenance data found in that content, withholds personal provenance data, is publicly accessible, and exposes an API so it can be called without visiting the provider's website. The provider also has to collect user feedback on how well the tool works and feed that back into improving it.
- **Section 22757.3(a)** requires the provider to offer the user the option of a manifest disclosure, meaning a visible, clear, conspicuous marker that identifies the content as AI-generated and is permanent or extraordinarily difficult to remove.
- **Section 22757.3(b)** requires a latent disclosure embedded in AI-generated image, video and audio content. It has to convey the provider's name, the name and version number of the system, the time and date of creation or alteration, and a unique identifier. It has to be detectable by the provider's own detection tool, consistent with widely accepted industry standards, and permanent or extraordinarily difficult to remove.
 
Note what is absent from the latent-disclosure duty. It covers image, video and audio. It does not cover text. The EU marking duty in Article 50(2) does cover text. Two rules that landed on the same day do not have the same scope.
 
![Three roles under the August 2, 2026 AI content labeling rules: provider, deployer, and third-party licensee, with the specific duty attached to each and the governing citation.](/blog/images/3-ai-content-labeling-three-roles.png)
 
## What is a third-party licensee, and why does that role matter to a small firm?
 
Almost all coverage of these rules describes two roles. The provider builds. The deployer uses. California wrote in a third one, and it is the role a small technology company is most likely to occupy without noticing.
 
Section 22757.3(c) handles what happens when a covered provider licenses its GenAI system to somebody else. Three things follow.
 
First, the covered provider has to require by contract that the licensee maintain the system's capability to include the latent disclosure in content it creates or alters. That clause is now sitting in license agreements whether or not anyone on your side read it.
 
Second, if the covered provider knows that a licensee modified the licensed system so that it can no longer include that disclosure, the provider has to revoke the license within 96 hours of discovering it. Not at renewal. Not after a remediation conversation. Within 96 hours.
 
Third, and this is the part that binds you directly, a third-party licensee has to cease using a licensed GenAI system after the license has been revoked.
 
That third duty is enforceable against the licensee. Section 22757.4(c) gives the Attorney General, a county counsel or a city attorney a civil action against a third-party licensee for violating it, seeking injunctive relief plus reasonable attorney's fees and costs. Section 22757.4(a) sets the general civil penalty at $5,000 per violation and entitles a prevailing plaintiff to costs and fees. Section 22757.4(b) makes each day of violation a discrete violation for covered providers, large online platforms and capture device manufacturers.
 
The operational risk is not exotic. A small SaaS company or agency white-labels a large provider's image or voice generation into its own product. Somewhere in the integration, an engineer strips metadata during a re-encode, or disables provenance embedding because it broke a file-size budget, or routes output through a pipeline that flattens it. The provider notices. The clock starts. The product loses its engine, and continuing to run it converts a technical decision into a statutory violation with a city attorney on the other side.
 
If your team has an AI vendor inventory, the license terms belong in it. If it does not, that is the gap to close first. The governance side of that inventory is the subject of [AI acceptable use policy for small business]({% post_url 2026-07-07-ai-acceptable-use-policy-small-business %}).
 
## Could the one-million-user threshold disappear?
 
This is the part to watch, because it would change who is covered without any new deadline attached.
 
Senate Bill 1000, authored by the same legislator who wrote the original SB 942, would amend the AI Transparency Act to delete the user threshold from the definition of covered provider, replace the AI detection tool with a disclosure verification tool, remove the manifest-disclosure option, and require the latent disclosure to state whether the content was generated or modified by AI. It carries an urgency clause, which means it takes effect immediately on signature rather than waiting for a January operative date.
 
As of this writing the bill has not been enacted. Treat the million-user threshold as the current law and as a moving part, not as a permanent exemption. Any firm that concluded it was out of scope purely because of that number should know the number is the thing being litigated in Sacramento.
 
![Timeline of AI content transparency dates from August 2, 2026 through August 2, 2028, marking which obligations are live now and which are still ahead under the EU AI Act and the California AI Transparency Act.](/blog/images/4-ai-content-labeling-deadline-timeline.png)
 
## What should a small firm actually do this month?
 
Five things, in order, none of which require a consultant.
 
**Inventory the surface, not the models.** List every place AI-generated or AI-modified image, audio, video or public-facing text leaves your organization. Marketing video, voice agents on the phone system, generated product imagery, automated news or market summaries, synthetic training material. Most firms find touchpoints in products that predate their AI policy.
 
**Decide your role for each one, in writing.** Provider, deployer, licensee. The same organization is frequently more than one at the same time for different systems, and the duties do not transfer between roles. A deployer cannot satisfy its own visible-disclosure duty by pointing at the provider's embedded mark.
 
**Read the license terms for anything you resell or embed.** You are looking for the clause that requires you to preserve disclosure capability, and for revocation language. If you cannot find it, ask the vendor in writing and keep the answer.
 
**Establish who holds editorial responsibility for published text.** The Article 50(4) text exception depends on human review and a person or organization holding editorial responsibility. That is a named-owner question, and it is much easier to answer before someone asks than after.
 
**Fix the timing of your visible disclosures.** First interaction or exposure, clear and distinguishable, accessible to a screen reader. A footer note or a line in the terms of service does not meet that standard.
 
If your firm is publishing synthetic media or embedding a licensed generative system and has no written internal rule governing either, the [AI Acceptable Use Policy Kit](https://payhip.com/b/AKSw2) ($47) gives you the policy language, the acceptable-use boundaries and the vendor questions to start from.
 
## The bottom line
 
August 2 was not one deadline. It was two rules from two jurisdictions that were deliberately synchronized, with different scopes, different penalty structures, and one grace period between them that expires on December 2, 2026.
 
For most small firms the honest answer is that the heavy duties land elsewhere, on the large providers. The exposure that does reach you sits in two places: the visible disclosure you owe as a deployer of synthetic media, and the license clause you inherited as a third-party licensee. Those are both readable in an afternoon. The cost of not reading them is measured in $5,000 increments per day.
 
## Sources
 
- Regulation (EU) 2024/1689 (Artificial Intelligence Act), Article 50 and Article 99(4). Official Journal L, 2024/1689, 12.7.2024.
- Regulation (EU) 2026/1744 (Digital Omnibus on AI), amending Regulation (EU) 2024/1689. Official Journal L, 2026/1744, 24.7.2026. In force 27 July 2026.
- European Commission, *Guidelines on the implementation of the transparency obligations for certain AI systems under Article 50 of the AI Act*, adopted 20 July 2026.
- California Business and Professions Code, Division 8, Chapter 25 (California AI Transparency Act), sections 22757.1, 22757.2, 22757.3, 22757.4, 22757.5 and 22757.6.
- California Assembly Bill 853 (Wicks), Stats. 2025, Ch. 674. Approved by the Governor 13 October 2025. Amends sections 22757.1, 22757.4 and 22757.6 and adds sections 22757.3.1, 22757.3.2 and 22757.3.3.
- California Senate Bill 942 (Becker), Stats. 2024, Ch. 291, which created the chapter.
- California Senate Bill 1000 (Becker), 2025 to 2026 Regular Session. Pending, not enacted as of publication.
