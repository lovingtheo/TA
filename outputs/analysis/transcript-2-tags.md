# Transcript 2 Tags — dovetail-transcript-2026-04-23 (1).vtt

**Participant:** P2 (Mark)
**Interviewer:** Jin Kang
**Study:** Survey workflow + AI tool concept evaluation (Study B)
**Date coded:** 2026-04-23
**Codebook type:** Emergent only (no predefined codes applied per researcher instruction; codebook independent from Study A)

---

## Code Table

| Code | Definition | # of quotes |
|------|-----------|-------------|
| B-EC1: Business Context Prerequisite | User requires AI to have prior knowledge of the company's industry, audience, and products before it provides useful survey assistance — generic AI lacking this context is seen as insufficiently valuable | 4 |
| B-EC2: Cross-System Data Access as Analysis Prerequisite | User views cross-system data integration (survey platform + CRM) as essential for meaningful analysis — embedded AI within the survey platform alone lacks the respondent context needed for segmentation insights | 7 |
| B-EC3: Human Drafts, AI Refines | User retains creative and strategic ownership of initial survey content; AI is delegated refinement of existing drafts rather than generation from scratch | 2 |
| B-EC4: AI as Strategic Survey Advisor | User engages AI not just for wordsmithing but for strategic survey design — question effectiveness, completion risk, goal alignment. AI functions as a thinking partner | 2 |
| B-EC5: LLM Integration as Orchestration Hub | User envisions an external LLM integration (not the survey platform) as the central hub for the full survey lifecycle, pulling in the survey platform as one data source among many connected systems | 5 |
| B-EC6: Survey Process Continuity Memory | User expects AI to retain the full goal, iteration history, and decision rationale from survey creation through to analysis, so analysis outputs remain aligned with original intent | 2 |
| B-EC7: PII Selective Forgetting Requirement | User requires AI to reliably delete specific sensitive fields (e.g., PII inadvertently loaded from CRM enrichment) on demand; expresses concern that current AI platforms fail to honor forget requests reliably | 2 |
| B-EC8: Data Enrichment Bottleneck | Current analysis workflow requires manual spreadsheet work (VLOOKUPs) to join survey and CRM data before AI can perform segmentation — this is time-consuming, error-prone, and the primary analysis pain point | 2 |
| B-EC9: Proactive AI Monitoring | User wants AI to proactively surface interim survey performance data (response rates, benchmarks vs. historical surveys) without manual checking, enabling real-time answers to stakeholder queries | 3 |
| B-EC10: Corporate Authorization Barrier | Organization has not yet authorized connecting AI systems to external platforms despite daily AI use — organizational approval is the missing piece for adopting LLM integration | 1 |
| B-EC11: Embedded AI Domain Specialization Value | The unique value user attributes to embedded AI in a survey platform is deep specialization in survey methodology — an advantage over general-purpose external LLMs that are "pseudo-expert in everything" | 2 |
| B-EC12: Feature Completeness as Switching Criterion | User's choice between embedded chat and LLM integration depends on whether the integration delivers a fully end-to-end experience; if it requires returning to the survey platform for any step, it loses its advantage | 2 |
| B-EC13: Historical Survey Performance as AI Context | User wants AI to learn from past survey performance data (question phrasing, length, drop-off, audience-specific effectiveness) to proactively guide current and future survey design | 2 |
| B-EC14: Ideal State — End-to-End Survey Wizard | User envisions the ultimate solution as an AI wizard that handles the full survey lifecycle (build → execution → analysis → packaging) with contextual awareness of each stage's requirements | 1 |

---

<details>
<summary><strong>B-EC1: Business Context Prerequisite</strong> — 4 quotes</summary>

**Definition:** User requires AI to have prior knowledge of the company's industry, audience, and products before it provides useful survey assistance — generic AI lacking this context is seen as insufficiently valuable.

---

**Quote 1** | `00:11:35–00:12:10` | Confidence: **strong**

