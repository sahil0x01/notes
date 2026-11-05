---
title: head and tail Linux Command
type: note
description:
tags:
  - linux
publish: true
---
Sometimes you don't want to print _everything_ in a file. Files can be really big after all.

## `head` Command
The [head](https://www.ibm.com/docs/en/aix/7.3?topic=h-head-command) command prints the first `n` lines of a file. The `-n` flag specifies `n` as shown:

```sh
head -n 10 file1.txt
```

If you don't specify a number using the `-n` flag, it will default to `10` [in](https://www.boot.dev/lessons/96b5e0ce-37f8-44c2-b219-ebdae3655f23#:~:text=Command-,The,10%2E) [[Learn Linux]]
## `tail` Command
The [tail](https://www.ibm.com/docs/en/aix/7.3?topic=t-tail-command) command prints the _last_ `n` lines of a file. The `-n` flag specifies `n` as shown [in](https://www.boot.dev/lessons/96b5e0ce-37f8-44c2-b219-ebdae3655f23#:~:text=Command-,The%20tail,txt) [[Learn Linux]] :

```sh
tail -n 10 file1.txt
```
	