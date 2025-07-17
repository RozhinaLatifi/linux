VIM has 2 mode 
1- Command mode 
2- Insert mode 

```
i => insert
escape => back to command mode 
```

# Vim Cheat Sheet

## Modes
- `i` – enter Insert mode  
- `Esc` – return to Normal mode  
- `v` – start Visual mode  
- `V` – start Visual Line mode  
- `Ctrl+v` – start Visual Block mode  
- `:` – enter Command-line mode  

## Navigation
- `h` – move left  
- `l` – move right  
- `j` – move down  
- `k` – move up  
- `w` – jump to start of next word  
- `b` – jump to start of previous word  
- `e` – jump to end of word  
- `0` – jump to beginning of line  
- `^` – jump to first non-blank character  
- `$` – jump to end of line  
- `gg` – jump to start of file  
- `G` – jump to end of file  
- `nG` – jump to line `n`  
- `Ctrl+d` – scroll down half page  
- `Ctrl+u` – scroll up half page  

## Editing
- `x` – delete character under cursor  
- `dd` – delete current line  
- `dw` – delete word  
- `D` – delete from cursor to end of line  
- `u` – undo  
- `Ctrl+r` – redo  
- `yy` – yank (copy) line  
- `p` – paste after cursor  
- `P` – paste before cursor  
- `r<char>` – replace character with `<char>`  
- `cw` – change word  
- `C` – change to end of line  
- `.` – repeat last change  

## Search
- `/pattern` – search forward for pattern  
- `?pattern` – search backward for pattern  
- `n` – repeat search in same direction  
- `N` – repeat search in opposite direction  

## Files
- `:w` – save file  
- `:q` – quit  
- `:wq` – save and quit  
- `:q!` – quit without saving  
- `:e filename` – open file  
- `:bn` – go to next buffer  
- `:bp` – go to previous buffer  
- `:bd` – close buffer  

## Windows (Splits)
- `:split` or `:sp` – horizontal split  
- `:vsplit` or `:vsp` – vertical split  
- `Ctrl+w` + `h/j/k/l` – move between windows  
- `Ctrl+w` + `q` – close current window  
- `Ctrl+w` + `=` – equalize split sizes  

## Marks and Registers
- `m<char>` – mark current position as `<char>`  
- `'a` – jump to line of mark `a`  
- `` `a `` – jump to exact position of mark `a`  
- `"*p` – paste from system clipboard (if supported)  

## Macros
- `q<char>` – start recording macro into register `<char>`  
- `q` – stop recording  
- `@<char>` – play macro  
- `@@` – repeat last macro  

## Misc
- `:help` – open help  
- `:noh` – clear search highlighting  
- `:%s/old/new/g` – replace all `old` with `new` in file  
