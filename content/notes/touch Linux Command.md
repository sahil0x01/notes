---
title: touch Linux Command
type: note
description:
tags:
  - linux
publish: true
---
The [`touch`](https://man7.org/linux/man-pages/man1/touch.1.html) command updates the access and modification timestamps of a file. By default, if the specified file does not exist, `touch` will create an empty file with the given filename. Because of this side-effect, you'll often see this command used to quickly create new empty files.

```sh
touch new_file.txt
```

You can also create multiple files at once by listing them:

```sh
touch some_file.txt some_other_file.txt
```

`touch` can be very handy when writing scripts because it ensures files exist without altering existing ones, creating new files only if necessary [in](https://www.boot.dev/lessons/2dada879-c1e5-4b4f-99b1-0165c5062b7f#:~:text=The,necessary) [[Learn Linux]]

