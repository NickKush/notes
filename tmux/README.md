# Tmux

**Tmux** - is an terminal multiplexer for `unix` operating systems.

#### [*Documentation*](https://github.com/tmux/tmux/wiki)

---

## Table of content

* [Terminal commands](#terminal-commands)
* [Cheet sheet](#cheet-sheet)
* [Commands](#commands)

---

## Terminal commands

- `tmux`, `tmux new` - start a new session
- `tmux ls` - list of all sessions
- `tmux a` - attach to last session
- `tmux a -t <value>` - attach to a session with name/index *value*

---

## Cheet sheet

*using my [configuration](https://github.com/NickKush/dotfiles/blob/master/config/tmux/.tmux.conf)*

`Ctrl + a` - "leader" key.

**Windows**:
- `<leader> c` - create window
- `<leader> ,` - rename window
- `<leader> &` - close window

- `<leader> 1..9` - switch window by number
- `<leader> p` - move to previous window
- `<leader> n` - move to next window
- `<leader> l` - move to previous selected window


**Panes**:
- `<leader> %` - create vertical pane
- `<leader> "` - create horizontal pane
- `<leader> x` - close pane

- `<leader> <arrow_keys>` - switch between panes
- `<leader> Ctrl+<arrow_keys>` - change size of the selected pane


**Sessions**
- `<leader> s` - list of all sessions
- `<leader> w` - list of all sessions and window previews

- `<leader> $` - rename session
- `<leader> d` - detatch from session

- `<leader> (` - move to previous session
- `<leader> )` - move to next session


**Others**
- `<leader> :` - enter command mode

## Commands

TODO
