---
title: "LLMs lack latent attention?"
date: 2026-04-11
---

Depending on how you read this blog^[No one reads this blog], you might not know that [the UC Merced Philosophy Department has a YouTube channel](https://www.youtube.com/@UCMercedPhilosophy) where we post recordings of our colloquium talks. Our guest this week^[The videos are still in editing as I'm writing this] was philosopher and cognitive scientist [Jelle Bruineberg](https://researchprofiles.ku.dk/en/persons/jelle-pieter-bruineberg/) from the University of Copenhagen. As I understood things from his talks, Jelle is developing an *interest-based account of attention*, on which our capacity to selectively focus on certain aspects of our environment and ignores others is tied to our goals and other interests. 

I've been attending way too much to LLMs recently, and in particular while playing around with Claude Code over the past three weeks I've noticed an interesting pattern. Claude is very, very good at identifying coding errors, anticipating bugs before/without actually running the code, and writing assertions, tests, and validation scripts to make sure everything is working correctly. But only when explicitly instructed to do so. By default, Claude will happily write buggy code and declare a task complete without any validation whatsoever, even when it writes a workplan that includes a list of validation steps at the end. 

An important aspect of Jelle's account is the idea of *latent attention*. This starts with an observation that we have innumerable goals and interests, many of which stretch out indefinitely over time and context. In any given context, most of our goals and interests are not salient and appropriately do not play a role in our active attention. But even a slight change of context can significantly change which of our goals and interests are salient. And so an important part of our attention mechanism — "latent attention" — must be managing or monitoring these latent interests, so that they can be activated when necessary. 

Given a software development task — one I've been playing around with this week is a simple chatroom web app — it seems reasonable to attribute to Claude^[At least, in the particular sessions/instances where the prompt is to develop this software] the goal of producing working and reliable code. Claude is remarkably capable of managing a significant amount of information in its context window — the prompt, the `CLAUDE.md` that gives general context for the project, the current file structure of the project and contents of particular source files — and actively attending to the most salient elements. 

But, when the context doesn't explicitly include checking for coding errors and actively verifying that everything works and will continue to work, Claude does not seem to have a reliable way of attending to these aspects of the task. In other words, Claude doesn't seem to have a latent attention mechanism, managing and monitoring non-explicit interests and activating them when they become salient. 