> "The question is, Does the AI have the contextual knowledge of our business? So is it the same AI that's ingesting all of the data that we're putting into it every day so that over time it's learning about our business? That's the only thing that gives me pause because if it, if it's just in a vacuum and it's AI that helps you build a survey, but understands nothing about your business, then that's a drawback for us."

*Rationale:* Primary statement of the prerequisite — AI business context determines whether embedded AI is genuinely useful or merely generic. "In a vacuum" is user's framing for the risk case.

---

**Quote 2** | `00:12:39–00:13:52` | Confidence: **strong**

> "Just understanding, um, our target audience, the industry, um, how our products are priced and sold... I'd be more comfortable interacting with an AI that has been trained on our business than one that's just brand new to us."

*Rationale:* Names the specific categories of business context that matter: audience, industry, pricing/sales model. Comfort level tied directly to prior AI training on their data.

---

**Quote 3** | `00:13:22–00:13:52` | Confidence: **strong**

> "If it understands our business, it's likely to have a better chance of understanding what types of questions are bound to elicit responses, especially things like open-ended questions, like how to get people to talk, understanding our personas... just helping phrase the questions in a way that resonates with them."

*Rationale:* Links business context to concrete survey quality outcomes — better question phrasing, audience-resonant language, higher response rates.

---

**Quote 4** | `00:32:31–00:33:38` | Confidence: **strong**

> "It wouldn't necessarily, um, no, how it's performing, because it doesn't — the way we operate surveys, it doesn't know the audience that's receiving the survey. So it's not going to know if it's been sent to the same audience as the last survey we sent... it's not going to have any contextual data around, you've got a lot of high-value customers answering this survey, because it knows nothing about who is a high-value customer versus a customer with a lower spend."

*Rationale:* Shows how the absence of business context in embedded AI specifically disables meaningful monitoring — the AI can count responses but cannot assess their significance.

</details>

---

<details>
<summary><strong>B-EC2: Cross-System Data Access as Analysis Prerequisite</strong> — 7 quotes</summary>

**Definition:** User views cross-system data integration (survey platform + CRM) as essential for meaningful analysis — embedded AI within the survey platform alone lacks the respondent context needed for segmentation insights.

---

**Quote 1** | `00:11:41–00:12:17` | Confidence: **moderate**

> "Not to skip ahead, but the real drawback would come at the analysis stage where we need to map the data with other systems."

*Rationale:* First mention — anticipates analysis as the point where single-system limitation becomes most consequential.

---

**Quote 2** | `00:27:50–00:28:41` | Confidence: **strong**

> "A lot of the time we want this data to pass through to Salesforce, so it's a manual process of creating new fields, creating maybe with Zapier, like an integration that takes this, the survey response data and maps it to fields in Salesforce... In a future state, I would love for AI to simplify those kind of integration pieces. And again, that's where you need to have an AI that's capable of accessing SurveyMonkey, but also accessing your CRM and other platforms."

*Rationale:* Names cross-system access as the prerequisite for solving the integration pain point — AI must reach both SurveyMonkey and CRM simultaneously.

---

**Quote 3** | `00:33:54–00:34:27` | Confidence: **strong**

> "Well, I think the first idea, it's going to have access to everything in our SurveyMonkey account... but because we're deploying the surveys externally, it's really just a bunch of questions and answers. There's no insight into the audience or who these people are who are answering. It's all anonymous versus the second option would have a whole bunch of contextual data around yeah, who these people are, what, how different questions are trending with different segments and personas."

*Rationale:* Direct comparison between embedded AI (anonymous survey data only) and LLM integration (full customer context through CRM access) — defines the capability gap.

---

**Quote 4** | `00:35:40–00:36:35` | Confidence: **strong**

> "The real power comes with mapping the results to the users in Salesforce with all the rest of their data. So that once we do that, if we pull in additional fields like account value and job title and a whole host of other data points, then there's a richer data set for the AI to analyze and spit out trends that would be very difficult for us to uncover manually."

