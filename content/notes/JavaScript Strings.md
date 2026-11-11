---
title: JavaScript Strings
type: note
description:
tags:
  - js
  - javascript
publish: true
---
In JavaScript, a (non-template) string can be written with either single or double quotes [in](https://www.boot.dev/lessons/bbd972f7-cdba-44d6-afeb-1b80c6370422#:~:text=In%20JavaScript%2C%20a%20%28non%2Dtemplate%29%20string%20can%20be%20written%20with%20either%20single%20or%20double%20quotes%2E%20For%20example) [[JavaScript|source]] . For example:
- `'Hello'`
- `"Hello"`

**Personally, we prefer double quotes**! It's important to have styling conventions so that all the code in a project looks consistent, making it easier to read and contribute to.

## Indexing

Square brackets are used to access individual characters inside a string. The characters are numbered from `0` to `length-1`. It's similar to how strings and lists work in Python, Go and many other languages.

```js
const greeting = "Hello";
console.log(greeting[0]); // 'H'
console.log(greeting[1]); // 'e'
console.log(greeting[2]); // 'l'
console.log(greeting[3]); // 'l'
console.log(greeting[4]); // 'o'
// you can also get the last char at length-1
console.log(greeting[greeting.length - 1]); // 'o'
```

The [`.length`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/length) property is used to get the number of characters in a string.