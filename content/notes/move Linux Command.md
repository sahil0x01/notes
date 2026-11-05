---
title: move Linux Command
type: note
description:
tags:
  - linux
publish: true
---
The [move command](https://www.ibm.com/docs/en/aix/7.3?topic=files-moving-renaming-mv-command) moves a file or directory from one location to another. You can use it to rename a file or to move it to a different directory altogether. If you're moving a directory, it can't be your current working directory [in](https://www.boot.dev/lessons/570087ff-dc69-4396-94f6-0ac620bf9550#:~:text=The,images) [[Learn Linux]]

Renaming a file:

```sh
mv draft.md final.md
```

Moving a file from the current directory to another nested directory:

```sh
mv report.csv archives/report.csv
```

Moving a file from the current directory, to the parent directory:

```sh
mv invoice.pdf ../invoice.pdf
```

If you don't want to rename the file and you're just moving it to a different directory, you can omit the filename:

```sh
mv photo.png images/
```