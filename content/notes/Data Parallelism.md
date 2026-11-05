---
title: Data Parallelism
type: note
description:
tags:
  - gpu
  - cuda
publish: true
---
There are so many cases where we want to compute some global operations like blurring a image or may be pixelating an image, grey scaling an image and so on. 

> [!note]
> Writing data parallel code entails (re)organizing the computation around the data such that one can execute the resulting independent computations in parallel to complete the overall job faster – often much faster [[Programming Massively Parallel Processors - a Hands On Approach|source]]
> 



If you'll notice, all these operations can be independent as they are dependent on either only a single pixel or neighbouring pixels. Like if you want to greyscale an image, each operation is dependent on a single pixel so we can parallelly do these operations independently and increase the speed of this operation much more than what we could have achieved by doing this global operation sequentially

There are other examples as well but this is the simplest one and much more closer to what we are learning right now

