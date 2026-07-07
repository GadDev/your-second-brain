---
title: "I built this for myself. Then 1,374 strangers cloned it."
source: "https://theaioperator.io/p/i-built-this-for-myself-then-1374"
author:
  - "[[Eugeniu Ghelbur]]"
published: 2026-05-10
created: 2026-07-07
description: "I built a free Claude + Obsidian skill for myself; 1,374 people cloned it in weeks. The origin story of obsidian-second-brain and why it spread."
tags:
  - "clippings"
---
### Two tools you already use don't talk to each other. Here's what happens when you make them.

![](https://substackcdn.com/image/fetch/$s_!_mp_!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1eb2de45-6bad-4c5f-b549-4b2416c2b60f_1048x697.png)

> **What is obsidian-second-brain?** A free, open-source Claude Code skill that gives Claude persistent memory through your Obsidian vault. 1,024 stars in seven weeks. MIT licensed. Built by Eugeniu Ghelbur. Repo: [github.com/eugeniughelbur/obsidian-second-brain](https://github.com/eugeniughelbur/obsidian-second-brain).

You use Claude every day. Every session starts from scratch. You re-explain everything. The conversation ends. Everything disappears.

You take notes in Obsidian. Hundreds of files. They just sit there. You make the same decision twice because you forgot you made it six months ago.

Two powerful tools. Completely disconnected.

That was my problem. I was tired of it. So I built the bridge.

Then I open-sourced it on GitHub. Seven weeks later, 1,374 strangers had cloned it.

This post is what I built, why people are using it, and what it might mean for you if you bring AI into your work.

## What obsidian-second-brain does

obsidian-second-brain is a free Claude Code skill. Open source. MIT license. The repo is called `obsidian-second-brain`.

Under the hood it’s 31 commands across four layers. But you don’t need to know all 31. You only need to know what each layer DOES:

1. **Claude remembers.** Every meeting, every decision, every voice memo, every screenshot. It gets saved to the right place in your vault automatically. You stop losing things.
2. **Claude thinks with you.** Your vault argues back. Before you decide something, you can ask “have I been here before?” and it shows you your past failures and reversed decisions on the same topic.
3. **Claude knows you.** Your identity, your projects, your current state. Loaded in ten seconds. Every session picks up where the last one ended.
4. **Claude pulls knowledge in.** X posts, web research, YouTube transcripts. They go into your vault, not just into a temporary chat that disappears.

Plus four scheduled agents that run while you sleep. The vault gets smarter without you.

You don’t even have to open Obsidian to use it. Everything happens through Claude.

![The 4 layers of obsidian-second-brain.](https://substackcdn.com/image/fetch/$s_!T5MA!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8904c85a-dc30-4f48-9b01-4b867bcd3100_2220x1494.png)

The 4 layers of obsidian-second-brain.

---

## What it actually does

Some real moments where it changes how you work:

- **After a meeting**, one command saves every decision, person, task, and idea to the right note. You do nothing.
- **You record a voice memo on your phone.** Drop it in. It gets transcribed, the action items get extracted, the right people and projects get linked.
- **You take a photo of a whiteboard.** Same thing. The image becomes searchable knowledge.
- **You find a great YouTube video.** It doesn’t get summarized into one new note. It REWRITES your existing pages. People get updated. Contradictions get resolved. Patterns trigger new synthesis pages.
- **Before a big decision**, the vault searches your past notes for the same topic and pushes back with your own words. Your vault holds you accountable.
- **You go to sleep**, and a nightly agent runs five phases: closes the day, reconciles contradictions, finds patterns across sources, heals orphan notes, rebuilds the index. You wake up to a smarter vault.

That’s the difference between a notes app and a second brain. The notes app waits for you. The second brain works for you.

## The proof

Here are the numbers, fresh from the GitHub Insights page today:

- **Created seven weeks ago.** 2026-03-24.
- **1,024 stars.**
- **99 forks.**
- **1,374 unique people cloned the repo in the last two weeks alone.** That’s not vanity. Cloning means they actually pulled the code down to try it.
- **5,910 unique visitors to the repo in 14 days.**
- The top referrer is Twitter, by a wide margin. The second is Google. People are searching for this and finding it.

![GitHub stars growth on obsidian-second-brain, March through May 2026.](https://substackcdn.com/image/fetch/$s_!hOoR!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa4682263-36db-4c86-bc9c-2bf9246f7f82_2220x1484.png)

GitHub stars growth on obsidian-second-brain, March through May 2026.

The first public user feedback came in a LinkedIn DM from a Cybersecurity Leader. He said he was “personally impressed by the correlation engine within one hour” of migrating his own data into the vault.

The first external code contribution came from someone I had never met. He shipped 695 lines of code to add a new `/podcast` command. He found a real bug in my code while doing it. The project isn’t just mine anymore.

The Substack readers who actually click through to the repo convert at 24 percent. Meaning the people who read about it stay.

---

## Why this matters if you’re a founder

Your team uses AI. Your team takes notes. The two don’t talk.

You hire someone in March. They have great calls with three customers in their first week. The notes go into a tool. The Claude conversations go nowhere. By June, that person has switched roles or left. The customer insight is gone.

Multiply that by fifty people on your team and you have institutional amnesia at scale. Your company knows things, but your company can’t remember them.

This open-source skill is how I solved that problem for one person. Me. The principles are the same at any size. The code is free to fork.

If you bring AI into your team in the next six months, your team is going to hit this exact wall. The fix isn’t a new SaaS subscription. It’s a pattern. The pattern is in the repo.

![Institutional amnesia: your team's customer insight dies the day someone leaves.](https://substackcdn.com/image/fetch/$s_!O5O9!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F00c517a4-d80a-4027-9a59-cf28a142c335_2234x1474.png)

Institutional amnesia: your team's customer insight dies the day someone leaves.

## Try it

GitHub repo: [github.com/eugeniughelbur/obsidian-second-brain](https://github.com/eugeniughelbur/obsidian-second-brain)

It’s free. MIT license. One command to install.

If you don’t use Obsidian or Claude Code yet, the README explains both. If you do, you can be running it in five minutes.

---

## Frequently asked questions

**What is obsidian-second-brain?**  
A free, open-source Claude Code skill that connects Claude to an Obsidian vault. Every conversation, decision, meeting note, voice memo, and research finding gets saved to the right place automatically. The vault then feeds context back into every future Claude session.

**Is it free?**  
Yes. MIT license. Free to use, fork, or extend. There is no paid tier.

**Who built it?**  
Eugeniu Ghelbur, AI Automation Engineer at Single Grain. The repo went public on 2026-03-24. As of 2026-05-10 it has 1,024 stars, 99 forks, and 1,374 clones in the prior 14 days.

**Do I need to know how to code?**  
No. One command installs it. The README walks you through Claude Code and Obsidian setup from scratch.

**Does it require Claude Code?**  
Yes. It is a Claude Code skill, not a standalone app. Claude Code is free at claude.com/claude-code.

**Does it require Obsidian?**  
Yes. Obsidian is free for personal use. The skill assumes a markdown vault on local disk.

**How is this different from Obsidian AI plugins like Smart Connections?**  
Most plugins call an AI API from inside Obsidian. obsidian-second-brain inverts that. Claude is the operator. The vault is its memory. You can go weeks without opening Obsidian. The vault gets smarter while you work somewhere else.

**Where is the repo?**  
[github.com/eugeniughelbur/obsidian-second-brain](https://github.com/eugeniughelbur/obsidian-second-brain)

---

## What’s next

This is week one of **The AI Operator**, my publication for people building with AI in production.

One post per Tuesday. Three things I write about:

- **Obsidian + AI workflows** (how to make your second brain actually intelligent, like this post)
- **AI agent patterns** (what works, what breaks, what I’m shipping)
- **AI for humans** (how to bring AI into your team or your life without scaring people)

If you’re bringing AI into your work and you want to see what’s actually working in production from someone who ships it, subscribe. There’s a button somewhere obvious on this page.

Thanks for being here. I write for the people who build.

Eugeniu