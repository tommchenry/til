# Delete Whitespaces At End of Lines

To get rid of all those stray whitespaces at the end of lines in Vim:

`:%s/\s\+$//`

## Bonus Points

Update your `~/.vimrc` to include:

`nnoremap <leader>W :%s/\s\+$//<cr>:let @/=''<CR>`

Now you never have to remember the damn string, just hit `leader` + `W`.
