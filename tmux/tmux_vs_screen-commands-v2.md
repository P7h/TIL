# tmux vs. screen commands

| **Action** | **tmux** | **screen** |
|---|---|---|
| start a new session | <kbd>tmux</kbd><br><kbd>tmux new</kbd><br><kbd>tmux new-session</kbd>	| <kbd>screen</kbd> | 
| start a new session with a name | <kbd>tmux new -s name</kbd> | <kbd>screen -S name</kbd> |
| re-attach a detached session | <kbd>tmux attach</kbd><br><kbd>tmux attach-session</kbd> | <kbd>screen -r</kbd> |
| re-attach a detached session with a name | <kbd>tmux attach -t name</kbd><br><kbd>tmux a -t name</kbd> | <kbd>screen -r name</kbd> |
| re-attach an attached session (detaching it from elsewhere) | <kbd>tmux attach -d</kbd><br><kbd>tmux attach-session -d</kbd> | <kbd>screen -dr</kbd> |
| re-attach an attached session (keeping it attached elsewhere) | <kbd>tmux attach</kbd><br><kbd>tmux attach-session</kbd> | <kbd>screen -x</kbd> |
| detach from currently attached session | <kbd>^b</kbd> <kbd>d</kbd><br><kbd>^b</kbd> <kbd>:detach</kbd> | <kbd>^a</kbd> <kbd>^d</kbd> |
| rename-window to newname | <kbd>^b</kbd> <kbd>,</kbd><br><kbd>^b</kbd> <kbd>:rename-window <newname></kbd> | <kbd>^a</kbd> <kbd>A</kbd> <kbd>newname</kbd> |
| list windows | <kbd>^b</kbd> <kbd>w</kbd> | <kbd>^a</kbd> <kbd>w</kbd> |
| list windows in chooseable menu | | <kbd>^a</kbd> <kbd>"</kbd> |
| go to window # | <kbd>^b</kbd> <kbd>#</kbd> | <kbd>^a</kbd> <kbd>#</kbd> |
| go to last-active window | <kbd>^b</kbd> <kbd>l</kbd> | <kbd>^a</kbd> <kbd>l</kbd> |
| go to next window | <kbd>^b</kbd> <kbd>n</kbd> | <kbd>^a</kbd> <kbd>n</kbd> |
| go to previous window | <kbd>^b</kbd> <kbd>p</kbd> | <kbd>^a</kbd> <kbd>p</kbd> |
| see keybindings | <kbd>^b</kbd> <kbd>?</kbd> | <kbd>^a</kbd> <kbd>?</kbd> |
| list sessions | <kbd>^b</kbd> <kbd>s</kbd><br><kbd>tmux ls</kbd><br><kbd>tmux list-sessions</kbd> | <kbd>screen -ls</kbd> |
| toggle visual bell | | <kbd>^a</kbd> <kbd>^g</kbd> |
| kill the current pane | <kbd>^b</kbd> <kbd>x</kbd><br><kbd>logout</kbd><br><kbd>^D</kbd> | <kbd>^a</kbd> <kbd>X</kbd> |
| destroy the current window | <kbd>^b</kbd> <kbd>&</kbd> | <kbd>^a</kbd> <kbd>k</kbd><br><kbd>^a</kbd> <kbd>^k</kbd> |
| exit current shell | <kbd>^d</kbd> | <kbd>^d</kbd> |
| create another window | <kbd>^b</kbd> <kbd>c</kbd> | <kbd>^a</kbd> <kbd>c</kbd> |
| switch to another pane | <kbd>^b</kbd> <kbd>o</kbd> | <kbd>^a</kbd> <kbd>Tab</kbd> |
| split pane horizontally | <kbd>^b</kbd> <kbd>"</kbd> | <kbd>^a</kbd> <kbd>S</kbd><br>then <kbd>^a</kbd> <kbd>Tab</kbd><br>and <kbd>^a</kbd> <kbd>c</kbd> |
| split pane vertically | <kbd>^b</kbd> <kbd>%</kbd> | <kbd>^a</kbd> <kbd>\|</kbd><br>then <kbd>^a</kbd> <kbd>Tab</kbd><br>and <kbd>^a</kbd> <kbd>c</kbd> |
| close other panes except the current one | <kbd>^b</kbd> <kbd>!</kbd> | |
| swap location of panes | <kbd>^b</kbd> <kbd>^o</kbd> | |
| re-arrange current panes within same window (different layouts)	| <kbd>^a</kbd> <kbd>space</kbd> | |
| show time | <kbd>^b</kbd> <kbd>t</kbd> | |
| show numeric values of panes | <kbd>^b</kbd> <kbd>q</kbd> | |
| enable scroll / view scrollback | <kbd>^b</kbd> <kbd>[</kbd><br>(and to exit <kbd>q</kbd>) | <kbd>^a</kbd> <kbd>[</kbd><br>(and to exit <kbd>q</kbd>) |
| copy text in one view | | <kbd>^a</kbd> <kbd>[</kbd> <kbd>^m</kbd><br>(highlight text and <kbd>enter</kbd>)<br>(to save: <kbd>^a</kbd> <kbd>></kbd>) |
| paste text into a view | | <kbd>^a</kbd> <kbd>]</kbd> |

### Other useful references
Extended from [tmux & screen cheat-sheet](http://www.dayid.org/comp/tm.html).

#### tmux
 * tmux shortcuts & cheatsheet: [https://gist.github.com/MohamedAlaa/2961058](https://gist.github.com/MohamedAlaa/2961058)
 * Book &raquo; "tmux: Productive Mouse-Free Development" 1st Ed: [https://www.amazon.com/tmux-Productive-Development-Brian-Hogan/dp/1934356964](https://www.amazon.com/tmux-Productive-Development-Brian-Hogan/dp/1934356964)

#### screen
 * Screen cheatsheet: [http://www.catonmat.net/download/screen.cheat.sheet.pdf](http://www.catonmat.net/download/screen.cheat.sheet.pdf)
 * Screen reference: [http://aperiodic.net/screen/quick_reference](http://aperiodic.net/screen/quick_reference)
 * Book &raquo; "GNU Screen: The virtual terminal manager" 1st Ed: [https://www.amazon.com/GNU-Screen-virtual-terminal-manager/dp/9888381393](https://www.amazon.com/GNU-Screen-virtual-terminal-manager/dp/9888381393)