*Rationale:* States the analytical value proposition of cross-system access — enriched data enables pattern detection beyond human capacity.

---

**Quote 5** | `00:37:04–00:38:46` | Confidence: **strong**

> "Today, yeah [manual upload]. But future state, what we're talking about with idea number 2 is that all of that is automated and it just knows how to map that data. So that would be really time-saving and really powerful."

*Rationale:* Positions automated cross-system data mapping as the primary future-state benefit of the LLM integration concept.

---

**Quote 6** | `00:39:52–00:40:07` | Confidence: **strong**

> "For all of that, it would be option 2 for me. I just don't think option 1 would be robust enough. I don't think it would have access to enough data to do a fulsome analysis."

*Rationale:* Definitive preference for LLM integration over embedded AI for analysis — data access depth is the decisive factor.

---

**Quote 7** | `00:44:32–00:44:50` | Confidence: **moderate**

> "Yeah, I guess it's that. It's that segmentation piece. It's industry analysis and it's also persona analysis. Is something resonating more with the C-suite people versus managers who are lower level, that sort of thing."

*Rationale:* Names the specific segmentation outputs that require cross-system data — CRM fields (job title, business unit) make industry and persona breakdowns possible.

</details>

---

<details>
<summary><strong>B-EC3: Human Drafts, AI Refines</strong> — 2 quotes</summary>

**Definition:** User retains creative and strategic ownership of initial survey content; AI is delegated refinement of existing drafts rather than generation from scratch.

---

**Quote 1** | `00:14:37–00:15:36` | Confidence: **strong**

> "In my experience, it's usually quicker to come with some sort of draft. So it would be pretty rare, if ever, that I would just ask the AI to craft a survey. I would at least have some sample questions that I'd want to get after... I'm always going to have some sort of draft questions, but really I'm looking to the AI to refine the questions, to use its aggregate knowledge of like the survey discipline to understand how to ask questions to elicit the right responses."

*Rationale:* Clear articulation of human-AI task boundary: human owns the draft; AI owns the refinement. "Pretty rare, if ever" signals this is a firm default, not a preference.

---

**Quote 2** | `00:07:19–00:07:57` | Confidence: **strong**

> "This one was suggested by somebody outside of our team, so by our product team. So it would have been meeting with them to understand their requirements, what they're trying to get out of it. They typically would come with some draft survey questions, which we would then take and refine, usually with the help of AI."

*Rationale:* Concrete description of the intake process — human stakeholders generate draft content, user's team refines it with AI assistance. AI enters after the first human draft exists.

</details>

---

<details>
<summary><strong>B-EC4: AI as Strategic Survey Advisor</strong> — 2 quotes</summary>

**Definition:** User engages AI not just for wordsmithing but for strategic survey design — question effectiveness, completion risk, goal alignment. AI functions as a thinking partner.

---

**Quote 1** | `00:07:59–00:08:17` | Confidence: **strong**

> "The refining stage is more than just wordsmithing. It's talking to the AI about strategy, about our goals, and are we likely to get the information we're looking for from these questions? Is it too long? Are people likely to abandon the survey? How can we make it tighter? Those sort of strategic elements as well as just like drafting the content."

*Rationale:* Explicitly distinguishes the strategic advisory role from the editorial role — AI evaluates survey design quality against research goals, not just prose quality.

---

**Quote 2** | `00:08:36–00:09:12` | Confidence: **moderate**

> "There's usually a second step where we'll go back and say, listen, AI, so-and-so really wants to include this. How do we work this into the survey?"

*Rationale:* AI is re-engaged as a design advisor when stakeholder requests threaten survey coherence — positions AI as mediator between stakeholder wishes and survey integrity.

</details>

---

<details>
<summary><strong>B-EC5: LLM Integration as Orchestration Hub</strong> — 5 quotes</summary>

