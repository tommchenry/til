# Add Vim Pane Switching

It's really annoying when you're learning to get Tmux and Vim working together
when you try to switch from a Vim pane to Tmux and have to switch contexts for
which hotkeys to push. This simplifies everything so a `Control` + `j` moves you
down, rather that's into a Vim split or a Tmux pane, doesn't matter.

[Add this plugin to your Vim
plugins](https://github.com/christoomey/vim-tmux-navigator)

Then add this to your `tmux.conf`

```
is_vim='echo "#{pane_current_command}" | grep -iqE "(^|\/)g?(view|n?vim?x?)(diff)?$"'
bind -n C-h if-shell "$is_vim" "send-keys C-h" "select-pane -L"
bind -n C-j if-shell "$is_vim" "send-keys C-j" "select-pane -D"
bind -n C-k if-shell "$is_vim" "send-keys C-k" "select-pane -U"
bind -n C-l if-shell "$is_vim" "send-keys C-l" "select-pane -R"
bind -n C-\ if-shell "$is_vim" "send-keys C-\\" "select-pane -l"
```

Don't do what I did and add the plugin and then read a number of articles that
refer to an outdated version so their `tmux.conf` lines don't actually do
anything.

PS: The correct `tmux.conf` lines are in the `vim-tmux-navigator` README as well.
