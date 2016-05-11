# Quit Typing the Branch Name

For literally years I did all of my `git push` like this:

`git push origin feature-some-feature-this-is-a-branch`

but you can just type

`git push origin head`

and git knows that `head` means `feature-some-feature-this-is-a-branch`

## Bonus Points

`git push -u origin head`

will set the `origin` as the upstream and now you can just type `git push` and
`git pull`, git already knows the branches from which to push and pull, nothing
else required.
