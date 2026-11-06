---
title: Methods in Python
type: note
description:
tags:
  - python
  - oops
publish: true
---
A method is just a function that's tied directly to a class and has access to its properties [in](https://www.boot.dev/lessons/a97af3a9-e2e7-4568-a6c8-532071e059fc#:~:text=A%20method%20is%20just%20a%20function%20that%27s%20tied%20directly%20to%20a%20class%20and%20has%20access%20to%20its%20properties) [[Object Oriented Programming|source]] . See the `take_damage` method here:

```python
class Soldier:
    health: int = 5

    # This is a method that reduces the
    # health of the soldier
    def take_damage(self, damage: int) -> None:
        self.health -= damage


soldier_one = Soldier()
soldier_one.take_damage(2)
print(soldier_one.health)
# prints "3"

soldier_two = Soldier()
soldier_two.take_damage(1)
print(soldier_two.health)
# prints "4"
```

## Self

Methods are defined _within_ the `class` declaration. Their first parameter is always the instance of the class that the method is being called on. By convention, it's called ["self"](https://docs.python.org/3/glossary.html#term-method), and because `self` is a reference to the object, you can use it to read and update the properties of the object.

Notice that methods are called directly on an object instance using the dot operator:

```python
my_object.my_method()
```

## Methods Can Return
If a normal function doesn't return anything, it's typically not a very useful function. In contrast, methods often don't return anything because they can mutate (update) the properties of the object instead.[in](https://www.boot.dev/lessons/882a9e84-f9c3-49aa-8e66-78b15ae49fe0#:~:text=If,instead%2E) [[Object Oriented Programming|source]]

However, they _can_ return values if you want! They're just functions with access to an object, after all. A common use case is a "getter" method that returns a calculated value based on the properties of the object.

```python
class Soldier:
    armor: int = 2
    num_weapons: int = 2

    def get_speed(self) -> int:
        speed = 10
        speed -= self.armor
        speed -= self.num_weapons
        return speed


soldier_one = Soldier()
print(soldier_one.get_speed())
# prints "6"
```