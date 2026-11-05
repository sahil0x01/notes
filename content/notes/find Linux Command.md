---
title: find Linux Command
type: note
description:
tags:
  - linux
publish: true
---
The [`find` command](https://www.gnu.org/software/findutils/) is a powerful tool for finding files and directories by name, not by their contents [in](https://www.boot.dev/lessons/0c4cbaad-aaa3-4e45-95aa-fb2445d50345#:~:text=The,chad%2A%22) [[Learn Linux]]

## Find a File by Name

Let's say you're looking for a file named `hello.txt` somewhere in your home directory. You can use the `find` command to search for exactly that title:

```sh
find some_directory -name hello.txt
```

## Pattern Search

The `find` command can also search for files that match a pattern. For example, if you wanted to find all files that end in `.txt`, you could run:

```sh
find some_directory -name "*.txt"
```

The `*` character is a wildcard that matches anything. If you're trying to find filenames that _contain_ a specific word, you can use the `*` character to match the rest of the filename:

```sh
# Find all filenames that contain the word "chad"
find some_directory -name "*chad*"
```