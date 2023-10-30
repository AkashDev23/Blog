---
title: "Getting started with vi editor"
datePublished: Mon Oct 30 2023 08:51:09 GMT+0000 (Coordinated Universal Time)
cuid: clocnuh68000u09mjfaiday7d
slug: getting-started-with-vi-editor
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/xbEVM6oJ1Fs/upload/c0213763758528936bf76f7c9eb2e7a8.jpeg
tags: linux, vi, linux-for-beginners, linux-basics, linux-commands

---

I've been learning Linux for about 2 months now and the main issue I was facing is with the vi editor. vi (visual editor) is the default editor that comes with the UNIX operating system. This editor is not similar to the other editors we use like Notepad, which makes it a challenge to get used to but don't worry; today, I'll be sharing some basic commands that will help you get started with this editor. Vi has a steep learning curve, but once you become proficient, you can achieve a high level of productivity and efficiency in text editing.

## Modes in vi editor

The vi editor essentially has two modes:

1. Command mode (also known as Normal Mode): This is the default mode when we open Vi. In this mode, we can navigate the document, perform various text manipulation tasks, and issue commands. We can move the cursor, copy, paste, delete text, search, etc. To enter this mode, press the **'Esc'** key from another mode, such as Insert Mode.
    
2. Insert Mode: This mode is used for writing and editing text into the document.
    

There are various vi commands that we can use but in this article, I'll be sharing the important ones that I use a lot. You just need to have a little bit of practice to get used to these commands. You have to keep in mind that Vi is case sensitive so don't use capital letters in place of small letters and vice versa.

**To Start Vi:** Type `vi filename` to open a file in the Vi editor.

**To Exit Vi:** To save your changes and exit Vi, use:`wq` followed by pressing Enter or simply `:x` and press Enter. The 'w' stands for saving, while 'q' means quit or exit. If you want to quit Vi without saving the latest changes, use:`q` followed by Enter.

To move the cursor

**Moving the Cursor:**

Unlike other editors, you can't move the cursor using a mouse in Vi. Here are some basic commands to navigate:

| Command | Description |  |
| --- | --- | --- |
| `j`, `<Enter>`, or ↓ |  | Move the cursor down one line. |
| `k` or ↑ | Move the cursor up one line. |  |
| `h`, `<Backspace>`, ← | Move the cursor left one character. |  |
| `l` or `<Space>` | Move the cursor right one character. |  |
| `0` (zero) | Move the cursor to the start of the current line. |  |
| `$` | Move the cursor to the end of the current line. |  |
| `G` | Go to the end of the document. |  |
| `gg` | Go to the beginning of the document. |  |
| `u` | Undo the last action. |  |
| `Ctrl + r` | Redo a change. |  |
| `yy` | Yank (copy) a line. |  |
| `p` | Paste the yanked line. |  |

**Inserting and Adding Text:**

| Command | Description |
| --- | --- |
| `i` | Insert text before the cursor. |
| `I` | Insert text at the beginning of the line. |
| `a` | Append text after the cursor. |
| `A` | Add text at the end of the current line. |
| `o` | Open a new line below the current line and start adding text. |
| `O` | Open a new line above the current line. |

**Changing Text:**

* `r`: Replace a single character under the cursor (no need to press 'Esc' afterward).
    

**Deleting Text:**

| Command | Description |
| --- | --- |
| `x` | Delete the character under the cursor, similar to the backspace key. |
| `Nx` | Delete N characters, starting with the character under the cursor (replace N with the number of characters you want to delete). |
| `dd` | Delete the entire current line. |

Make sure to press 'Esc' to exit insert mode and use these commands in normal mode. You can also consider using the Vim editor, which is an advanced version of Vi, offering additional features.

*Stay In the Loop! 💌 Subscribe to Our Newsletter for Exclusive Tips and Updates. Don't Miss Out on the Latest in Linux and Vi Editor Mastery. Join Now!*