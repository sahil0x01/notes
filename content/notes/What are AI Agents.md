---
title: What are AI Agents
type: note
description:
tags:
  - ai
  - agents
publish: true
---
## History of Agents
The word agent comes from the Latin word "agens". This means "the one who acts". There is this [paper](https://ijcai.org/proceedings/1973/0031.pdf) from Hewitt, Bishop and Steiger in 1973 
![[actor-formalism.png]]

I'll make some notes on this paper, once I finish reading this. This "agent" concept is older than most people think

The LLM era of Agents changed in a way so that we can give models examples and then they can do the tasks. Basically, currently agents are becoming more and more general tasks handlers. Previously its mostly for specific tasks

## Anatomy of an Agent
There are 5 components:
- the model: its the LLM core or only the model capabilities
- thinking tokens: Its the section of planning and reasoning, you can see these tokens coming in the response
- Traces so far: memory component of an agent
- Act: The tools that the agent can use to take actions like search tool, bash tool, grep tool and so on
- Observation: The observations that the agent makes based on its environment


> I need to read the Reflextion paper as well

## Why we Need Memory for Agents
Even though the context window for models are improving but still they are not enough for tasks that are there for long hours like 5-10 hours or may be days too.

### Different Types of Memory
There are mainly 3 types of memory episodic memory, semantic memory and procedural memory. I'll add the links to the research paper and my notes on the research paper later once I finish reading them