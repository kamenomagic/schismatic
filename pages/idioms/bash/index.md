---
layout: page
title: Bash
---


## Redirecting stdout and stderr [StackOverflow
Issue](https://askubuntu.com/questions/625224/how-to-redirect-stderr-to-a-file)
1. Redirect stdout to one file and stderr to another file:
  * `command > out 2>error`

2. Redirect stdout to a file (>out), and then redirect stderr to stdout (2>&1):
  * `command >out 2>&1`

3. Redirect both to a file (this isn't supported by all shells, bash and zsh support it, for example, but sh and ksh do
not):
    * `command &> out`