**Definition:** User envisions an external LLM integration (not the survey platform) as the central hub for the full survey lifecycle, pulling in the survey platform as one data source among many connected systems.

---

**Quote 1** | `00:21:19–00:22:10` | Confidence: **strong**

> "It seems to me in the future state, it's going to be easier for something like Claude to connect all those systems than it would be in SurveyMonkey. So when you start talking about everything other than just survey creation, like collaboration, like analysis, then I think all roads are starting to lead to an external, primarily AI solution that pulls in SurveyMonkey as the survey component. I just don't think it's realistic to expect a tool like SurveyMonkey to be the home base that connects to all these tools."

*Rationale:* Definitive framing of the architecture: LLM integration = hub; SurveyMonkey = a component. SurveyMonkey cannot serve as orchestration center.

---

**Quote 2** | `00:22:47–00:23:15` | Confidence: **strong**

> "I guess it would need to be full-featured enough that I didn't need to do part of it in Claude and log in and do part of it in SurveyMonkey. So as long as I could build, iterate, launch, analyze."

*Rationale:* Sets the bar for LLM integration adoption: full lifecycle coverage (build → iterate → launch → analyze) without returning to the survey platform.

---

**Quote 3** | `00:30:44–00:31:12` | Confidence: **strong**

> "Yeah, I think this, the second idea, the having the external AI be the hub for things can help with the integration piece because it's going to be able to connect to various platforms. It's going to be able to hopefully test things for you without a lot of manual work and clicks."

*Rationale:* Identifies "hub for things" as the precise function — LLM integration manages connections to external systems and reduces manual orchestration effort.

---

**Quote 4** | `00:31:22–00:32:23` | Confidence: **moderate**

> "An external AI would have the context of how it's doing in relation to your other surveys that you ran to a similar audience. So it could say, hey, we're only 3 hours in, you've already got 100 responses, this is trending a lot better than the last survey you ran. And that's an answer I can give to our CEO if he asks me."

*Rationale:* Extends hub role to monitoring — LLM integration can cross-reference current survey performance against historical data from previous surveys, enabling real-time stakeholder reporting.

---

**Quote 5** | `00:39:52–00:40:24` | Confidence: **strong**

> "For all of that, it would be option 2 for me. I just don't think option 1 would be robust enough... And yeah, at that point, if we're just preparing, synthesizing the data and preparing it and creating PowerPoints, then I don't see the advantage of going back into SurveyMonkey for that."

*Rationale:* Confirms LLM integration as preferred environment for all post-creation stages — synthesis, reporting, and packaging all done outside the survey platform.

</details>

---

<details>
<summary><strong>B-EC6: Survey Process Continuity Memory</strong> — 2 quotes</summary>

**Definition:** User expects AI to retain the full goal, iteration history, and decision rationale from survey creation through to analysis, so analysis outputs remain aligned with original intent.

---

**Quote 1** | `00:46:22–00:47:24` | Confidence: **strong**

> "It should understand all of the thought and back and forth and iteration that went into the survey creation process. So it should understand what were my goals coming into this, how did the survey evolve from an initial idea to what it is now, because it sort of needs to understand the evolution of all that to know what data analysis outputs are going to be relevant, right? So if it can map back to the original goals, then that's ideal rather than just starting from the dataset and not knowing all the history."

*Rationale:* Most direct statement of continuity memory requirement — goal, evolution, and iteration history must carry from creation to analysis for the analysis to be meaningful.

---

**Quote 2** | `00:47:46–00:48:15` | Confidence: **strong**

> "I think it would be time-consuming and annoying because you would have to sort of remind — retrain it on all the work that was done external to it. You'd probably be copying and pasting conversations over for it to understand how we got to this point... Yeah, it would probably be frustrating enough that I wouldn't want to do that on a regular basis."

*Rationale:* States the consequence of absent continuity memory — manual context re-entry (copy-pasting conversation history) is friction severe enough to deter regular use.

</details>

