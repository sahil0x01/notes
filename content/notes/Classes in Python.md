---
title: Classes in Python
type: note
description:
tags:
  - python
  - oops
publish: true
---
A [class](https://docs.python.org/3/tutorial/classes.html) is a special type in an object-oriented programming language like Python. If you squint really hard, it's kinda like a dictionary in that it usually stores name-value pairs [in](https://www.boot.dev/lessons/28072480-92b7-40e7-9a82-09f0a9b0241d#:~:text=A,define) [[Object Oriented Programming|source]] :

```python
# Defines a new class called "Soldier"
# with three properties: health, armor, damage
class Soldier:
    health: int = 5
    armor: int = 3
    damage: int = 2
```

Just like a string, integer or float, a class is a _type_, but instead of being a built-in type, classes are custom types that you define.