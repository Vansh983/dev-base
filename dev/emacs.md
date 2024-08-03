# Emacs Commands

## Overview
- [Emacs Commands](#emacs-commands)
  - [Overview](#overview)
  - [Introduction](#introduction)
  - [Installing Emacs](#installing-emacs)
  - [Starting Emacs](#starting-emacs)
  - [Opening a File](#opening-a-file)
  - [Saving a File](#saving-a-file)
  - [Closing Emacs](#closing-emacs)
  - [Navigating in Emacs](#navigating-in-emacs)
  - [Copying, Cutting, and Pasting](#copying-cutting-and-pasting)
  - [Searching in Emacs](#searching-in-emacs)
  - [Undoing Changes](#undoing-changes)
  - [Managing Buffers](#managing-buffers)
  - [Customizing Emacs](#customizing-emacs)
  - [Installing Packages](#installing-packages)
  - [Using Emacs Help System](#using-emacs-help-system)

## Introduction

Emacs is a highly customizable and extensible text editor. It is known for its powerful editing capabilities and a vast array of features that can be extended through Emacs Lisp (elisp) programs.

## Installing Emacs

To install Emacs on macOS using Homebrew:

```sh
brew install emacs
```

## Starting Emacs

To start Emacs, simply type:

```sh
emacs
```

To start Emacs in the background:

```sh
emacs &
```

## Opening a File

To open a file in Emacs, use the following command within Emacs:

```emacs
C-x C-f
```

This stands for `Control + x` followed by `Control + f`, then type the file name and press `Enter`.

## Saving a File

To save a file in Emacs:

```emacs
C-x C-s
```

This stands for `Control + x` followed by `Control + s`.

## Closing Emacs

To close Emacs:

```emacs
C-x C-c
```

This stands for `Control + x` followed by `Control + c`.

## Navigating in Emacs

- Move the cursor forward by one character: `C-f`
- Move the cursor backward by one character: `C-b`
- Move the cursor up by one line: `C-p`
- Move the cursor down by one line: `C-n`
- Move to the beginning of the line: `C-a`
- Move to the end of the line: `C-e`
- Move forward by one word: `M-f`
- Move backward by one word: `M-b`
- Move to the beginning of the buffer: `M-<`
- Move to the end of the buffer: `M->`

Note: `M` stands for the `Meta` key, which is often the `Alt` key or `Escape` key on modern keyboards.

## Copying, Cutting, and Pasting

- Set the mark (start selection): `C-<space>`
- Copy the region: `M-w`
- Cut the region: `C-w`
- Paste the last copied or cut text: `C-y`

## Searching in Emacs

- Incremental search forward: `C-s`
- Incremental search backward: `C-r`

To perform a search and replace:

```emacs
M-%
```

This stands for `Meta + %`.

## Undoing Changes

To undo the last change:

```emacs
C-/
```

Alternatively:

```emacs
C-x u
```

## Managing Buffers

- List all buffers: `C-x C-b`
- Switch to another buffer: `C-x b`
- Kill a buffer: `C-x k`

## Customizing Emacs

To customize Emacs, you can edit the `~/.emacs` or `~/.emacs.d/init.el` file. For example, to set the default tab width to 4 spaces, add the following line:

```lisp
(setq-default tab-width 4)
```

## Installing Packages

To install packages in Emacs, you need to initialize the package system and add package repositories in your `~/.emacs` or `~/.emacs.d/init.el` file:

```lisp
(require 'package)
(setq package-archives '(("melpa" . "https://melpa.org/packages/")
                         ("gnu" . "https://elpa.gnu.org/packages/")))
(package-initialize)
```

To install a package (e.g., `use-package`):

1. Open Emacs and run the following command:

```emacs
M-x package-refresh-contents
```

2. Then install the package:

```emacs
M-x package-install RET use-package RET
```

## Using Emacs Help System

To access the help system:

- Open the Emacs manual: `C-h r`
- Describe a function: `C-h f`
- Describe a variable: `C-h v`
- Describe a key binding: `C-h k`
- List all key bindings: `C-h b`
