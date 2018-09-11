---
title: "Vim Shortcuts"
date: 2018-07-16T10:37:46-08:00
tags: ["Vim", "keyboard shortcuts"]
categories: ["commands and shortcuts"]
draft: false
---

## My Commonly-Used Shortcuts

### Folding in Vim

Shortcut | Description
---------|------------
zf#j | creates a fold from the cursor down # lines
zf/string | creates a fold from the cursor to string
zj | moves the cursor to the next fold
zk | moves the cursor to the previous fold
zo | opens a fold at the cursor
zO | opens all folds at the cursor
zm | increases the foldlevel by one
zM | closes all open folds
zr | decreases the foldlevel by one
zR | decreases the foldlevel to zero -- all folds will be open
zd | deletes the fold at the cursor
zE | deletes all folds
[z | move to start of open fold
]z | move to end of open fold
zO | opens all folds at the cursor

### Configuration
Shortcut | Description
---------|------------
:vimfiles | Show the loaded vim files (vimrc, etc.).
:so $MYVIMRC | Reload the vimrc

### Navigation
Shortcut | Description
---------|------------
[{       | Jump to beginning of code block
gm 	     | Jump to middle of the screen
w 	     | N words foward
W        | N words forward (blank-separated) 
{/}      | N paragraphs forward/backward 
%      | Goto matching brace 
g<movement> | Move across displayed lines when wrapped
CTRL+^      | Edit alternate file 
e | End of word
0 | First character of line
^ | First non-blank character of line
0 | Last character of line
gm | Middle of line
g0/^/$ | Beginning/non-blank beginning/end of a wrapped line
f/FX | Jump to next, previous character X in a line 
; | Repeat last jump
, | Repeat reverse of last jump
M/H/L | Jump to middle/top/bottom of the screen
CTRL+f/b | Jump forward/backward one screen
CTRL+u/d | Jump forward/backward 1/4 screen
CTRL+e/y | Scroll up/down one line
zt | Scroll line to top of screen
Ng/G | Go to line N
gg/G | First/last line of file
m/M | Make a file or global mark
'X | Go to beginning of line with mark X
`X | Go to line and column of mark X
d'X | Delete to mark X
'0 | Go to the line you were at when you last exited vim
'1-9 | Go to the line you were at when you exited vim the Nth time before
''\``| Go to the beginning/column of the line where you last jumped from
'.\`.| Go to the beginning/column of the last change

### Windows
Shortcut | Description
---------|------------
CTRL-w + s/v | Horizontal/Vertical split
CTRL-w + j/k  | Focus up/down to different windows
CTRL-w + J/K  | Move buffer up/down to different windows
CTRL-w + w | Cycle to a window counter-clockwise
CTRL-w + p | Focus previous window
CTRL-w + o | Make the current window the only one
CTRL-w + r | Rotate windows clockwise
CTRL-w + x | Exchange window with the next one
CTRL-w + t | Move window to new tab 
CTRL-w + c | Close window
CTRL-w + < | Increase vertical window size
CTRL-w + > | Decrease vertical window size
CTRL-w + - | Decrease horizontal window size
CTRL-w + + | Increase horizontal window size
CTRL-w + = | Make windows equal in size
80 CTRL-w + \| | Make window 80 columns

### Buffers
Shortcut | Description
---------|------------
ls       | List buffers
b1       | Goto first buffer
bn/p       | Goto next/previous buffer
bf/l       | Goto first/last buffer
bd       | Delete buffer
ba       | Open window for every buffer
CTRL+^       | Goto last file you edited
\be | Buffer explorer
d | Delete buffer (buffer explorer)

### Editing
Shortcut | Description
---------|------------
i/I       | Insert mode at current position/beginning of the line
a/A       | Insert mode at current position+1/end of the line
o/O | Open new line below/above current line
r | Replace character and return to insert mode
R | Replace current text, and press backspace to restore
c3w | Change 3 words. Changed text is on the unnamed register
x | Delete current character
dd | Delete line
J | Join line
gJ | Join line without adding space
<</>> | Indent/outdent
Ctrl+t/d | Indent/outdent in insert mode
(/)/{/} | Move back/forward one sentence/paragraph
% | Go to matching brace or control structure depending on the language
vit | Visually select the contents of a tag. 'o' will switch the insertion point from the beginning/end
s/./&-/g | Add a dash after every character in the line 
@: | Execute last command
; | Execute last movement (some, like fc) 
; | Repeat latest f, t, F or T [count] times. See |cpo-;|
### Search
Shortcut | Description
---------|------------
g#/#/N/n/*/g* | Matches: prev. partial/prev./next/next current word/next partial match
y?X| Yank text until previous occurence of subject X
:[range]s[ubstitute]/{pattern}/{string}/[flags] [count] | Search over range: c (confirm or skip each match), i/I (ignore case, case sensitive), n (show number of matches), p (print matching lines)
:[range]g[lobal]/{pattern}/cmd | Execute command over range: # (show matches), d (delete lines), y (yank lines)
.,10g/{pattern}/d | Delete matches from cursor and next 10 lines
.,'a+10g/{pattern}/d | Delete matches from mark [a} and next 10 lines
.,'a+10g/{pattern}/# | Show line numbers from mark [a} and next 10 lines
g/X/p | Print all lines matching {X}
v/X/# | Show lines and numbers not matching {X}
:.,'a s/{pattern}/{string} | Search until mark {a}
:g/{subject}/normal O{string} | Add a line containing {string} above each occurrence of {subject}
:noh | Turn off highlighting until the next search
d/{search}/e | Delete until next occurence of {search} inclusive
:g/^$/d | Delete all blank lines
:g/{search}/+ y | Yank line after {search}
Ctrl+r+\ | Paste search pattern in command mode

### Visual Mode
Shortcut | Description
---------|------------
o | Move the other end of the selection

### Visual Mode
Shortcut | Description
---------|------------
o | Move the other end of the selection
