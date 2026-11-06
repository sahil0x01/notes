---
title: Polymorphism in Python
type: note
description:
tags:
  - python
  - oops
publish: true
---
Polymorphism is the ability of a variable, function or object to take on multiple forms [in](https://www.boot.dev/lessons/d48609f7-48a6-4f28-b3ff-214aed9619df#:~:text=Polymorphism%20is%20the%20ability%20of%20a%20variable%2C%20function%20or%20object%20to%20take%20on%20multiple%20forms) [[Object Oriented Programming|source]]
- "poly" = "many"
- "morph" = "form"

For example, classes in the same hierarchical tree may have methods with the _same name and [signature](https://developer.mozilla.org/en-US/docs/Glossary/Signature/Function)_ but different implementations. Here's a simple example:

```python
class Creature:
    def move(self) -> None:
        print("the creature moves")


class Dragon(Creature):
    def move(self) -> None:
        print("the dragon flies")


class Kraken(Creature):
    def move(self) -> None:
        print("the kraken swims")


creatures: list[Creature] = [Creature(), Dragon(), Kraken()]
for creature in creatures:
    creature.move()
# prints:
# the creature moves
# the dragon flies
# the kraken swims
```

Because all three classes have a `.move()` method, we can shove the objects into a single list, and call the same method on each of them, even though the _implementation_ (method body) is different.