---

<details>
<summary><strong>B-EC7: PII Selective Forgetting Requirement</strong> — 2 quotes</summary>

**Definition:** User requires AI to reliably delete specific sensitive fields (e.g., PII inadvertently loaded from CRM enrichment) on demand; expresses concern that current AI platforms fail to honor forget requests reliably.

---

**Quote 1** | `00:53:33–00:54:13` | Confidence: **strong**

> "Yeah, it should, depending on, you know, rules we have around PII, it should help us to remove that sort of data from its memory. It should allow me to be specific and prescriptive about what I want it to forget, which is — I found even with the big AI platforms, if you ask it to forget something, it will, it will clearly not do that sometimes."

*Rationale:* Names PII as the primary category requiring selective deletion and surfaces a documented failure of current AI platforms to comply with forget requests — this is a real, tested concern.

---

**Quote 2** | `00:55:02–00:55:37` | Confidence: **strong**

> "It's more when we're enriching the data with more data from Salesforce. So, you know, there's no value to including phone numbers or anything like that. But you know, you might unintentionally load something like that into an AI and then say, oh, please disregard that column from that spreadsheet forever."

*Rationale:* Provides the concrete scenario — accidental PII inclusion during Salesforce data enrichment. "Disregard forever" is the user's framing of the required forgetting behavior.

</details>

---

<details>
<summary><strong>B-EC8: Data Enrichment Bottleneck</strong> — 2 quotes</summary>

**Definition:** Current analysis workflow requires manual spreadsheet work (VLOOKUPs) to join survey and CRM data before AI can perform segmentation — this is time-consuming, error-prone, and the primary analysis pain point.

---

**Quote 1** | `00:27:50–00:28:38` | Confidence: **strong**

> "A lot of the time we want this data to pass through to Salesforce, so it's a manual process of creating new fields, creating maybe with Zapier, like an integration that takes this, the survey response data and maps it to fields in Salesforce... In a future state, I would love for AI to simplify those kind of integration pieces."

*Rationale:* Identifies the integration setup itself (not just analysis) as a manual bottleneck — creating fields and building Zapier flows for each survey is slow, error-prone, and requires testing.

---

**Quote 2** | `00:37:51–00:38:46` | Confidence: **strong**

> "The heavy lifting is in, it's in spreadsheets, right? So you're taking the raw data and you're enhancing it with Salesforce data. So, you know, you've got two tabs, you're doing VLOOKUPs to pull in fields into the survey data and doing all that data work to get a larger data set that you can then plug back into the AI... But future state, what we're talking about with idea number 2 is that all of that is automated and it just knows how to map that data."

*Rationale:* Detailed description of the manual data join process — VLOOKUPs between two spreadsheet tabs is the current solution; LLM integration automates this entirely.

</details>

---

<details>
<summary><strong>B-EC9: Proactive AI Monitoring</strong> — 3 quotes</summary>

**Definition:** User wants AI to proactively surface interim survey performance data (response rates, benchmarks vs. historical surveys) without manual checking, enabling real-time answers to stakeholder queries.

---

**Quote 1** | `00:29:17–00:30:09` | Confidence: **strong**

> "Something that was more proactive and telling you that, you know, responses are coming in, giving you some sort of idea of if it's performing well or not, because I'll get — I'll start to get questions a few hours after we've sent the survey. How's it doing? I don't know what is it doing. I've got to craft an answer to that that makes sense and it's accurate."

*Rationale:* Describes the concrete pain — stakeholder queries arrive before user has checked results; proactive AI push would eliminate the lag and enable accurate real-time answers.

---

**Quote 2** | `00:31:22–00:32:23` | Confidence: **strong**

> "Being able to tell that data is flowing into your CRM... being able to help you respond to those queries before a survey is finished, like a simple question, how's this survey doing? So an external AI would have the context of how it's doing in relation to your other surveys that you ran to a similar audience. So it could say, hey, we're only 3 hours in, you've already got 100 responses, this is trending a lot better than the last survey you ran."

