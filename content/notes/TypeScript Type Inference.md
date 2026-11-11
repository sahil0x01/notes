---
title: TypeScript Type Inference
type: note
description:
tags:
  - ts
  - typescript
publish: true
---
[Type inference](https://www.typescriptlang.org/docs/handbook/type-inference.html) lets TypeScript determine a variable's type _from its value_, so we actually don't need to write obvious annotations [in](https://www.boot.dev/lessons/f215c3bf-2cb9-4b05-8d87-232edfcd5939#:~:text=Type%20inference%20lets%20TypeScript%20determine%20a%20variable%27s%20type%20from%20its%20value%2C%20so%20we%20actually%20don%27t%20need%20to%20write%20obvious%20annotations) [[TypeScript|source]]

```ts
// explicit (unnecessary)
const bootupLog: string = "starting server...";

// inferred (preferred)
const bootupLog = "starting server...";
```

Both versions are type-safe, but the inferred version is shorter!