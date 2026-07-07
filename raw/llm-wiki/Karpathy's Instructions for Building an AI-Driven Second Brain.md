---
title: "Karpathy's Instructions for Building an AI-Driven Second Brain"
source: "https://techstrong.ai/features/karpathys-instructions-for-building-an-ai-driven-second-brain/"
author:
  - "[[Joab Jackson]]"
published: 2026-04-07
created: 2026-07-07
description: "The RAG approach requires vector computation to find similar sets of words that could be used to build an answer to your question."
tags:
  - "clippings"
---
Ever worry about all the stuff you learned before, but have since forgotten about? Or maybe you are curious about latent ideas lurking in your subconscious?

A personal knowledge base, automated with AI, could be valuable for such ideation. Now, the Godfather of Vibe Coding, Andrej Karpathy, has created a personal knowledge base for himself, providing a pattern that others can use as well.

“I think there is room here for an incredible new product,” he wrote on X.

A personal knowledge base would work best for compulsive note-takers, or compulsive collectors of web data, though it could theoretically work on any body of knowledge.

The idea is to aggregate all the documents about a subject of interest into a directory or repository, then have an LLM compile the data into a wiki of markdown files, so it then can easily answer questions, and generate synthetic data, with this curated data set.

Once you accumulate about 100 articles, or about 400,000 words, your LLM agent can answer complex questions about the wiki, and with a lot less work.

Maintaining a knowledge base reduces the number of tokens you need to explore the subject, as the markdown files are condensed versions of the raw data that the LLM could use for source material.

It sounds a bit like standard knowledge management, but with some key differences. KM solutions tend to keep documents in proprietary formats and require the user to annotate the material with metadata. Karpathy’s approach has the LLM do the indexing and updating, and files are written into the wiki using an open markdown format.

In a sense, Karpathy is borrowing from author Tiago Forte’s 2022 book “Building a Second Brain,” which popularized the concept of building a knowledge base to store the details of everything someone learns.

But with Karpathy’s pattern, it is the LLM, not the user, that does all the indexing.

“You rarely ever write or edit the wiki manually, it’s the domain of the LLM,” Karpathy wrote.

### LLM-Managed Markdown

In a traditional chat session, the LLM uses Retrieval Augmented Generation (RAG) to build responses. The RAG approach requires vector computation to find similar sets of words that could be used to build an answer to your question.

With the knowledge base itself, the LLM can search across the base at a fraction of the computational cost.

Most data online, from chats to web pages to audio files, is swamped in metadata and formatting data, which is all a great deal of chaff that the RAG must remove to get at the data. Plus a lot of the data is duplicated, which the LLM must reconcile again and again, for each new session.

A knowledge base gives the AI a more compact, more refined set of data to work with.

Those who run Google’s NotebookLM or similar AI-infused knowledge management tools get the idea. But while NotebookLM can be used for individual projects, the Karpathy approach could be used for all the documents in the person’s life. In essence, the repository of contents, not the app itself, is the locus of the information.

This also helps with the stateless AI problem. Each new session, the LLM must learn the material again, as well as the person’s background. More tokens; more work for the LLM. With this approach the LLM can update the wiki with this stateful information, so it can be easily picked up later.

### Karpathy’s Stack

In subsequent X messages, Karpathy admitted that he has not fully automated the process yet. He still adds in documents by hand, though he has the LLM file and index the new document itself.

Karpathy wrote a “hacky collection of scripts” in Python to bridge the LLM and his material. The scripts instruct the LLM to read the data and write the Wiki files. The scripts also let the LLM know to reason through the knowledge base to find answers. He also created a linting process, some LLM-based health checks to identify incorrect and missing information, as well as to add in additional information.

Karpathy reviews the results in Obsidian, a tool he uses for note-taking that captures notes and web articles in markdown, as well as in a slide-show format.

### Second Brain-as-a-Service

Karpathy is one of the most influential independent developers in the AI space. He coined the term vibe coding, which describes the process of quickly iterating new applications through AI. He was a founding member and research scientist for OpenAI, and was the director of AI at Tesla, guiding the company through the early stages of developing autopilot. In 2024, he founded Eureka Labs to focus on AI-native education.

Others quickly took notice of the knowledge base pattern Karpathy described. Popular sci/tech podcaster Lex Fridman set up a similar repository, which generates “interactive podcasts” on specific topics that can present the material and answer questions while he runs. Blogger Robert Scoble has also set up a similar set of AI-driven software to keep track of the AI news on X.

On X, engineer Nick Spisak walked through a process of creating such a “second brain,” one that doesn’t involve writing any code. He suggested setting up three folders. One is for the source data, the second is for the Wiki where the LLM will place the organized material, and the third will hold the answers to the questions it is asked.

Then, create a schema file to describe the knowledge base to the LLM.

Spisak suggested building “domain-specific” vaults, rather than trying to cram everything into one giant directory, which could lead to diffuse results.

One can use Obsidian to view what the LLM creates, and the Obsidian Web Clipper Chrome plug-in to capture any new material you find on the Web. Spisak also suggested using Vercel Labs’ agent-browser, which allows an LLM to use a browser to find and download more web posts. You also need Node.js on your machine for this to work.

You will need to run an AI coding agent, such as Claude Code or the OpenAI Codex.

“The AI is the librarian. You give it rules via a config file, and it maintains your entire wiki. You never manually organize a single page,” Spisak wrote.