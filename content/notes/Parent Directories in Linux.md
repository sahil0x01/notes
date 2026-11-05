---
title: Parent Directories in Linux
type: note
description:
tags:
  - linux
publish: true
---
The [`cd` command](https://www.gnu.org/software/bash/manual/html_node/Bourne-Shell-Builtins.html#index-cd) "changes directory" to move _into_ a directory. But how do you move back _out_ of the current directory?

The answer is two dots: `..`

`..` is a special alias that refers to "the parent directory." It's a shortcut that you can use to move up one level in the directory tree.

If you chain multiple `..` segments together:

```sh
cd ../..
```

Then you will move up that many directories [in](https://www.boot.dev/lessons/78334093-2660-49b1-9a5b-7a61d79ef6b4#:~:text=The,directories) [[Learn Linux]]
