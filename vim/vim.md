# Vim

Since I am a vim user, the text editor I will be introducing is vim.

[Vim](https://en.wikipedia.org/wiki/Vim_(text_editor)), one of the most acient and yet popular text editor in the world, which is also one of the two initial members of the [Editor war](https://en.wikipedia.org/wiki/Editor_war). Both of them are almost always available by default with MacOS or a linux system, which enables one to perform text editing on virtually anywhere.

## Upon entering

To enter the vim from bash, simply type:
```bash
vim
```
or
```bash
vi
```
and hit Enter.

In old time vim is the improved version of vi, and would have more features and extendabilities. But now they are basically the same program.

Once I heard of a joke saying that somebody was using vim for a indefinite long time only because he did not know how to quit the program. So I will introduce the way to quit vim at the very beginning.

In the simplest case:
```vim
:q<CR>
``` 
or 
```vim
:quit<CR>
``` 
(`<CR>` here stands for Enter, it will be used through out the entire vim tutorial. As well as, the 
`<C-[key]>` stands for `control + [key]`, and  `<C-S-[key]>` stands for `control + shift + [key]`.
For `:` commands, `<CR>` at end will be omitted.)
would do the job, but when you have accidently modified the file, it would not quit, one could append a `!` sign to the above commands to quit the program and discard the changes:
```vim
:q!
```
. But to exit the program with changes saved, one has many options:
```
:wq
```
,
```
:x
```
or simply press `ZZ` in the [normal mode](#normal-mode).

## User Interface

The user interface of vim consist of the following part from the top to bottom:

* tab line: a line that display tabs when it's available.
* buffer: the area to display the text under editing.
* status line: a line that display many information of the document including the mode.
* command line: the line that will show the command you are typing during `:` command, search, etc.

## Normal mode

Vim as three modes: Normal mode, Insert mode, Visual mode

When you open vim for an empty buffer or a file, you would always enter the normal mode.
This is where you type commands and do all the editing, while the [Insert mode](#insert-mode) is mojarly for typing in texts. The idea is that one do all the editing here and type in the Inser mode.

The original navigation key in vim is h, j, k, l, for left, up, down and right, due to the design of the machine where it was originally developed. But now one can also acheive this with the arrow keys. Such acient convention is kept for minimum hand movement.

The basic commands are (unless specified, these commands do not ):

* mode switching
    * esc: go back to Normal mode.
    * i: enter [Insert mode](#insert-mode) at current curser position.
    * v: enter [Visual mode](#visual-mode) at current curser position.
    * a: enter [Insert mode](#insert-mode) at the position behind the current curser.
    * A: enter [Insert mode](#insert-mode) at the end of line.
    * I: enter [Insert mode](#insert-mode) at the beginning of line, it will skip the front whit spaces.
    * o: add a new line after the curser and enter Insert mode.
    * O: add a new line before the curser and enter Insert mode.

* navigation
    * 0: go to (move curser to) the beginning of the line.
    * $: go to the end of line.
    * G: go to the end of file.
    * gg: go to the beginning of file.
    * w: go to the beginning of the next word unit (word to word, word to symbol, symbol to word, etc.).
    * W: go to the beginning of the next word seperated by space.
    * e: go to the end of the next word unit.
    * E: go to the end of the next word seperated by space.
    * b: reverse of e.
    * B: reverse of E.

* Undo and redo
    * u: undo.
    * `<C-u>`: redo.

* Searching and replacing
    * %: go to the conterpart of parenthese or bracket.
    * #: search backward for the exact match without any adjacent alphabetical charactors.
    * /: enter searching mode, with forward searching.
    * ?: enter searching mode, with backward searching.
    * `:s`: search and replace, will be explain in an independent section since it can get very complicated.


* text manipulation
    * r: replace a charactor.
    * R: Enter a replace mode that one could continuously replace the contents in the buffer.
    * s: delete the charactor at the current curser poistion and enter Insert mode.
    * ~: toggle upper/lower case of the charactor at the curser position.

* cut, copy, pasting
    * dd: delete a line and store the line in the vim clipboard.
    * yy: yank a line (copy in vim).
    * p: paste the content from clipboard after the curser.
    * P: paste the content from clipboard before the curser.


## Insert mode

This is where you type in stuff as in all other editors.

Though there are still features like templates and autocompletions (shortcut `<C-n>`), etc in this mode.


## Visual mode

Visual mode is the selection mode in vim, one can enter from normal mode.

There are different type of visual modes:

* v: normal visual mode.
* V/`<S-v>`: line visual mode.
* `<C-v>`: block visual mode, this mode gives you more flexibility to edit texts, such as adding text the multple lines at the same position.