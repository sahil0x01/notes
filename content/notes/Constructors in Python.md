---
title: Constructors in Python
type: note
description:
tags:
  - python
  - oops
publish: true
---
A constructor is a specific method on a class called [`__init__`](https://docs.python.org/3/reference/datamodel.html#object.__init__) that is called automatically when you create a new instance of a class. [in](https://www.boot.dev/lessons/896116cd-38a8-4401-a36d-3557a0214a44#:~:text=A%20constructor%20is%20%28usually%29%20better%2E%20It%27s%20a%20specific%20method%20on%20a%20class%20called%20%5F%5Finit%5F%5F%20that%20is%20called%20automatically%20when%20you%20create%20a%20new%20instance%20of%20a%20class) [[Object Oriented Programming|source]]
So, using a constructor, the code from above would look like this:

```python
class Soldier:
    def __init__(self) -> None:
        self.name = "Legolas"
        self.armor = 2
        self.num_weapons = 2
```

Not only is this _safer_ (we'll talk about why later), but it also allows us to make the starting property values configurable:

```python
class Soldier:
    def __init__(self, name: str, armor: int, num_weapons: int) -> None:
        self.name = name
        self.armor = armor
        self.num_weapons = num_weapons


soldier_one = Soldier("Legolas", 2, 10)
print(soldier_one.name)
# prints "Legolas"
print(soldier_one.armor)
# prints "2"
print(soldier_one.num_weapons)
# prints "10"

soldier_two = Soldier("Gimli", 5, 1)
print(soldier_two.name)
# prints "Gimli"
print(soldier_two.armor)
# prints "5"
print(soldier_two.num_weapons)
# prints "1"
```