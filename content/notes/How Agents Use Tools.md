---
title: How Agents Use Tools
type: note
description:
tags:
  - ai
  - agents
publish: true
---

## What are Tools?
An LM-used tool is a function interface to a computer program that runs externally to the LM, where the LM generates the function calls and input arguments in order to use the tool [[Agentic Systems Explained]]

For example, doing web search or interacting with some api's like getting weather, getting location, time, some interpreter like python, node, etc to execute code and so on![[tool-use-examples.png]]

## Learning to Call Tools
[This](https://arxiv.org/abs/2302.04761) paper explains that LLMs can teach themselves to use tools

Toolformer trains LMs to decide which APIs to call, when to call them, what arguments to pass and how to best incorporate the results [[Agentic Systems Explained]]

