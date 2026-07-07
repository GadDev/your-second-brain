---
title: "Build an AI Second Brain(LLM Wiki Pattern) With Claude Code and Obsidian"
source: "https://medium.com/@tahirbalarabe2/build-an-ai-second-brain-llm-wiki-pattern-with-claude-code-and-obsidian-fc41cc213d50"
author:
  - "[[Tahir]]"
published: 2026-06-01
created: 2026-07-07
description: "TLDR:Build an AI-powered knowledge base in Obsidian. Use Claude Code slash commands to ingest, link, and query your notes into a smart secon"
tags:
  - "clippings"
---
![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*tq4C-CsXWLIuwmiq7BMkJg.png)

**TLDR:**Build an AI-powered knowledge base in Obsidian. Use Claude Code slash commands to ingest, link, and query your notes into a smart second brain.

### READ THIS FIRST

[What is LLM Wiki Pattern? Persistent Knowledge with LLM Wikis](https://medium.com/@tahirbalarabe2/what-is-llm-wiki-pattern-persistent-knowledge-with-llm-wikis-3227f561abc1)

[What is Obsidian?The free and flexible app for your private thoughts.](https://medium.com/@tahirbalarabe2/what-is-obsidian-the-free-and-flexible-app-for-your-private-thoughts-683f53442222)

GITHUB:

## [GitHub - balarabetahir/Build-an-AI-Second-Brain-LLM-Wiki-Pattern-With-Claude-Code-and-Obsidian…](https://github.com/balarabetahir/Build-an-AI-Second-Brain-LLM-Wiki-Pattern-With-Claude-Code-and-Obsidian?source=post_page-----fc41cc213d50---------------------------------------)

### Build an AI-powered knowledge base in Obsidian. Use Claude Code slash commands to ingest, link, and query your notes…

github.com

You hear people talk about having a second brain. The usual version is just a glorified filing cabinet. You dump things in. You search for them later. That’s not a second brain. That’s a hard drive with opinions.

A real second brain needs two parts:

- The part that collects
- The part that thinks

Most people stop at the collection part. I used to be one of them. I had folders and tags and elaborate color coding systems. I spent hours organizing. Then I never looked at any of it again. Because organizing isn’t thinking. Organizing is just rearranging.

### The Rule That Changed How I Work

I recently built the other half for myself. I used Obsidian for notes and Claude Code as an automated wiki maintainer. The interesting thing wasn’t the tools. The interesting thing was the rule I decided to follow.

Raw separate from wiki.

Raw is where everything goes when it first arrives. Web clippings. Chat logs. Export files from other apps. Messy. Unstructured. Untouched.

I never change anything in raw. Ever. I call this the load bearing rule. Break it and the whole thing collapses.

Wiki is where Claude Code compiles knowledge. It does three things for me:

- Reads everything in raw
- Connects ideas across my notes
- Creates index pages automatically

And it never writes back to raw. I made sure of that. The separation is absolute.

### Why I Keep Things Separate

This matters more than it sounds. When I preserve the original source material, I preserve the ability to reconsider. What seems important today might seem less important tomorrow. But if I summarized and tagged and filed everything immediately, I would have baked in my first interpretation. I couldn’t go back to the raw material because I would have destroyed it in the act of organizing.

The raw folder is my memory. The wiki folder is my understanding. They need each other, but I don’t let them touch.

### How I Talk to My Second Brain

I use slash commands to talk to Claude Code. Each command is just a text file with instructions.

```rb
┌─────────────────────────────────────────────────────────────────────────┐
│                         MY SLASH COMMANDS                                │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│   ┌─────────────┐                                                       │
│   │  /ingest    │                                                       │
│   └──────┬──────┘                                                       │
│          │                                                              │
│          ▼                                                              │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │  Processes new material from raw folder into wiki folder        │   │
│   │                                                                 │   │
│   │  raw/ ──────────────────────────────────────────► wiki/         │   │
│   │  [messy unstructured files]      [compiled linked pages]        │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│   ┌─────────────┐                                                       │
│   │  /query     │                                                       │
│   └──────┬──────┘                                                       │
│          │                                                              │
│          ▼                                                              │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │  Answers questions and shows me citations                       │   │
│   │                                                                 │   │
│   │  "What did I say about X?" ─────► "Here is the answer from      │   │
│   │                                   raw/conv_12.md line 34"       │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│   ┌─────────────┐                                                       │
│   │   /log      │                                                       │
│   └──────┬──────┘                                                       │
│          │                                                              │
│          ▼                                                              │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │  Captures my thoughts and ideas                                 │   │
│   │                                                                 │   │
│   │  Random thought ──────────────────────────► daily log entry     │   │
│   │  "I should automate the ingest process"    with timestamp       │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│   ┌─────────────┐                                                       │
│   │  /lint      │                                                       │
│   └──────┬──────┘                                                       │
│          │                                                              │
│          ▼                                                              │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │  Checks for broken links and issues                             │   │
│   │                                                                 │   │
│   │  wiki/ ─────────────────────────────────────► Report:          │   │
│   │  [all pages]                                 "3 bad dates"      │   │
│   │                                            "17 broken links"    │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

Claude Code reads the file and does what it says. Simple enough that I understood it immediately. Powerful enough that I couldn’t have built it alone.

## What Actually Happened

Here’s what struck me about the scale of this. I converted 42 conversations from [Claude.ai](https://claude.ai/) from JSON to markdown. Claude Code created 42 files, each with proper YAML front matter:

yaml

```rb
source: claude-ai
date: 2024-01-15
topic: ai-agents
```

Then I ran /ingest. In one command, Claude Code turned those raw files into wiki pages with links and tags and connections. Minutes of work instead of days.

### What Claude Code Actually Does

But here’s what’s easy to miss. Claude Code didn’t understand my material. Not really. It just followed the rules I gave it:

- Look for entities in my notes
- Create pages for them
- Link related concepts together

The understanding still has to come from me. Claude Code just builds the scaffolding. I still have to climb it.

This is the opposite of what most people think AI will do for them. They think AI will do the thinking and leave the grunt work to humans. But that’s backwards. AI is great at grunt work. Reading 42 files and extracting entities. Formatting markdown. Checking for broken links. That’s the stuff I hate doing.

The thinking part? The judgment about what matters and what doesn’t? That’s still mine.

## What My Wiki Looks Like

The wiki pages Claude Code creates are sparse. I opened a page about mobility and it showed me six related concepts from my own notes:

- \[\[threat-modelling\]\]
- \[\[maestro-framework\]\]
- \[\[ai-agent-governance\]\]
- \[\[securing-ai-agents-data-governance\]\]
- \[\[risen-framework\]\]
- \[\[ics-security\]\]

Each one is just a name and a link. No explanation. No summary. No judgment. That’s intentional. The wiki isn’t supposed to replace my thinking. It’s supposed to make my thinking easier by showing me what I already have and how it connects.

### Asking Questions With Proof

When I run /query, Claude Code searches my wiki and returns passages with citations. It tells me where each fact came from:

- Which raw file
- Which line
- What the original source was

==This is the test of a good second brain. Not whether it remembers things, but whether it can prove what it remembers. I need to trust where my information came from.==

### Cleaning Up My Mess

I ran /lint and it found 17 broken links. Claude Code could fix the trivial ones automatically. But the broken links needed a decision from me. Should source citations use wiki links or plain text? That’s not a technical question. That’s my judgment call.

## Get Tahir’s stories in your inbox

Join Medium for free to get updates from this writer.

Claude Code flagged the problem. I made the choice.

### Capturing Random Thoughts

I used /log to capture a thought about nothing. No entities matched. No wiki pages touched. That’s fine. Sometimes a thought is just a thought. The system doesn’t need to capture everything. It just needs to capture what matters. And I only know what matters after I’ve thought about it.

### Why My Old Systems Failed

Most attempts at personal knowledge management fail because they try to do too much. They want to:

- Capture everything
- Organize everything
- Connect everything

I know because I tried them all. A system that does everything does nothing well. The raw/wiki separation forced me into minimalism.

```rb
┌─────────────────────────────────────────────────────────────────────────┐
│                         MY VAULT ARCHITECTURE                            │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│                      ┌─────────────────────────┐                        │
│                      │     OBSIDIAN VAULT       │                        │
│                      └───────────┬─────────────┘                        │
│                                  │                                      │
│              ┌───────────────────┴───────────────────┐                 │
│              │                                       │                 │
│              ▼                                       ▼                 │
│   ┌──────────────────────┐               ┌──────────────────────┐       │
│   │       RAW FOLDER      │               │      WIKI FOLDER      │       │
│   ├──────────────────────┤               ├──────────────────────┤       │
│   │                      │               │                      │       │
│   │  What I put there:   │               │  What I put there:   │       │
│   │                      │               │                      │       │
│   │  • Web clippings     │               │  • Index pages       │       │
│   │  • Chat logs (JSON)  │               │  • Entity pages      │       │
│   │  • App exports       │               │  • Linked concepts   │       │
│   │  • Raw notes         │               │  • Graph view nodes  │       │
│   │                      │               │                      │       │
│   ├──────────────────────┤               ├──────────────────────┤       │
│   │                      │               │                      │       │
│   │  My rule:            │               │  My rule:            │       │
│   │                      │               │                      │       │
│   │  NEVER MODIFY        │               │  NEVER OVERWRITE     │       │
│   │                      │               │  RAW                 │       │
│   │                      │               │                      │       │
│   └──────────────────────┘               └──────────────────────┘       │
│              │                                       │                  │
│              │                                       │                  │
│              └───────────────────┬───────────────────┘                  │
│                                  │                                      │
│                                  ▼                                      │
│                    ┌─────────────────────────┐                          │
│                    │    THEY NEVER TOUCH      │                          │
│                    └─────────────────────────┘                          │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

Raw gets everything. Wiki gets only what survives the ingest process. Everything else stays in raw, untouched, available if I need it, invisible if I don’t.

### It Felt Backward At First

This was the opposite of my usual approach. My usual approach was to decide what matters up front. Tag it. File it. Move on.

The raw/wiki approach forced me to decide what matters after seeing everything. Let Claude Code do the mechanical work of connecting. Then I do the human work of deciding.

I didn’t like it at first. It felt wrong to leave things messy. But I tried it anyway.

### What It Cost Me

I estimated this project would take 60 minutes. It took longer. It always does. But the time wasn’t spent organizing. It was spent setting up rules:

1. Install Obsidian and Claude Code
2. Scaffold the raw/ and wiki/ folders
3. Write the CLAUDE.md schema
4. Define the slash commands

The actual organization happens automatically after that. I run /ingest when I want. Once a day. Once a week. Whenever I have new material.

### What I Learned

This is how I built a second brain that actually works. I didn’t build it all at once. I built a pipeline:

1. Stuff goes in raw
2. Claude Code processes it
3. I review what comes out

Claude Code doesn’t replace me. It just does the parts I don’t want to do.

The hardest part wasn’t the technology. The hardest part was accepting that I don’t know what matters until I see it connected to everything else. I have to collect first and organize second. Raw first. Wiki second.

Most people won’t do this because it feels backward. I almost didn’t either. But organizing as you collect means you’re organizing before you understand. And organizing before you understand is just making a mess in slow motion. I know because I made that mess for years.

Now I have something that actually works.

GITHUB:

## [GitHub - balarabetahir/Build-an-AI-Second-Brain-LLM-Wiki-Pattern-With-Claude-Code-and-Obsidian…](https://github.com/balarabetahir/Build-an-AI-Second-Brain-LLM-Wiki-Pattern-With-Claude-Code-and-Obsidian?source=post_page-----fc41cc213d50---------------------------------------)

### Build an AI-powered knowledge base in Obsidian. Use Claude Code slash commands to ingest, link, and query your notes…

github.com

## Frequently Asked Questions (FAQ)

**1\. What exactly is an AI second brain?**  
An AI second brain is a knowledge management system where an AI agent automatically organizes, links, and synthesizes your scattered notes into a structured wiki. Instead of you manually tagging and linking files, the AI reads your raw source material and builds a navigable knowledge base for you in Obsidian.

**2\. What tools do I need to build this system?**  
You need two core tools. The first is Obsidian, a free note-taking app that acts as the visual interface and stores everything as plain Markdown files. The second is Claude Code, a command-line AI agent that requires a paid Claude account (Pro, Max, or Team). Claude Code does the work of reading your notes and writing the linked wiki pages.

**3\. What is the LLM Wiki pattern by Andrej Karpathy?**  
The LLM Wiki pattern treats a wiki as a codebase that an LLM manages. Karpathy frames Obsidian as the IDE and the LLM as the programmer. The pattern’s most critical rule is strictly separating a read-only `raw/` directory for your original notes and a `wiki/` directory where the AI writes all synthesized pages.

**4\. Why do I need to separate the raw and wiki folders?**  
This separation is the foundational rule of the entire system. The `raw/` folder acts as your immutable memory of record that you own. The `wiki/` folder is the AI’s interpretation of that memory. If the AI were allowed to edit `raw/`, its synthesis would overwrite your original notes, and you would lose your source of truth.

**5\. What is a CLAUDE.md file and why is it important?**  
The CLAUDE.md file is a configuration rulebook placed at the root of your vault. Claude Code automatically reads this file in every session. It teaches the AI your vault’s structure, your preferred page conventions, your writing style, and the specific topics you work on so every page it creates follows your personal rules.

**6\. What are the four slash commands I need to know?  
**The entire system operates on four slash commands. `/ingest` compiles raw source notes into wiki pages. `/query` synthesizes cited answers from your wiki. `/lint` runs a health check to find broken links and orphan pages. `/log` captures a single thought or note and timestamps it to your activity log.

**7\. Where do I get the data to put in the raw folder?**  
You export your existing data from the apps you already use. The main sources include AI chat exports from Claude or ChatGPT, meeting notes from Granola, document exports from Notion or Google Docs, web clippings via the Obsidian Web Clipper, or Kindle highlights. You only need 5 to 10 files from one tool to get started.

**8\. My export files are in JSON, not Markdown. What should I do?**  
Most AI chat tools export conversations as JSON, which Obsidian cannot display natively. In this project, you use Claude Code to run a conversion script that scans your `raw/` folder, parses the JSON messages, and converts them into clean, human-readable Markdown files with proper YAML frontmatter for each conversation.

**9\. How long does the /ingest command take to run?**  
A full ingest can take 10 minutes or more on a large batch of source files and consumes a significant number of tokens. The recommended approach is to start with a demo ingest limited to 2 sources by typing `/ingest 2`. You then run the full ingest in smaller batches by re-running the command without arguments.

**10\. What will I see in Obsidian’s Graph View after an ingest?**  
After running `/ingest`, the Graph View transforms into an interconnected web. Each node is a wiki page, and each line represents a wiki-link between pages. Dense clusters of nodes show topics where your notes had the most overlap, while isolated nodes may indicate areas needing more source material.

**11\. What does the /query command actually do?**  
The `/query` command lets you ask questions about your own knowledge base. For example, you can ask "What are the main themes across my sources?" Claude Code will read your wiki pages, synthesize an answer grounded in your content, cite each claim by the specific wiki page name, and explicitly flag if any sources disagree with each other.

**12\. Why should I run the /lint command regularly?**  
Running `/lint` weekly, especially after a large ingest, keeps your wiki healthy. The command scans every wiki page and reports broken wiki-links, orphan pages that have no connections, missing required frontmatter fields, pages untouched for over 30 days, and any factual contradictions it finds between your pages.

**13\. Can I use this system if I am a complete beginner?**  
Yes, this project requires no prior coding experience. It has an “Easy” difficulty rating and a structured, step-by-step approach. The tutorial walks you through installing the tools, building the folder structure, and running your first AI commands. The only prerequisite is a paid Claude account to use Claude Code.

**14\. Is there a mobile app version of this second brain?**  
Claude Code, the AI agent that does the compiling, runs in a desktop terminal. However, Obsidian has a free mobile app for iOS and Android. You can sync your vault folder using iCloud or any cloud storage service to browse, read, and capture quick notes into your second brain from your phone, even if you cannot run the `/ingest` command there.

**15\. What happens after I finish this initial project setup?**  
Your daily workflow becomes a simple loop. You drop new source notes into `raw/` as you generate them, run `/ingest` to compile them into the wiki, and then use `/query` to explore the new connections. The system is designed so that every new note cross-links with what you already have, making the vault sharper the longer you use it.