# Vim Commands

## Overview
- [Vim Commands](#vim-commands)
  - [Overview](#overview)
  - [Opening a File](#opening-a-file)
  - [Inserting Text](#inserting-text)
  - [Saving and Quitting](#saving-and-quitting)
  - [Navigating in Vim](#navigating-in-vim)
  - [Copying, Cutting, and Pasting](#copying-cutting-and-pasting)
  - [Undoing and Redoing Changes](#undoing-and-redoing-changes)
  - [Searching and Replacing](#searching-and-replacing)
  - [Working with Multiple Files](#working-with-multiple-files)
  - [Configuring Vim](#configuring-vim)
  - [Using Visual Mode](#using-visual-mode)

## Opening a File

To open a file in Vim.

```sh
vim file-name
```

Replace `file-name` with the name of the file you want to open.

## Inserting Text

To enter insert mode and start inserting text.

```sh
i
```

To enter insert mode at the end of the line.

```sh
A
```

## Saving and Quitting

To save changes and quit Vim.

```sh
:wq
```

To quit without saving changes.

```sh
:q!
```

To save changes without quitting.

```sh
:w
```

## Navigating in Vim

To move the cursor up, down, left, or right.

```sh
k - up
j - down
h - left
l - right
```

To move to the beginning of the line.

```sh
0
```

To move to the end of the line.

```sh
$
```

## Copying, Cutting, and Pasting

To copy (yank) a line.

```sh
yy
```

To cut (delete) a line.

```sh
dd
```

To paste the copied or cut content.

```sh
p
```

## Undoing and Redoing Changes

To undo the last change.

```sh
u
```

To redo the undone change.

```sh
Ctrl + r
```

## Searching and Replacing

To search for a pattern.

```sh
/pattern
```

To search and replace within the entire file.

```sh
:%s/old/new/g
```

Replace `pattern`, `old`, and `new` with the respective search pattern and replacement text.

## Working with Multiple Files

To open multiple files in tabs.

```sh
vim -p file1 file2
```

To switch to the next tab.

```sh
:tabnext
```

To switch to the previous tab.

```sh
:tabprev
```

## Configuring Vim

To open the Vim configuration file.

```sh
vim ~/.vimrc
```

To set line numbers.

```sh
:set number
```

To enable syntax highlighting.

```sh
:syntax on
```

## Using Visual Mode

To enter visual mode.

```sh
v
```

To enter visual line mode.

```sh
V
```

To enter visual block mode.

```sh
cmd + v
```

In visual mode, you can select text and perform operations like copying, cutting, and pasting.