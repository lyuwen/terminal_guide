# Shell Programming

Speaking of shell programming, one would always comes across commands that they never used before.
It is a good habit to first try
```bash
man COMMAND
```
to open the manpage or use
```bash
COMMAND --help
```
to print out the help text and learn how to use them at first, though these methods may not always work, or provide intuitive instructions.


## BASH on different platforms


## Variables

There are ordinary runtime variables and environment variables in the BASH, one can also define envrionment variables in the bashrc file.

In BASH, to get the value of a variable, one could use `${VARIABLE}` or sometimes `$VARIABLE` when this form would not be misleading to shell. In the formmer formular, one can also perform substitutions of the values: 

* `${VARIABLE/pattern/substitution}` for substituting the first pattern found in the variable.
* `${VARIABLE//pattern/substitution}` for substituting all patterns found in the variable.

There are also several system defined variables that would be very helpful to shell usage and programming.

* `~`: the home directory of the current user, the same as `${HOME}`.
* `$?`: the return code of the last command.
* `!$`: the last argument of the last command.
* `${PWD}`: current working directory.
* `${PATH}`: the searching path for commands.
* `${PYTHONPATH}`: the searching path for python modules.

The following are often used in shell scripts:

* `$0`: the zeroth argument, a.k.a. the name of the script.
* `$1`: the first argument.
* `${@}`: a list all arguments not including the zeroth.
* `${#}`: the number of arguments not including the zeroth.

## Subsections

* [Programming](programming.md): Condition and loops, piping, etc.
* [Remote access](remote_access.md): SSH.
* [Building system](build_system.md): Building system such as `make` and `scons`.

## Commands

Here we will cover the commands and their features I use the most:

* [directory commands](#directory-commands): `cd`, `mkdir`
* [copying and moving files](#copying-and-moving-files): 
    `cp`, `mv`. Remote copying/syncing will be discussed in [Remote access](remote_access.md).
* [sed](#sed)
* [grep](#grep)
* [awk](#awk)


### directory commands

### copying and moving files

### sed

### grep

### awk



---
[←](../README.md) • [↑](#shell-programmins) • [Github](https://github.com/lyuwen/terminal_guide)

Copyright (C) 2018 by Lyuwen Fu