*Rationale:* Describes the ideal proactive monitoring output — not just raw count, but comparative context against historical surveys for the same audience.

---

**Quote 3** | `00:40:45–00:42:12` | Confidence: **moderate**

> "Hopefully, you know, proactively asking what it can do next. You know, would you like me to synthesize this data into report? Would you like me to create some PowerPoint slides?"

*Rationale:* Extends proactive behavior from monitoring to the reporting stage — AI should anticipate the next workflow step and offer to execute it without waiting to be prompted.

</details>

---

<details>
<summary><strong>B-EC10: Corporate Authorization Barrier</strong> — 1 quote</summary>

**Definition:** Organization has not yet authorized connecting AI systems to external platforms despite daily AI use — organizational approval is the missing piece for adopting LLM integration.

---

**Quote 1** | `00:04:24–00:04:47` | Confidence: **strong**

> "No. So that is something that we're actively pursuing, but we're still technically in a pilot stage with Claude, even though it's, we use it every day for everything. But we're not to the point where corporate has signed off on us connecting systems yet. So that's the piece that's missing."

*Rationale:* Frames organizational authorization — not technical capability — as the current blocker for concept 2. Usage is mature; approval is pending. "The piece that's missing" frames this as an imminent rather than distant barrier.

</details>

---

<details>
<summary><strong>B-EC11: Embedded AI Domain Specialization Value</strong> — 2 quotes</summary>

**Definition:** The unique value user attributes to embedded AI in a survey platform is deep specialization in survey methodology — an advantage over general-purpose external LLMs that are "pseudo-expert in everything."

---

**Quote 1** | `00:42:47–00:44:11` | Confidence: **moderate**

> "I don't think so, unless I find that your AI is so fine-tuned to survey analysis that it's giving better analysis than an external AI would... if I was getting something different, then maybe I would actually — if there were both options available, at least the first, maybe the first couple of times that I do something like this, I would be curious to see how each version of the AI handles that data analysis and make my own determination."

*Rationale:* Conditional framing — embedded AI returning to relevance only if its survey-specific fine-tuning produces measurably better analysis. User would empirically test both before deciding.

---

**Quote 2** | `00:56:18–00:57:16` | Confidence: **strong**

> "The only other value I see would be, you know, an AI that's really trained and tuned on, like, the art of survey creation versus any sort of AI platform which is pseudo-expert in sort of everything, but not specifically built around one core function like surveys."

*Rationale:* Clearest statement of embedded AI's potential differentiated value — domain specialization in survey creation vs. breadth-over-depth trade-off of general-purpose LLMs.

</details>

---

<details>
<summary><strong>B-EC12: Feature Completeness as Switching Criterion</strong> — 2 quotes</summary>

**Definition:** User's choice between embedded chat and LLM integration depends on whether the integration delivers a fully end-to-end experience; if it requires returning to the survey platform for any step, it loses its advantage.

---

**Quote 1** | `00:16:34–00:17:09` | Confidence: **strong**

> "To be honest, I don't have a strong preference. Um, it's just a matter of what Claude can deliver. Like, is it full-featured? Is it going to give me the link at the end that I need to embed in my email? If I don't need to go into SurveyMonkey, SurveyMonkey at all, to be honest. I prefer to just do it in Claude. Um, so yeah, there's nothing — there would be nothing particularly annoying with doing it in Claude unless I had to log into SurveyMonkey to finalize and launch anyways. Then I might as well just do it all there."

*Rationale:* Decision logic laid bare: if the integration handles everything end-to-end, prefer it; if it still requires SurveyMonkey for any step, the consolidation advantage disappears entirely.

---

**Quote 2** | `00:22:47–00:23:15` | Confidence: **strong**

> "I guess it would need to be full-featured enough that I didn't need to do part of it in Claude and log in and do part of it in SurveyMonkey. So as long as I could build, iterate, launch, analyze."

