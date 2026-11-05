---
title: Shebang
type: note
description:
tags:
  - linux
publish: true
---
A ["shebang"](https://en.wikipedia.org/wiki/Shebang_\(Unix\)) is a special line at the top of a script that tells your shell which program to use to execute the file [in](https://www.boot.dev/lessons/897afab9-f2c7-478b-943a-792efb0c23f7#:~:text=A,script,-%2E) [[Learn Linux]]

The format of a shebang is:

```sh
#! interpreter [optional-arg]
```

For example, if your script is a Python script and you want to use Python 3, your shebang might look like this:

```sh
#!/usr/bin/python3
```

This tells the system to use the Python 3 interpreter located at `/usr/bin/python3` to run the script.