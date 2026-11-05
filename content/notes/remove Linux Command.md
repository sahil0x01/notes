---
title: remove Linux Command
type: note
description:
tags:
  - linux
publish: true
---
The [remove command](https://www.ibm.com/docs/en/aix/7.3?topic=files-deleting-rm-command) deletes a file [in](https://www.boot.dev/lessons/f0720fd2-b19d-41a9-a30d-60cb2127e4cd#:~:text=The,some%5Fdirectory) [[Learn Linux]] :

```sh
rm some_file.txt
```

You can optionally add a `-r` flag to tell the `rm` command to delete a directory and _all_ of its contents recursively. "Recursively" is just a fancy way of saying "do it again on all of the subdirectories and their contents."

```sh
rm -r some_directory
```