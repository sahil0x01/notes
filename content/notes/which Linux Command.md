---
title: which Linux Command
type: note
description:
tags:
  - linux
publish: true
---
The `which` command tells you the location of an installed command line program. For example, `which sh` asks for the location of the `sh` (shell) program. On most machines it lives at `/bin/sh` [in](https://www.boot.dev/lessons/5d1321fd-a35e-4d70-b20f-dc4721feae9a#:~:text=The%20which%20command%20tells%20you%20the%20location%20of%20an%20installed%20command%20line%20program%2E%20For%20example%2C%20which%20sh%20asks%20for%20the%20location%20of%20the%20sh%20%28shell%29%20program%2E%20On%20most%20machines%20it%20lives%20at%20%2Fbin%2Fsh%2E) [[Learn Linux]]

If you were to `cat /bin/sh`, you wouldn't see readable text. You'd see a screen full of garbage. That's because your `sh` program is a _compiled_ executable, probably written in C. The raw machine code isn't meant for human eyes.

A file with a `.sh` extension, on the other hand, is a shell script. It's a text file that contains commands that will be _interpreted_ and run by the `sh` program. They are both executable programs, but only one can be run without the help of another program.