---
title: JavaScript Variables
type: note
description:
tags:
  - js
  - javascript
publish: true
---
[`var`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var) is the _old_ way to declare variables in JavaScript. Use [`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) when reassignment is allowed and [`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const) when it isn't [in](https://www.boot.dev/lessons/35adce15-77ba-4ab8-a1cd-1d4abb065441#:~:text=var%20is%20the%20old%20way%20to%20declare%20variables%20in%20JavaScript%2E%20Use%20let%20when%20reassignment%20is%20allowed%20and%20const%20when%20it%20isn%27t) [[JavaScript|source]]

```javascript
// username can be reassigned, so we use `let`
let username = "dengar_the_bh";
username = "boba_fett";

// smsSendingLimit can't be reassigned, so we use `const`
const smsSendingLimit = 1000;
```

`var` is function-scoped, so a variable declared inside an `if` block can leak outside it! `let` and `const` are block-scoped, which is ~~always~~ usually what you want.