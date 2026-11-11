---
title: JavaScript Conditionals
type: note
description:
tags:
  - js
  - javascript
publish: true
---
`if` statements in JavaScript use parentheses around the condition [in](https://www.boot.dev/lessons/e1fbef2d-496b-41a1-9e57-f55d3f717670#:~:text=if%20statements%20in%20JavaScript%20use%20parentheses%20around%20the%20condition) [[JavaScript|source]]

```javascript
if (height > 4) {
  console.log("You are tall enough!");
}
```

`else if` and `else` are supported as you might expect:

```javascript
if (height > 6) {
  console.log("You are super tall!");
} else if (height > 4) {
  console.log("You are tall enough!");
} else {
  console.log("You are not tall enough!");
}
```

We'll cover some more of these, but for now, here are some common comparison operators:

- `===` equal to
    
- `!==` not equal to
    
- `<` less than
    
- `>` greater than
    
- `<=` less than or equal to
    
- `>=` greater than or equal to