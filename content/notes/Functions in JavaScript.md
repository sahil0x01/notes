---
title: Functions in JavaScript
type: note
description:
tags:
  - js
  - javascript
publish: true
---
This is how function declaration works in JavaScript:
```js
// function declaration
function getSum(a, b) {
  return a + b;
}

// function call
const result = getSum(60, 9);

console.log(result);
// 69
```


In Python, a function must be defined _before_ any code that executes it. But that's _not so_ in JavaScript! As long as a function is defined _somewhere_ in the file, it can be called even _before_ the definition [in](https://www.boot.dev/lessons/c7d0b185-4962-40e4-9796-613ed07a6d47#:~:text=In,definition) [[JavaScript|source]]

```js
console.log(getLabel(3));
// prints 'awful'

function getLabel(numStars) {
  if (numStars > 7) {
    return "great";
  } else if (numStars > 3) {
    return "okay";
  } else {
    return "awful";
  }
}
```

This works because JavaScript ["hoists"](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting) the function declaration to the top of the file _before_ the code is executed.