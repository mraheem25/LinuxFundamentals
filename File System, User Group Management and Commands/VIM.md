# VIM - Vi IMproved 

Vim is a text editor

Similar to the echo command, it creates a file if the file doesn't exist (`vim file.txt`) 

#### 3 modes of VIM
  - Command mode (what you first enter into)
  - Insert mode (used for editing files and writing scripts). To enter, press i from command mode. Press esc to re enter command mode
  - Visual mode (used for selecting text). To enter, press v from command mode. Press esc to re enter command mode

### Navigating VIM in command mode
  - `:wq!` - force save and quit, where w = write, q = quit and ! = force. Note, :w just saves and :q quits without saving
  - `k` - move up (Can also use arrow key)
  - `j` - move down (Can also use arrow key)
  - `h` - move left (Can also use arrow key)
  - `l` - move right (Can also use arrow key)
  - `0` - move to beginning of line
  - `shift+4` (Mac) or * - move to end of line
  - `W` - move forward by a word
  - `B` - move back by a word
  - `:x` - move to line x
  - `/word` - search for word. If multiple occurrences, use `n` for next occurrence and `N` for previous occurrence
  - `D` - Delete part of a line, `dd` - delete a whole line
  - `yy` - yank/copy and `p` - paste
  - `u` - undo and `ctrl+r` - redo
  - `:set number` - to number line and `:set nonumber` to turn off
  - `:syntax on` - syntax highlighting