*Rationale:* Names the four lifecycle stages that must be covered for feature completeness: build, iterate, launch, analyze. Missing any one stage collapses the case for LLM integration.

</details>

---

<details>
<summary><strong>B-EC13: Historical Survey Performance as AI Context</strong> — 2 quotes</summary>

**Definition:** User wants AI to learn from past survey performance data (question phrasing, length, drop-off, audience-specific effectiveness) to proactively guide current and future survey design.

---

**Quote 1** | `00:49:41–00:50:05` | Confidence: **strong**

> "It should have historical data and context around what has worked for us specifically in the past, and not just suggest general best practices. It should look at okay, what resonated in past surveys? Let's try to recreate that in current and future surveys."

*Rationale:* Distinguishes company-specific historical performance from generic survey best practices — AI should apply learned patterns from this organization's own survey history, not general guidelines.

---

**Quote 2** | `00:50:35–00:52:52` | Confidence: **strong**

> "Questions, the way questions are phrased. I think more broadly, just survey length. So if it has enough data to understand, you know, when we go beyond 8 questions, we see significant drop-off — for it to know that and to guide us away from doing that, those sorts of decisions."

*Rationale:* Provides a concrete example of what historical performance context enables — org-specific drop-off threshold (8 questions) should inform AI recommendations, not generic UX research averages.

</details>

---

<details>
<summary><strong>B-EC14: Ideal State — End-to-End Survey Wizard</strong> — 1 quote</summary>

**Definition:** User envisions the ultimate solution as an AI wizard that handles the full survey lifecycle (build → execution → analysis → packaging) with contextual awareness of each stage's requirements.

---

**Quote 1** | `00:41:51–00:42:12` | Confidence: **strong**

> "What I'm envisioning is a sort of like survey process wizard that, that handles everything from the build to the execution to the analysis to the, to the packaging of the analysis as sort of like this, this little module or wizard that knows exactly what you need at every stage. Like that, that's like the blue sky sort of ideal future state."

*Rationale:* User's own framing — "survey process wizard" is in-vivo language describing an integrated, context-aware AI orchestrator. Named as "blue sky ideal" (aspirational, not near-term expectation).

</details>

---

## Unassigned Turns

| Timestamp | Text (condensed) | Reason not coded |
|-----------|-----------------|------------------|
| `00:01:12–00:02:24` | Background: director marketing ops, CRM admin, surveys (NPS, market research, intake forms). Latest survey: Q1 product feature/pricing interest survey | Background/intro — not about AI task allocation |
| `00:09:46–00:10:36` | Building stage: copy/adapt previous survey, create conditional logic, generate link, minimal design (logo only) | Standard survey platform operations; no AI involvement or task allocation discussed |
| `00:20:23–00:20:54` | Brainstorming tools: Word (document), Slack (real-time collaboration/wordsmithing, references to external docs) | Describes collaboration tool stack; does not address AI task allocation |
| `00:23:55–00:24:27` | Survey branding: just a logo, recently changed, minimal design investment | Branding logistics; no AI-relevant decision-making |
| `00:24:38–00:25:44` | Distribution: survey link → Salesforce marketing automation → adapt template → AI-assisted email content → A/B test subject lines → approval → 1–2 reminder sends | Distribution workflow; AI assistance in email content is incidental and not discussed in depth |
| `00:38:55–00:39:34` | After analysis: share via Slack (smaller surveys) or AI-assisted PowerPoint (larger surveys); review within marketing team; share with executive team | Reporting logistics; AI-assisted PowerPoint is mentioned but not elaborated as a task allocation decision |
| `00:51:33–00:53:00` | What to remember across surveys vs. per-survey: audience differences, brand tone, question length norms; single-survey specifics don't need to persist. No survey is in a vacuum where prior context wouldn't help | Elaboration of B-EC13 — not a new concept but continuation; kept here as note rather than double-coded |
