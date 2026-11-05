---
title: Vector Addition in GPU
type: note
description:
tags:
  - gpu
  - cuda
publish: true
---
Let me explain a simple vector addition operation and specifically how we can do it in a GPU. This example is in the [[Programming Massively Parallel Processors - a Hands On Approach|source]]

From [[Data Parallelism|this]] note, we understood that we can do operations independently and do operations much faster, we can create thousands and millions of threads to operate independent operations

## Naive GPU Vector Addition
These are the steps to follow:
1. Allocate device memory for vectors like malloc in c
2. Transfer inputs host -> Device (Here host means CPU and Device means GPU)
3. Launch Kernel and perform additions (Kernels are simply functions that are defined and run on GPUs)
4. Copy or transfer back the output from Device -> Host
5. Free Device memory like `free()` in C language

> [!note]
> Normally, we keep data on the GPU as long as possible to asynchronously schedule many kernel launches

![[Screenshot 2026-11-03 at 13.51.03.png]]

This image is taken from [this](https://www.youtube.com/watch?v=NQ-0D5Ti2dc) video from GPU Mode channel

Here, we have to vectors $\vec{x}$ and $\vec{y}$, for each element of these two vectors we launch a thread and a single thread calculates the output for a single element to output vector $\vec{z}$

