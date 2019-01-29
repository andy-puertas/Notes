### Vim Notes

*****

#### Vim

3 Basic Modes :

* ***Insert*** 
    * `I` Key
    * normal text Editor
* ***Normal*** Mode
    * `Esc` key
    * navigation and manipulation of text
* Visual Mode
    * `v` key
    * you select text with movement keys before you decide what to do with it.
*****
#### Movement

##### Cursor Movement
`h`, `j`, `k`, `l` move the cursor
* `h` moves the cursor left <-- 
* `j` moves cursor down 
* `k` moves cursor up
* `l*` moves cursor right


##### Word Movement
`w`, `b`, `e`, moves around by words

* `w` moves to the *start* of the next word
* `e` moves to the *end* of the word
* `b` moves to the *beginning* of the word

##### Numbers and Movement

* Pressing `3w` is the same as pressing w three times.
* `30i- Esc` would type out - 30 times

##### Find

to find and move to the next or previous ocurrence of a character, use `f` and `F` 
* `fo` find the next o
* you can combine with numbers.  `3fq`
* can also be used with brackets and parentheses I think?
##### Goto

* beginning of a line, `0`
* end of a line `$`
* `gg` takes you to the beginning of the file
* `G` takes you to the end
* `line number` along with `G` takes you to specific line
*
##### Find Word

* find next occurence of word under cursor with `*` and previous with `#`

##### Search
* `/` followed by what you want to find
* repeat search for next and previous `n`, `N`

##### Insert New Line
* press `o` or `O` to insert text into new line

##### Removing Characters
* `x` removes under cursor
* `X` removes to the left
* `r` replaces one character without changing to insert mode.

##### Deleting
* `d` is the delete command
* combine with movement `dw` deletes first word to the right
* it also copies, so you can paste with `p`.

##### Repetition

* `.` repeats the previous comamand

##### Real Vim
* `:w` saves
* `:q` quits
* `:q!` quit without saving
* `u` for undo
* `ctrl` `R` for redo
* `:help` for some help

***

##### Extras and Customization

* colors can be found in `/usr/share/vim/`
* here is the current set up of my `.vimrc` file which is inside `~/.vimrc`

'set expandtab
set tabstop=4
set softtabstop=4
set shiftwidth=4
set autoindent
set textwidth=80
colorscheme darkblue
au InsertLeave * colorscheme darkblue
au InsertEnter * colorscheme molokai`
