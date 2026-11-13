---
title: RAG Explained
type: note
description:
tags:
  - ai
  - agents
publish: true
---
## Why Retrieval?
This helps the LLM to get the exact information from the source instead of just guessing its answer. Like checking your calender to tel you about your next meeting time instead of guessing, if LLM can retrieve your calender information then it can give you the actual and factual answer

This is a dynamic process and can give you citations to the sources it used for the answer which really helps in verifying the solution [[Agentic Systems Explained|source]]

> [!Note] Retrieval is a common mechanism for identifying such relevant information:
> - Dynamic: its easy to update/add documents to your retrieval system
> - Interpretable: LLM can generate pointers to retrieved documents that support human verification of its generations (citations)


## Retriever - Reader Framework
Input: a large collection of documents $D = D_1, D_2, ..., D_n$ and $Q$
Output: an answer string $A$

> Q stands for question
> D stands for Documents
> A stands for answer

Retriever: $f(D, Q) -> P_1, ..., P_k$ . Here, $k$ is pre-defined (e.g., 100 or 50 or 10)
Reader: $g(Q, {P_1, ..., P_k}) -> A$. Here, $A$ is reading comprehension problem



## Retrieval Augmented Generation (RAG)
