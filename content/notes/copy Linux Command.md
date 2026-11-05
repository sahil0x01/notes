---
title: copy Linux Command
type: note
description:
tags:
  - linux
publish: true
---
The [copy command](https://www.ibm.com/docs/en/aix/7.3?topic=c-cp-command) does what you would (hopefully) expect: it copies a file from one location to another [in](https://www.boot.dev/lessons/ba3c8b4f-aedd-4aad-99b3-59d17fcf3fb6#:~:text=The,new%5Fdir) [[Learn Linux]]

```sh
cp source_file.txt destination/
```

You can also copy a directory and all of its contents recursively by adding the `-R` flag:

```sh
cp -R my_dir new_dir
```
