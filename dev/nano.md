# Nano Commands

## Overview
- [Nano Commands](#nano-commands)
  - [Overview](#overview)
  - [Opening a File](#opening-a-file)
  - [Inserting Text](#inserting-text)
  - [Saving and Quitting](#saving-and-quitting)
  - [Navigating in Nano](#navigating-in-nano)
  - [Copying, Cutting, and Pasting](#copying-cutting-and-pasting)
  - [Undoing and Redoing Changes](#undoing-and-redoing-changes)
  - [Searching and Replacing](#searching-and-replacing)
  - [Configuring Nano](#configuring-nano)
  - [Using Help](#using-help)

## Opening a File

To open a file in Nano.

```sh
nano file-name
```

Replace `file-name` with the name of the file you want to open.

## Inserting Text

To start inserting text, simply start typing after opening the file.

## Saving and Quitting

To save changes.

```sh
^O (Control + O)
```

To quit Nano.

```sh
^X (Control + X)
```

To save changes and quit.

```sh
^X (Control + X), then Y, then Return
```

## Navigating in Nano

To move the cursor up, down, left, or right.

```sh
^P (Control + P) - up
^N (Control + N) - down
^B (Control + B) - left
^F (Control + F) - right
```

To move to the beginning of the line.

```sh
^A (Control + A)
```

To move to the end of the line.

```sh
^E (Control + E)
```

## Copying, Cutting, and Pasting

To cut a line.

```sh
^K (Control + K)
```

To uncut (paste) a line.

```sh
^U (Control + U)
```

To copy text.

1. Set the mark at the beginning of the text to be copied using `^6 (Control + Shift + 6)`.
2. Move the cursor to the end of the text.
3. Cut the marked text using `^K (Control + K)`.
4. Immediately uncut (paste) the text using `^U (Control + U)` to copy it.

## Undoing and Redoing Changes

To undo the last action.

```sh
M-U (Option + U)
```

To redo the last undone action.

```sh
M-E (Option + E)
```

## Searching and Replacing

To search for a pattern.

```sh
^W (Control + W)
```

To search and replace.

```sh
^\\ (Control + \\)
```

## Configuring Nano

To open the Nano configuration file.

```sh
nano ~/.nanorc
```

To enable line numbers, add the following line to the configuration file.

```sh
set linenumbers
```

To enable syntax highlighting, add syntax definitions to the configuration file.

## Using Help

To open the help documentation.

```sh
^G (Control + G)
```