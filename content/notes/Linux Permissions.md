---
title: Linux Permissions
type: note
description:
tags:
  - linux
publish: true
---
In a Unix-like operating system, permissions control who can do what to which files and directories. The permissions of an individual file or directory are visually represented as a 10-character string [in](https://www.boot.dev/lessons/23d60fb8-2e90-4861-abde-26d3886722f8#:~:text=In,string) [[Learn Linux]]

```text
drwxrwxrwx
```
Let's break down each character. The first one just tells you whether you're looking at a file or a directory:

- `-`: Regular file (e.g. `-rwxrwxrwx`)
    
- `d`: Directory (e.g. `drwxrwxrwx`)
    

The next 9 characters are broken up into 3 sets of `rwx` and represent the permissions themselves for the "owner," "group," and "others," in order. Each group of 3 represents the permissions for reading, writing, and executing, in order. So, for example:

- `rwx`: All permissions
    
- `rw-`: Read and write, but not execute
    
- `r-x`: Read and execute, but not write
    
- The first 3 characters are "owner" permissions. The "owner" is usually just the user who created the file or directory, but it can be manually changed.
    
- The next 3 characters are "group" permissions. Unix-like systems support groups of users, and each file or directory is assigned to exactly one owning group. Anyone who is not the owner and not a member of that group falls under "others." To be honest, unless you're a system administrator, you won't often worry about groups.
    
- The last 3 characters are "others" permissions. This is everyone else.