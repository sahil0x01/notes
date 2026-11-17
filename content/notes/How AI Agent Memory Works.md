---
title: How AI Agent Memory Works
type: note
description:
tags:
  - ai
  - agents
publish: true
---
## Problems with Memory
> Loss of procedure, knowledge and progress [[Agentic Systems Explained|source]]

You have to explain the same thing everytime be it a plan a fact, preference. Also when a session grows too long and you want to continue working on a new session, the agent cannot recall what we did last time and so on

## Benefits of Agent Memory
> Personalization, learning from experience and statefulness [[Agentic Systems Explained|source]]

With memory, agents can learn your preference and act accordingly, they can learn things and start to apply those learning across sessions and as I said you can start a new session and continue to work on some old stuff as they would remember where we left off, instructions, etc


## Types of Memory
[This](https://arxiv.org/pdf/2309.02427) paper is a very important paper as a lot of people have built memory systems based on [this](https://arxiv.org/pdf/2309.02427) paper![[coala-paper.png]]

Here, we have:
- Procedural Memory: the set of rules that can be applied to the working memory to determine the agents behaviour. Essentially the skills of the agent. It's the knowledge of HOW to complete tasks
- Semantic Memory: Stores facts about the world, details about the user, preferences, general knowledge, etc
- Episodic Memory: its the sequences of the agents past behaviours like in chatbots this is a store of all the prior chats. Generally its the raw logs of what occured
- Working Memory: Generally the context window, this is what agent generally sees and is reasoning over including observations, goals, user input and internal reasoning

![[parametric-vs-context-memory.png]]

## Key Questions to Ask When we Think About Memory Architecture
- **What** will get stored to/retrieved from memory?
	- Facts (specific and general), Procedures, Conversation progress, ...
- **When** will we trigger the memory storage/retrieval?
	- Agent tools (on-demand), background workers, event-driven, ...
- **How** will we store memories/retrieve from memory?
	- Filesystem, databases(retrieval), knowledge graphs, ...


## The HOW Part
The three most common approaches are: filesystem, databases and knowledge graphs

### FileSystem
- Every memory is a file
- Can let the agent manage its memories
- Adds hierarchy by default
- Grep, ls, and other bash commands are the memory tools![[file-system-memory.png]]


### Database
- Can build a vector database and retrieve memories from it
- Common to use SQLite DB if you want to search over metadata
- For exact term lookup, you can use BM25

### Knowledge Graph
Skipping creating notes on it for now