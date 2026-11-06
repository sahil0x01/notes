---
title: Inheritance in Python
type: note
description:
tags:
  - python
  - oops
publish: true
---
Inheritance allows a "child" class, to inherit properties and methods from a "parent" class [in](https://www.boot.dev/lessons/62882641-2df2-4be0-8300-63c70ae2663f#:~:text=Inheritance%20allows%20a%20%22child%22%20class%2C%20to%20inherit%20properties%20and%20methods%20from%20a%20%22parent%22%20class%2E) [[Object Oriented Programming|source]]. It's a way to share code between classes. For example, say we have this Aircraft class:

```py
class Aircraft:
    def __init__(self, height: int, speed: int) -> None:
        self.height = height
        self.speed = speed

    def fly_up(self) -> None:
        self.height += self.speed
```

And say we want to also model more specific _kinds_ of aircraft. We could create a more specific `Helicopter` class like this:

```py
class Helicopter:
    def __init__(self, height: int, speed: int) -> None:
        self.height = height
        self.speed = speed
        self.direction = 0

    def fly_up(self) -> None:
        self.height += self.speed

    def rotate(self) -> None:
        self.direction += 90
```

Trouble is, we've rewritten a lot of the same code twice... wouldn't it be nice if a `Helicopter` could just take all the behavior from an `Aircraft`, and then just add its own unique behavior on top of that? Well, it can! We'll just make `Helicopter` a child class of `Aircraft`:

```py
class Helicopter(Aircraft):
    def __init__(self, height: int, speed: int) -> None:
        super().__init__(height, speed)
        self.direction = 0

    def rotate(self) -> None:
        self.direction += 90
```

By adding `Aircraft` in parentheses after `Helicopter`, we're saying "make `Helicopter` a child class of `Aircraft`". Now `Helicopter` inherits all the properties and methods of `Aircraft`!

The [super()](https://docs.python.org/3/library/functions.html#super) function returns a proxy of the parent class, meaning we can use it to call the parent class's constructor and other methods. So the `Helicopter`'s constructor says "first, call the `Aircraft` constructor, and then additionally set the `direction` property".

Now, say we want to create a `Jet` class. Again, because all jets are aircraft, we can inherit from `Aircraft` again. One parent class can have as many child classes as you want.

```py
class Jet(Aircraft):
    def __init__(self, speed: int) -> None:
        # Jets always start on the ground
        super().__init__(0, speed)

    def go_supersonic(self) -> None:
        self.speed *= 2
```


## When to Inherit
> A should only inherit from B if A is _always_ a B [in](https://www.boot.dev/lessons/c71187c5-3320-4ab6-b1a5-0211e68d3f1c#:~:text=A%20should%20only%20inherit%20from%20B%20if%20A%20is%20always%20a%20B) [[Object Oriented Programming|source]]

When a child class inherits from a parent, it inherits _everything_. If you only want to share _some_ functionality, inheritance should **not** be the tool you use. Just share some functions, or maybe make a new parent class that both classes can inherit from.