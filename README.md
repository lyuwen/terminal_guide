# A beginner's guide to terminal world

As per request of my friend, I am composing a beginner's guide to the command line interface **Terminal**, and stuff related to it. The main idea is a hands-on booklet that one can refer to while using the terminal. To achieve mastery, one still needs a lot more to learn.

## More

This page will introduce very basic stuff about bash. 
Further knowledge will stay seperate for easy navigation.

* [Vim](vim/vim.md)
* [Shell Programming](shell_programming/shell_programming.md)

## BASH introduction

When opening a terminal, shell is first program begins running and print a `$ ` sign in the screen, waiting for inputs.

Bourne Again SHell (BASH), being one of the most popular shell implementations in the world, is the default shell of MacOS system, as well as many linux distributions. We will introduce the usage of a shell with BASH, preferrably BASH v4+ (note that MacOS is using a 3.0 version of BASH, which would be inconvenient in some way.

To install a 4.0+ version of BASH in MacOS, simply use [Homebrew](https://brew.sh) package manager.
```bash
brew install bash
```
To use this version of BASH as login shell, add `/usr/local/bin/bash` to the file `/etc/shells`, then in `System Preferences > Users & Groups`, change the `login shell` in `Advanced Options`.

## Basics

The most basic commands in the shell are

| Command |                               Meaning                              |
|:-------:|:------------------------------------------------------------------:|
|    cd   |                          change directory                          |
|    ls   |                           list directory                           |
|   pwd   |                       print working directory                      |
|   echo  |                                print                               |
|   cat   |                     concatenate and print files                    |
|   more  |  display content, one full screen at a time, only able to go down  |
|   less  | similar to more, but is able to go backward, and has more features |
|   grep  |                     search for pattern in file                     |
|   sed   |                            stream editor                           |
|   awk   |             a pattern searching and processing language            |
|    rm   |                             remove file                            |
|  touch  |    Create a new file or change the modification time of a file     |
|    wc   |             count words(-w), charactors(-c), lines(-l)             |

And basic shortcuts are

|   Shortcuts  |                           Function                           |
|:------------:|:------------------------------------------------------------:|
|  control + l |                         Clean screen                         |
|  control + u |                 Delete to the beginning line                 |
|  control + w |              Delete to the beginning of the word             |
|  control + a |             Move curser to the beginning of line             |
|  control + e |                Move curser to the end of line                |
|  control + c | Keyboard Interupt, often used to interrupt a running program |
|  control + d |             Exit some programs or ssh connections            |
|  control + z |                   Pause the running process                  |
|  control + r |                    Search command history                    |


___
[↑](#a-beginners-guide-to-terminal-world) • [Github](https://github.com/lyuwen/terminal_guide)
<div style="text-align: right" color=#7B7D7D> Copyright (C) 2018 by Lyuwen Fu </div>