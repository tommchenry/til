# Sessions

I've been using windows as the top-level of tmux navigation, but there are also sessions. Sessions are complete instances of tmux that you're visiting as a client -- if your connection is interrupted, you can always return to them so long as the session isn't killed.

To start a new session, invoke it in the command line as:

```
tmux new -s session_name
```

To attach to an existing session you already created:

```
tmux a -t session_name
```

To list all the existing sessions:

```
tmux ls
```

To detach from the current session:

```
tmux detach
```

To rename the current session:

`prefix key` + `$`
