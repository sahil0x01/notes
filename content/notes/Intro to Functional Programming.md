---
title: Intro to Functional Programming
type: note
description:
tags:
  - functional-programming
  - python
publish: true
---
Functional programming is a style (or "paradigm" if you're pretentious) where we compose functions instead of mutating state [in](https://www.boot.dev/lessons/acb5117d-0f34-40b3-81f0-b89828f0e443#:~:text=Functional%20programming%20is%20a%20style%20%28or%20%22paradigm%22%20if%20you%27re%20pretentious%29%20where%20we%20compose%20functions%20instead%20of%20mutating%20state%2E) [[Functional Programming in Python|source]] . By contrast, [imperative programming](https://en.wikipedia.org/wiki/Imperative_programming) updates state along the way:

```python
car = create_car()
car.add_gas(10)
print(car.get_gas())
# 10
```

[Functional programming](https://en.wikipedia.org/wiki/Functional_programming) composes functions that return new values:

```python
car = create_car()
car_with_gas = add_gas(car, 10)
gas = get_gas(car_with_gas)
print(gas)
# 10
```

Each function's output becomes the next function's input. The original `car` isn't changed, because `add_gas` just returns a new copy.