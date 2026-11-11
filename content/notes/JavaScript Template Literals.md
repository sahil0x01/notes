---
title: JavaScript Template Literals
type: note
description:
tags:
  - js
  - javascript
publish: true
---
They're JavaScript's version of Python's f-strings [in](https://www.boot.dev/lessons/9b16d2d7-d436-4fc7-a986-30f29868cb8e#:~:text=They%27re%20JavaScript%27s%20version%20of%20Python%27s%20f%2Dstrings) [[JavaScript|source]] . For example:

```javascript
const shadeOfRed = 101;
console.log(`The shade is ${shadeOfRed}`);
// The shade is 101
```

Template literals _must start and end with a backtick_, and anything inside of the dollar-sign bracket enclosure is automatically _cast_ to a string.