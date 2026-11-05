---
title: Linux Changing Permissions
type: note
description:
tags:
  - linux
publish: true
---
The [chmod command](https://www.ibm.com/docs/en/aix/7.3?topic=c-chmod-command) lets you change the permissions of a file or directory [in](https://www.boot.dev/lessons/633f53b5-29fe-4de3-b039-f1df17b9f57c#:~:text=The%20chmod%20command%20lets%20you%20change%20the%20permissions%20of%20a%20file%20or%20directory) [[Learn Linux]]

To recursively change a directory and everything inside it, use the `-R` flag:

```sh
chmod -R u=rwx,g=,o= DIRECTORY
```

In the command above, `u` means "user" (aka "owner"), `g` means "group," and `o` means "others." The `=` means "set the permissions to the following," and the `rwx` means "read, write and execute." The `g=` and `o=` mean "set group and other permissions to nothing." The uppercase `-R` means "recursively," which means "do this to all of the contents of the directory as well."