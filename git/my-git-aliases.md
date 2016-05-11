# My Git Aliases

From my `~/.bashrc`

```
alias gst='git status'
alias ga='git add'
alias gaa='git add -A'
alias gap='git add -p'
alias gc='git commit -m'
alias gp='git push'
alias glog='git log --oneline --decorate'
alias gco='git checkout'
alias gcob='git checkout -b'
alias gcom='git checkout master'
alias gpo='git push origin'
alias gph='git push heroku master; heroku run rake db:migrate'
alias gbclean='git branch --merged | grep -v "\*\|master\|develop" | xargs -n 1 git branch -d'
alias pr='hub pull-request'
```
