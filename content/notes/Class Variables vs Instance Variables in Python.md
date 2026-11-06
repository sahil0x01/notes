---
title: Class Variables vs Instance Variables in Python
type: note
description:
tags:
  - python
  - oops
publish: true
---
## Instance Variables
Instance variables vary from object to object and are **declared in the constructor** [in](https://www.boot.dev/lessons/c41fcdcf-4d78-4d40-945e-6014fabef3a4#:~:text=Instance%20variables%20vary%20from%20object%20to%20object%20and%20are%20declared%20in%20the%20constructor%2E%20They%27re%20more%20common) [[Object Oriented Programming|source]] They're more common:

```python
class Wall:
    def __init__(self) -> None:
        self.height = 10  # instance variable (per object)


south_wall = Wall()
south_wall.height = 20  # only updates this instance of a wall
print(south_wall.height)
# prints "20"

north_wall = Wall()
print(north_wall.height)
# prints "10"
```

## Class Variables
Class variables are shared between instances of the same class and are **declared at the top level of a class definition** [in](https://www.boot.dev/lessons/c41fcdcf-4d78-4d40-945e-6014fabef3a4#:~:text=Class%20variables%20are%20shared%20between%20instances%20of%20the%20same%20class%20and%20are%20declared%20at%20the%20top%20level%20of%20a%20class%20definition%2E) [[Object Oriented Programming|source]] They're less common:

```python
class Wall:
    height: int = 10  # class variable (shared across all instances)


south_wall = Wall()
print(south_wall.height)
# prints "10"

Wall.height = 20  # updates all instances of a Wall

print(south_wall.height)
# prints "20"
```