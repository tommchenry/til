# Interactive Rebases

`git rebase -i head~10` will start an interactive rebase of the last 10 commits
on this branch. Change the number as necessary. Maybe run `git log` ahead of
time to know how many commits you're looking to rebase through.

Anyway an interactive rebase shows you a list of those commits and lets you run
through them like a for or each loop, performing the action you set on each. You
can squash two (or more) commit messages together into one, edit messages, or
even remove commits from rebasing entirely on this branch. The instructions are
all there in the comments on the list.

Useful, but mostly locally when you're trying to clean up your commits before
you push a branch up to a repo. You wouldn't, say, `git rebase -i
origin/master`.

See also: [Squash](git/squash.md)
