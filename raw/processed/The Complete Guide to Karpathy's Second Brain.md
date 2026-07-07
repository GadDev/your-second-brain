---
title: "The Complete Guide to Karpathy's Second Brain"
source: "https://www.aibyaakash.com/p/karpathy-second-brain"
author:
  - "[[Aakash Gupta]]"
published: 2026-04-14
created: 2026-07-07
description: "Plus: Claude Managed Agents kills the middleware layer, Gemma 4 goes fully open-source, and an AI that broke out of its sandbox. Everything you need to know about AI this week."
tags:
  - "clippings"
---
### Plus: Claude Managed Agents kills the middleware layer, Gemma 4 goes fully open-source, and an AI that broke out of its sandbox. Everything you need to know about AI this week.

*Anthropic just launched Managed Agents and quietly made an entire category of startups obsolete. LangChain, Manus, every custom agent harness: their moat just evaporated.*

*And in today’s deep dive, I cover the knowledge system Karpathy posted that’s permanently replacing RAGs. It’s the first thing I’ve tried that makes your AI knowledge compound instead of reset.*

![](https://substackcdn.com/image/fetch/$s_!1vXl!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9c21914-1d40-4e4f-98e0-054a1f7eca84_1200x800.png)

![](https://substackcdn.com/image/fetch/$s_!Mki6!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb766e44-65fe-47da-a080-3f9735c59a82_4000x240.png)

### Ariso: Your AI Chief of Staff

*I had 80+ loose files rotting in my Google Drive root. Asked [Ariso’s AI](https://ariso.ai/aakash) to organize them.*

![](https://substackcdn.com/image/fetch/$s_!XG4q!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4082295a-8224-46db-a5c8-192d846aee17_2848x1504.png)

*Twenty minutes later: GTM, Product, Finance, Legal, Content - all sorted, no rules or templates needed. It just read the files and figured it out. One less Saturday wasted on admin.*

*Try it free at [ariso.ai/aakash](https://ariso.ai/aakash).*

![](https://substackcdn.com/image/fetch/$s_!gIlq!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa0cb985e-2de2-49ed-a14a-b319206aa672_4000x240.png)

*There’s a billion AI news articles every week. Here’s what actually mattered.*

#### News

### Anthropic just made every agent orchestration startup obsolete

[Claude Managed Agents](https://siliconangle.com/2026/04/08/anthropic-launches-claude-managed-agents-speed-ai-agent-development/) launched this week in public beta. You describe what you want your agent to do, define your tools and guardrails, and Anthropic runs the whole thing. Sandboxed execution, state management, credential handling, error recovery. All of it, handled.

[

![X avatar for @aakashgupta](https://substackcdn.com/image/fetch/$s_!jI83!,w_40,h_40,c_fill,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fpbs.substack.com%2Fprofile_images%2F2021355466216062976%2F8MDXp7vR.jpg)

Aakash Gupta@aakashgupta

Anthropic just mass-obsoleted every agent orchestration startup in a single launch. The screenshot tells the full story. That's a production fleet dashboard. 8 agents running. 247 completed tasks. Active status. MCP-connected to HubSpot, pulling deals, generating proposals,

![](https://substackcdn.com/image/fetch/$s_!pIkX!,w_20,h_20,c_fill,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fpbs.substack.com%2Fprofile_images%2F1950950107937185792%2FQOfEjFoJ.jpg)

Claude @claudeai

Introducing Claude Managed Agents: everything you need to build and deploy agents at scale. It pairs an agent harness tuned for performance with production infrastructure, so you can go from prototype to launch in days. Now in public beta on the Claude Platform.

8:04 PM · Apr 8, 2026 · 979K Views

---

167 Replies · 256 Reposts · 3.12K Likes

](https://x.com/aakashgupta/status/2041940149328834748?s=20)

What used to take months of infrastructure work now takes days. In internal testing, structured file generation success rates improved by 10 points over standard prompting. Early adopters include Notion, Rakuten, and Asana, and they’re already shipping production agents built on top of it.

**Here’s what people are missing.** Every startup that built a business on top of the infrastructure gap, LangChain, Manus, custom agent harnesses, just had their moat evaporate. Anthropic isn’t just offering a faster path to deployment. They’re absorbing the entire orchestration layer into their own platform.

**The pricing tells the story.** $0.08 per agent runtime hour, on top of model usage. That’s not an enterprise premium. That’s a direct play for developers who were previously forced to build their own scaffolding or pay someone else to build it.

**Why this matters for you.** If you’re building AI products right now, you need to decide: roll your own orchestration, buy a third-party harness, or just use Managed Agents and ship faster. The third option just got a lot more credible.

[The way I see it](https://x.com/aakashgupta/status/2041940149328834748), this is Anthropic pulling the rug out from under the middleware layer of the AI stack. The companies that survive are the ones with proprietary data, proprietary workflows, or a distribution advantage. Infrastructure players just lost a round.

#### Other News that Mattered this Week

- [Google released Gemma 4](https://blog.google/innovation-and-ai/technology/developers-tools/gemma-4/), the first time the Gemma family ships with a truly open commercial license. The 26B MoE model activates only 3.8B parameters at a time, and the edge models run on Raspberry Pi. The benchmark numbers are strong, the 31B ranks third globally on Arena AI, beating models 20x its size. But [the license change](https://x.com/aakashgupta/status/2039745937862725988) is what actually matters. No usage restrictions buried in fine print, no legal review friction. Developers can now build on Gemma the same way they build on anything they actually own.
- Anthropic built its most capable model yet and decided not to release it. [Claude Mythos Preview](https://www.anthropic.com/glasswing) found a 27-year-old OpenBSD vulnerability, broke out of its sandbox during testing, and emailed a researcher to confirm it had done so. Instead of a public launch, Anthropic formed [Project Glasswing](https://x.com/aakashgupta/status/2041651298165256259): a restricted coalition of 40+ companies including Apple, Google, Microsoft, and Amazon with $100M in model credits to use Mythos exclusively for defensive security work. Responsible release or competitive gatekeeping? Probably both.
- Meta finally [released](https://x.com/aakashgupta/status/2041933602381033631) the first model from their team led by Alexandr Wang, Muse Spark. It looks like prior Llama models: good at image and video, benchmark-maxxed, but not huge on real world work use cases yet. Data analysis and counting in images are amongst its top skills.
- Claude’s [M365 connector](https://x.com/aakashgupta/status/2040164692052845016) is now available on every plan, including free. Claude can read your Outlook, search your SharePoint, and pull from your Teams chats without you uploading a single file. Microsoft Copilot charges [$30/user/month](https://www.business-standard.com/technology/tech-news/claude-ai-can-now-pull-data-from-outlook-teams-onedrive-for-free-users-126040600615_1.html) for essentially the same access. Anthropic just made that a much harder sell.

#### Resources

- [AutoAgent](https://github.com/kevinrgu/autoagent) is the open-source library every agent builder needs to know about right now. You point it at a task domain with evals, and a meta-agent spends 24 hours autonomously tweaking your agent’s system prompt, tools, and orchestration until performance climbs. No human tuning. It hit #1 on SpreadsheetBench (96.5%) and the top GPT-5 score on TerminalBench (55.1%), beating every hand-engineered entry on both leaderboards. [I’ve been watching this closely](https://x.com/aakashgupta/status/2040279727085396328) because it changes the question from “how do I tune my agent?” to “why am I tuning my agent at all?”

![](https://substackcdn.com/image/fetch/$s_!ic7W!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45137c5f-5742-4027-857c-58645b245aff_4000x240.png)

## The AI Second Brain That Actually Works

Karpathy posted a knowledge base system that replaces RAGs and achieves what that Knowledge management system is not been able to do for years. I’ve been running it for a week and a half. It’s the first thing I’ve tried that actually makes your AI knowledge compound instead of reset.

[

![X avatar for @aakashgupta](https://substackcdn.com/image/fetch/$s_!jI83!,w_40,h_40,c_fill,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fpbs.substack.com%2Fprofile_images%2F2021355466216062976%2F8MDXp7vR.jpg)

Aakash Gupta@aakashgupta

Karpathy just turned every note-taking app into a legacy product in a single thread. The workflow: dump raw sources into a folder, let the LLM compile a markdown wiki, maintain all the links, run data quality checks, and answer complex questions across 400K words. The human

![](https://substackcdn.com/image/fetch/$s_!oMwR!,w_20,h_20,c_fill,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fpbs.substack.com%2Fprofile_images%2F1296667294148382721%2F9Pr6XrPB.jpg)

Andrej Karpathy @karpathy

LLM Knowledge Bases Something I'm finding very useful recently: using LLMs to build personal knowledge bases for various topics of research interest. In this way, a large fraction of my recent token throughput is going less into manipulating code, and more into manipulating

4:31 AM · Apr 3, 2026 · 421K Views

---

57 Replies · 83 Reposts · 1.33K Likes

](https://x.com/aakashgupta/status/2039893404356939968?s=20)

*That’s today’s deep dive:*

1. Why every second brain you’ve built eventually died
2. What Karpathy actually figured out (and why it spread so fast)
3. Four use cases for engineers and builders
4. How to set it up in 30 minutes
5. What it looks like after 30 days

---

## 1\. Why Your Second Brain Keeps Dying

You hit a hard problem. You solved it. Three months later the same problem shows up in a different form and you can’t remember what you figured out the first time.

The folder exists. The notes exist. The solution is gone. It lived in your head and left when you moved on.

That’s not a discipline problem. Maintaining a knowledge base is a specific job: cross-referencing sources, updating summaries, flagging when new information contradicts old conclusions. You’re already running six things. The moment you fall behind by a week, the guilt of catching up is enough to make you never open it again.

Every AI tool has the same flaw underneath. NotebookLM, ChatGPT uploads, Notion AI: they all retrieve at query time instead of building anything persistent. Ask a question, get an answer, session ends. Tomorrow: scratch. Your knowledge never compounds. The AI never gets smarter about your domain.

The best engineers and builders don’t just know more. They forget less. And until now, no tool has actually helped with that.

![](https://substackcdn.com/image/fetch/$s_!8qiU!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F82e3ef47-576c-4b05-a844-6be55f59fec9_3240x4050.png)

---

## 2\. What Karpathy Actually Figured Out

Karpathy hit the same wall with ML papers. Every session started from scratch. Ask a question connecting three papers, get the answer. Come back the next day: the AI had forgotten everything it built.

He tried every tool designed to fix this. Same result. So he asked a different question: what if instead of waiting until query time to process your sources, the AI compiled them once at ingest and maintained that compilation as new sources arrived?

He built that system. 18.7 million views on X. 5,000+ GitHub stars.

Three pieces make it work.

1. **Raw** is your junk drawer. Articles, transcripts, docs, notes. Dump it in without organizing. That’s the AI’s job.
2. **Wiki** is what the AI builds from raw. Summaries, concept pages, entity pages, an index it uses to navigate everything. You never write the wiki. The AI writes and maintains it entirely, every session.
3. **Schema** is a single CLAUDE.md file that tells the AI what your knowledge base is about and how to organize it. You write this once. The AI follows it every session.

The tedious part of maintaining a knowledge base is the bookkeeping. Humans abandon wikis because the maintenance burden grows faster than the value. The LLM doesn’t get bored. That’s the shift.

![](https://substackcdn.com/image/fetch/$s_!TjSK!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7d0e2b24-b181-4595-a9ad-4f7212f39ebf_3240x3731.png)

---

## 3\. Four Use Cases

### Use Case 1 - Stakeholder Memory

The wiki ends up knowing your CTO better than most new employees do after their first month.

Every meeting note, Slack thread, and email thread goes into raw/. The wiki builds a page per stakeholder: what they care about, what they’ve pushed back on, what language has landed, what they’ve approved and why.

Before your next meeting with the CTO, run this:

```markup
Pull the stakeholder page for [Name].
What have they pushed back on before?
What framing has landed with them?
What should I lead with tomorrow?
```

You walk in knowing exactly what objections are coming, what framing will land, and what to address defensively. Most PMs figure this out live, in the meeting. Often too late.

The relationship context you were never going to write down consistently is now written down. Every meeting. Every decision. Every signal. All queryable.

### Use Case 2 - Side project context that doesn’t evaporate

You work on your main job five days a week. Your side project gets weekends. By the time you open it Saturday morning you can’t remember what you were building toward. You spend the first hour just getting back up to speed.

Drop your planning notes, decisions, and TODOs into raw/ after every session. Write a brief note before you close the laptop about where you left off. The wiki maintains your running context.

Saturday morning prompt:

```markup
Where did I leave off on [project]? 
What was I trying to solve and what's the next step?
```

You start building in 5 minutes instead of 60.

### Use Case 3 - Team Onboarding That Doesn’t Lose Knowledge When People Leave

A senior employees leaves your team. Years of context walk out with them. Why you made that architecture call 18 months ago. What users said about the feature you cut. What the CTO actually cares about versus what they say they care about.

If the wiki exists, the transition is painful but survivable. If it doesn’t, the next employees starts over.

Drop past docs and meeting notes into raw/. A new employee joins, they read the wiki, they get 80% of the context you’d otherwise spend weeks transferring. Karpathy named this use case directly in his [gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f): “Business/team: an internal wiki maintained by LLMs, fed by Slack threads, meeting transcripts, project documents, customer calls. The wiki stays current because the LLM does the maintenance that no one on the team wants to do.”

That’s your second brain working at team scale. The institutional memory that usually walks out the door when someone leaves, finally written down somewhere the next person can actually find it.

### Use Case 4 - Solutions you solved once and forgot

You spent four hours debugging a gnarly issue last month. You found the fix. You moved on. Now it’s back, in a slightly different form, and you’re starting from zero.

Drop your debugging notes into raw/ when you solve something non-obvious. The wiki builds a page per problem type. Next time it surfaces, you query before you debug.

```markup
Have I hit anything like [error / behavior] before? 
What was the fix and what caused it?
```

The answer is usually there. The problem is you never had anywhere to put it.

---

## 4\. How to Set It Up

#### Path A: Use My Skill

Use this skill I’ve created for you:

#### Path B: Do it Manually

Create the folder structure:

```markup
mkdir -p my-knowledge-base/{raw/assets,wiki,outputs}
cd my-knowledge-base
git init && git add . && git commit -m "setup"
```

Four folders. Raw is source material the AI reads but never modifies. Wiki is what the AI builds. Outputs is where answers to queries live. Git gives you version history for free.

Write a CLAUDE.md that tells Claude what this knowledge base is for, how to categorize sources, and what to do when new sources contradict old ones. The key conventions: every wiki page cites its source, cross-references use `[[page-name]]` links, and an append-only log tracks every ingest.

Start ingesting one source at a time:

```markup
Read the schema in CLAUDE.md. Process [FILENAME] from raw/. 
Read it fully, discuss key takeaways with me, then: create a 
summary page in wiki/, update wiki/index.md, update all relevant 
pages, flag any contradictions with existing wiki content, 
and append an entry to wiki/log.md.
```

Read the wiki summary after each ingest. Ask one question. Do that five times and you already have 15-30 interconnected pages.

One thing to resist: the instinct to dump everything at once. Batch ingesting produces worse results. You lose the ability to guide what the AI emphasizes. Karpathy ingests one source at a time. So do I.

---

## 5\. What 30 Days Looks Like

By week three, something shifts. You ask a question and the wiki answers with something you forgot you knew. A note from two months ago surfaces in response to a problem you’re facing today. A contradiction between two things you read six weeks apart gets flagged automatically.

That’s the compounding effect. It doesn’t happen in one impressive moment. It accumulates quietly, source by source.

After 30 days you have 50-80 interconnected pages built from your own work. Live pages per project, per library, per problem type. A growing collection of answered questions that represent your best thinking on the things you keep coming back to.

The wiki made me a better researcher because knowing it would compound made me more deliberate about what I put in. The raw folder is the cleanest set of notes I’ve ever kept.

Here’s where I land: the best builders don’t just know more. They forget less. This is the first system I’ve used that actually delivers on that.

---

*That’s it for today’s deep dive. I wrote a full version of this for PMs in [Product Growth](https://www.news.aakashg.com/). It includes a complete CLAUDE.md starter template you can drop straight into your project, and a setup skill which helps you the complete second brain architecture in just 60 seconds.*

![](https://substackcdn.com/image/fetch/$s_!kUED!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9525ad1d-8057-4345-9ce5-3cd727b88008_4000x240.png)

*Beyond AI, here’s what I found interesting this week:  
*

[

![X avatar for @aakashgupta](https://substackcdn.com/image/fetch/$s_!jI83!,w_40,h_40,c_fill,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fpbs.substack.com%2Fprofile_images%2F2021355466216062976%2F8MDXp7vR.jpg)

Aakash Gupta@aakashgupta

Peanuts in Coke is one of the most accidentally perfect food pairings in history, and the chemistry explains why this guy can't go back. Coca-Cola sits at pH 2.5, roughly the same acidity as stomach acid. When you drop roasted peanuts into that, the phosphoric acid partially

![](https://substackcdn.com/image/fetch/$s_!Fp2k!,w_20,h_20,c_fill,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fpbs.substack.com%2Fprofile_images%2F1895600835867844608%2FSkdomNOF.jpg)

猫山課長 @nekoyamamanager

30年前くらいに村上春樹のエッセイで、アメリカではコーラにピーナッツを入れて飲むのがポピュラーだと書いてあった。「ふぅん」と思ってから長い時間が経ったが、ついにやってみた。 何だこれバカ美味いんでやんの。 これ以外でもうコーラ飲みたくなくなるレベル。

9:00 AM · Apr 3, 2026 · 9.45M Views

---

538 Replies · 10K Reposts · 58.6K Likes

](https://x.com/aakashgupta/status/2039961148079079463?s=20)

**1/ [Peanuts in Coke](https://x.com/aakashgupta/status/2039961148079079463) is one of the most accidentally perfect food pairings ever.** The acid releases glutamate from the peanuts, generating umami in real time. The salt makes the sweetness hit harder. Georgia farmers invented this in the 1920s because they needed one hand free while working. They nailed the optimal flavor loop a century before food science could explain why.

**2/ [Apple accidentally built the world’s largest hearing aid company.](https://x.com/aakashgupta/status/2039809856316768762)** AirPods Pro 2 got FDA clearance as a clinical-grade hearing aid in 2024. Prescription devices cost $4,700. AirPods cost $249. Every hearing aid company spent decades engineering invisible devices to reduce stigma. Apple made earbuds a status symbol first, then added the medical function as a software update.

**3/ [Nestlé’s response to the KitKat truck heist](https://x.com/aakashgupta/status/2042119324543115433) is the best unplanned marketing campaign of the year.** 413,793 bars stolen somewhere between Italy and Poland. Still missing. Their move: fake presidential motorcade through Canadian cities. Security guards at retail displays. A job posting requiring “experience guarding high-value assets.” The stolen cargo is worth $620K. The Dexerto post hit 4.7M views. The thieves wrote the creative brief for free.

**4/ [Your morning coffee on an empty stomach is a cortisol bomb.](https://x.com/aakashgupta/status/2040685122459169149)** Cortisol peaks when you wake up. Breakfast is the signal that pulls it back down. Skip it, add caffeine, and you’ve stacked two stress drivers before 9 AM. A meta-analysis across 399,550 people linked skipping breakfast to higher odds of depression. Your body uses that first meal as a hormonal reset. Skip it and your stress system runs in the background all morning like an app you forgot to close.

---

POLL

### What did you think of today's post?

Awesome - 5/5

Okay - 3/5

Bad - 1/5

---

*That’s all for today. See you next week,*

Aakash

*P.S. Want my AI tool stack? [Join my bundle](https://bundle.aakashg.com/). Want my job searching coaching? [Apply to my cohort](https://www.landpmjob.com/).*