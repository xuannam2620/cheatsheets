# Global
`:help keyword` - open help for keyword  
`:o file` - open file  
`:saveas file` - save file as  
`:close` - close current pane  
`K` - open man page for word under the cursor  

### Cursor movement  
`h` - move cursor left  
`j` - move cursor down  
`k` - move cursor up  
`l` - move cursor right  
`H` - move to top of screen  
`M` - move to middle of screen  
`L` - move to bottom of screen  
`w` - jump forwards to the start of a word  
`W` - jump forwards to the start of a word (words can contain punctuation)  
`e` - jump forwards to the end of a word  
`E` - jump forwards to the end of a word (words can contain punctuation)  
`b` - jump backwards to the start of a word  
`B` - jump backwards to the start of a word (words can contain punctuation)  
`%` - move to matching character (default supported pairs: '()', '{}', '[]' - use :h matchpairs in vim for more info)  
`0` - jump to the start of the line  
`^` - jump to the first non-blank character of the line  
`$` - jump to the end of the line  
`g_` - jump to the last non-blank character of the line  
`gg` - go to the first line of the document  
`G` - go to the last line of the document  
`5G` - go to line 5  
`fx` - jump to next occurrence of character x  
`tx` - jump to before next occurrence of character x  
`Fx` - jump to previous occurence of character x  
`Tx` - jump to after previous occurence of character x  
`;` - repeat previous f, t, F or T movement  
`,` - repeat previous f, t, F or T movement, backwards  
`}` - jump to next paragraph (or function/block, when editing code)  
`{` - jump to previous paragraph (or function/block, when editing code)  
`zz` - center cursor on screen  
`Ctrl + b` - move back one full screen  
`Ctrl + f` - move forward one full screen  
`Ctrl + d` - move forward 1/2 a screen  
`Ctrl + u` - move back 1/2 a screen  

### Insert mode - inserting/appending text  
`i` - insert before the cursor  
`I` - insert at the beginning of the line  
`a` - insert (append) after the cursor  
`A` - insert (append) at the end of the line  
`o` - append (open) a new line below the current line  
`O` - append (open) a new line above the current line  
`ea` - insert (append) at the end of the word  
`Esc` - exit insert mode  

### Working with multiple files  
`:e` file - edit a file in a new buffer  
`:bnext` or `:bn` - go to the next buffer  
`:bprev` or `:bp` - go to the previous buffer  
`:bd` - delete a buffer (close a file)  
`:ls` - list all open buffers  
`:sp file` - open a file in a new buffer and split window  
`:vsp file` - open a file in a new buffer and vertically split window  
`Ctrl + ws` - split window  
`Ctrl + ww` - switch windows  
`Ctrl + wq` - quit a window  
`Ctrl + wv` - split window vertically  
`Ctrl + wh` - move cursor to the left window (vertical split)  
`Ctrl + wl` - move cursor to the right window (vertical split)  
`Ctrl + wj` - move cursor to the window below (horizontal split)  
`Ctrl + wk` - move cursor to the window above (horizontal split)  
