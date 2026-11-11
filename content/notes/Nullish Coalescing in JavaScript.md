---
title: Nullish Coalescing in JavaScript
type: note
description:
tags:
  - js
  - javascript
publish: true
---
The [`nullish coalescing`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing) operator `??` is a way to handle these cases in a more concise way [in](https://www.boot.dev/lessons/597d103c-3bff-4848-bad6-1eea37482005#:~:text=The%20nullish,empty%2E) [[JavaScript|source]]

```js
let myName = null;
console.log(myName ?? "Anonymous"); // "Anonymous"

myName = "Lane";
console.log(myName ?? "Anonymous"); // "Lane"
```

If the value on the left of `??` is `null` or `undefined`, the value on the right is returned. Otherwise, the value on the left is returned. **It's a way to set sane defaults for variables that might be empty**.