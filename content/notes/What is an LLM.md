---
title: What is an LLM
type: note
description:
tags:
  - llm
  - ai
  - inference
publish: true
---
A large language model is a class of language models based on deep neural networks and trained on massive amounts of text. Its core capability is: given a piece of text, predict the next most likely token [in](https://datawhalechina.github.io/zero-to-sglang/eng/part1/Chapter1_Introduction_to_LLM.html#_6-2-exercises:~:text=A,token%2E) [[Zero To SGLang|source]]

In 2017, Google published the Transformer architecture in a paper called "Attention is all you need". This architecture replaced RNNs/CNNs with self attention mechanism

Then in 2018-2019, two different variants came up: BERT(A Bidirectional Encoder) and GPT(An Autoregressive Decoder)

In 2020, GPT-3 (175B parameters) model release and it showed something called "few-shot learning" capability

From 2022 to present, we have now a bunch of models


There are some limitations too, these models can give you response and they might look correct but they are wrong (we call this hallucination), models have a limited knowledge and this happens due to their training data cutoff date, these models have limited memory and that's why models start to perform worse if the context window exceed with a long task

