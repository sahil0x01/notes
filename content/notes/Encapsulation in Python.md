---
title: Encapsulation in Python
type: note
description:
tags:
  - python
  - oops
publish: true
---
[Encapsulation](https://en.wikipedia.org/wiki/Encapsulation_\(computer_programming\)) is the practice of hiding complexity inside a ["black box"](https://en.wikipedia.org/wiki/Black_box) so that it's easier to focus on the problem at hand [in](https://www.boot.dev/lessons/6cd6445f-6226-4a98-a9f9-ee03e07cf37c#:~:text=Encapsulation%20is%20the%20practice%20of%20hiding%20complexity%20inside%20a%20%22black%20box%22%20so%20that%20it%27s%20easier%20to%20focus%20on%20the%20problem%20at%20hand) [[Object Oriented Programming|source]]
The simplest example of encapsulation is a function. The caller of a function doesn't need to worry too much about what happens inside, they just need to understand the inputs and outputs.

```py
# who even knows how this function works???
# I sure don't, I just call it and assume
# it calculates the acceleration correctly
acceleration: float = calc_acceleration(initial_speed, final_speed, time)
```

To _use_ the `calc_acceleration` function, we don't need to think about each line of code inside the function definition. We just need to know that if we give it the inputs:

- `initial_speed`
- `final_speed`
- `time`

It will produce the correct `acceleration` as an output.

## Public and Private
By default, all properties and methods in a class are _public_. That means that you can access them with the `.` operator:

```python
wall.height = 10
print(wall.height)
# 10
```

[Private](https://docs.python.org/3/tutorial/classes.html#tut-private) data members are a way to encapsulate logic and data _within a class definition_. To make a property or method private just prefix it with two underscores:

```python
class Wall:
    def __init__(self, armor: int, magic_resistance: int) -> None:
        self.__armor = armor
        self.__magic_resistance = magic_resistance

    def get_defense(self) -> int:
        return self.__armor + self.__magic_resistance


front_wall = Wall(10, 20)

# This results in an error
print(front_wall.__armor)

# This works
print(front_wall.get_defense())
# 30
```

We do this to make it _easier to use our class_. Now when another developer (or even ourselves) use the `Wall` class, they don't need to think about how `armor` and `magic_resistance` affect the `defense` of a `Wall`. In fact, we don't even allow them to access `armor` and `magic_resistance` directly by making them private with `__`.

They simply call the public `get_defense()` method and know that the correct value will be returned.

Encapsulation is all about making code easy to work with by "hiding" complicated code within a "[black box](https://en.wikipedia.org/wiki/Black_box)". It makes it so we don't have to worry about the details of how a function or method works... we just _use_ it.

This is kinda like how the inner workings of your car's power steering are hidden from you. You don't need to be an expert on hydraulic systems to turn the wheel from side to side.


> Encapsulation and the concepts of private and public members have **NOTHING** to do with security. Encapsulation and the concepts of private and public members have **NOTHING** to do with security

**Encapsulation is about organization, not security.**