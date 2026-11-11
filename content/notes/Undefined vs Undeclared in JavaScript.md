---
title: Undefined vs Undeclared in JavaScript
type: note
description:
tags:
  - js
  - javascript
publish: true
---
We can create an undefined variable by giving it a name, but no value [in](https://www.boot.dev/lessons/8d821ae2-58e1-41c1-b335-73fb01af2727#:~:text=We%20can%20create%20an%20undefined%20variable%20by%20giving%20it%20a%20name%2C%20but%20no%20value) [[JavaScript|source]]

```js
let favoriteSandersonCharacter; // undefined
console.log(typeof favoriteSandersonCharacter); // "undefined"
```

However if we _never create the name_, it's "un_declared_", and undeclared variables actually throw an error (so don't do this):

```js
console.log(favoriteRothfussCharacter); // ReferenceError: favoriteRothfussCharacter is not defined
```

The worst part is that the undeclared variable error actually says "not defined"

As an aside, you can use `const` to declare a variable that is assigned to `undefined`, but you wouldn't be able to set its value later, so why would you want to?

```js
const favoriteSandersonCharacter; // SyntaxError: missing = in const declaration
const favoriteSandersonCharacter = undefined; // undefined
```