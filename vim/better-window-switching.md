# Better Window Switching

For a long time I had these lines in my `.vimrc`

```
nnoremap <leader>s :sp<CR>
nnoremap <leader>v :vsp<CR>
```

But then I read [this
article](http://stevelosh.com/blog/2010/09/coming-home-to-vim/#important-vimrc-lines)
and swiped the better:

```
nnoremap <leader>v <C-w>v<C-w>l
nnoremap <leader>s <C-w>s<C-w>j
```

This way, opening a new split automatically bumps your cursor to the new split.
