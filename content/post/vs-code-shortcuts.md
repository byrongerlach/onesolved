---
title: "Visual Studio Code Keyboard Shortcuts"
date: 2017-07-22T15:31:32-07:00
tags: ["VS Code", "keyboard shortcuts"]
categories: ["commands and shortcuts"]
draft: false
---

## My Commonly-Used Shortcuts

Shortcut | Description
---------|------------
Ctrl + K + S | List all shortcuts
Alt + &#8679;| Move line up. 
Alt + Shift + &#8679;| Copy above.
Ctrl + Shift + L | Put multi-cursor at all occurences of current selections 
Ctrl + C/X | Copy/Cut line
Ctrl + Shift + K | Delete line
Ctrl + (Shift) + Enter | Insert line (above) or below
Ctrl + (K) + Shift + [/] | Fold/Unfold (sub) region
Ctrl + Shift + E | Focus on file explorer
Ctrl + ` | Focus on Terminal
Alt + z | Toggle word-wrap

## My Keybindings.json File
```
{ "key": "ctrl+`", "command": "workbench.action.focusActiveEditorGroup", "when": "terminalFocus" },
{ "key": "ctrl+`", "command": "workbench.action.terminal.focus", "when": "!terminalFocus" }
```