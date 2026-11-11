---
title: TypeScript Basic Types
type: note
description:
tags:
  - ts
  - typescript
publish: true
---
TypeScript adds type annotations to JavaScript variables using a `:` followed by the type [in](https://www.boot.dev/lessons/e22ec6b8-33a2-44f9-82b7-b48494961f91#:~:text=TypeScript,string%27%2E) [[TypeScript|source]] . The most common primitive types are:

```ts
const bootupMessage: string = "starting server...";
const port: number = 3000;
const isOnline: boolean = true;
const noValue: null = null;
const notDefined: undefined = undefined;
```

If a value doesn't match its type, the TypeScript compiler reports an error:

```ts
const bootupMessage: string = 123;
// Error: Type 'number' is not assignable to type 'string'.
```