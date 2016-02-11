# tmux vs. screen commands

| **Action** | **tmux** | **screen** |
|---|---|---|
| start a new session | `tmux` OR<br>`tmux new` OR<br>`tmux new-session`	| `screen` | 
| start a new session with a name | `tmux new -s name` | `screen -S name` |
| re-attach a detached session | `tmux attach` OR<br>`tmux attach-session` | `screen -r` |
| re-attach a detached session with a name | `tmux attach -t name` | `screen -r name` |
| re-attach an attached session (detaching it from elsewhere) | `tmux attach -d` OR<br>`tmux attach-session -d` | `screen -dr` |
| re-attach an attached session (keeping it attached elsewhere) | `tmux attach` OR<br>`tmux attach-session` | `screen -x` |
| detach from currently attached session | <kbd>Ctrl + b</kbd> <kbd>d</kbd> OR<br><kbd>Ctrl + b</kbd> `:detach` | <kbd>Ctrl + a</kbd> <kbd>Ctrl + d</kbd> |
| rename-window to newname | <kbd>Ctrl + b</kbd>, <newname> OR <br><kbd>Ctrl + b</kbd> `:rename-window <newname>`| <kbd>Ctrl + a</kbd> <kbd>A</kbd> <newname> |
| list windows | <kbd>Ctrl + b</kbd> <kbd>w</kbd> | <kbd>Ctrl + a</kbd> <kbd>w</kbd> |
| list windows in chooseable menu | | <kbd>Ctrl + a</kbd> <kbd>"</kbd> |
| go to window # | <kbd>Ctrl + b</kbd> <kbd>#</kbd> | <kbd>Ctrl + a</kbd> <kbd>#</kbd> |
| go to last-active window | <kbd>Ctrl + b</kbd> <kbd>l</kbd> | <kbd>Ctrl + a</kbd> <kbd>l</kbd> |
| go to next window | <kbd>Ctrl + b</kbd> <kbd>n</kbd> | <kbd>Ctrl + a</kbd> <kbd>n</kbd> |
| go to previous window | <kbd>Ctrl + b</kbd> <kbd>p</kbd> | <kbd>Ctrl + a</kbd> <kbd>p</kbd> |
| see keybindings | <kbd>Ctrl + b</kbd> <kbd>?</kbd> | <kbd>Ctrl + a</kbd> <kbd>?</kbd> |
| list sessions | <kbd>Ctrl + b</kbd> <kbd>s</kbd> OR<br>`tmux ls` OR<br>`tmux list-sessions` | `screen -ls` |
| toggle visual bell | | <kbd>Ctrl + a</kbd> <kbd>Ctrl + g</kbd> |
| create another shell | <kbd>Ctrl + b</kbd> <kbd>c</kbd> | <kbd>Ctrl + a</kbd> <kbd>c</kbd> |
| exit current shell | <kbd>Ctrl + d</kbd> | <kbd>Ctrl + d</kbd> |
| split pane horizontally | <kbd>Ctrl + b</kbd> <kbd>"</kbd> | |
| split pane vertically | <kbd>Ctrl + b</kbd> <kbd>%</kbd> | |
| switch to another pane | <kbd>Ctrl + b</kbd> <kbd>o</kbd> | |
| kill the current pane | <kbd>Ctrl + b</kbd> <kbd>x</kbd> OR<br>`logout` OR<br><kbd>Ctrl + D</kbd> | |
| close other panes except the current one | <kbd>Ctrl + b</kbd> <kbd>!</kbd> | |
| swap location of panes | <kbd>Ctrl + b</kbd> <kbd>Ctrl + o</kbd> | |
| show time | <kbd>Ctrl + b</kbd> <kbd>t</kbd> | |
| show numeric values of panes | <kbd>Ctrl + b</kbd> <kbd>q</kbd> | |
| enable scroll/view scrollback | <kbd>Ctrl + b</kbd> <kbd>[</kbd> (And to exit <kbd>q</kbd>) | <kbd>Ctrl + a</kbd> <kbd>[</kbd> (And to exit <kbd>q</kbd>) |
| copy text in one view | | <kbd>Ctrl + a</kbd> <kbd>[</kbd> <kbd>Ctrl + m</kbd> (then highlight text and <kbd>enter</kbd>) |
| paste text into a view | | <kbd>Ctrl + a</kbd> <kbd>]</kbd> |