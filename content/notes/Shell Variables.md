---
title: Shell Variables
type: note
description:
tags:
  - linux
publish: true
---
Shells aren't just for running other programs. Bash and Zsh also happen to be powerful programming languages: they have variables, functions, loops, and more. That said, only [crazy people](https://github.com/cgsdev0/bash-stack) write large programs in shell languages... shells are optimized for running other programs and writing small scripts, not for writing large applications [in](https://www.boot.dev/lessons/004ccd6e-6614-4468-bc74-51e3bb293011#:~:text=Shells,applications) [[Learn Linux]]

## Creating a Variable
```bash
name="Sahil"
```
Notice there are no spaces between the variable `name`, assignment operator `=` and value `"Sahil"`


## Using a Variable
```bash
echo $name
Sahil
```
In shell, we need to use the `$` prefix with the variable name to use it otherwise it'll just print the text "name"

## Interpolating a Variable in a String
```bash
echo Hello $name
Hello Lane
```
