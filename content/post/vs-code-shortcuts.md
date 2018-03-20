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
Ctrl+K V | Markdown side-by-side preview
Collapse all |CTRL + M + O |
Expand all | CTRL + M + L |
Expand all and disable outlining | CTRL + M + P |
Collapse/expand the current section | CTRL + M + M |
Ctrl + P | Find by file name
Ctrl+Shift+[   | Fold (collapse) region  editor.fold
Ctrl+Shift+]   | Unfold (uncollapse) region  editor.unfold
Ctrl+K Ctrl+[  | Fold (collapse) all subregions  editor.foldRecursively
Ctrl+K Ctrl+]  | Unfold (uncollapse) all subregions  editor.unfoldRecursively
Ctrl+K Ctrl+0  | Fold (collapse) all regions editor.foldAll
Ctrl+K Ctrl+J  | Unfold (uncollapse) all regions

## My Keybindings.json File
```
{ "key": "ctrl+`", "command": "workbench.action.focusActiveEditorGroup", "when": "terminalFocus" },
{ "key": "ctrl+`", "command": "workbench.action.terminal.focus", "when": "!terminalFocus" }
```
## Terminal settings in settings.json

```
"terminal.integrated.shell.windows": "C:\\windows\\Sysnative\\WindowsPowerShell\\v1.0\\powershell.exe",
"terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe"
```