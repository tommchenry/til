# Quit Typing Your Password

Friend, you've got to set up an SSH key on your computer for GitHub 

## Generate an SSH Key

Put this in your Terminal: `ssh-keygen -t rsa -b 4096 -C
"your_email@whatever.com"` (where your_email@whatever.com is the email address
associated with your GitHub account). You'll be asked for a location to save the
key and a passphrase by which to generate it.

## Add the SSH Key to the ssh-agent

Start ssh-agent in the background by typing the following in the Terminal:

`eval "$(ssh-agent -s)"`

Now add the SSH key your generated in the first step to the ssh-agent:

`ssh-add ~/.ssh/id_rsa`

## Add the SSH Key to Your GitHub Account

In your Terminal, type:

`pbcopy < ~/.ssh/id_rsa.pub`

This will copy the generated SSH key to your clipboard (`pbcopy`).

Now in GitHub go to `Settings > SSH and GPG Keys` and click `New SSH Key`

Give a descriptive title for the computer that generated this SSH key, then
paste the contents of your clipboard into they Key field and click `Add SSH Key`

## Change Your Remote

Now you'll need to change your remote URL from HTTPS to SSH.

`git remote -v` will list your existing remotes. They're probably set to
something like `https://github.com/USERNAME/OTHERREPOSITORY.git` or else you're
already done.

You'll need to type `git remote set-url origin git@github.com:USERNAME/OTHERREPOSITORY.git`
(where USERNAME and OTHERREPOSITORY are your GitHub username and repo,
respectively).

Finally, type `git remote -v` one last time to make sure that your repositories
have switched from HTTPS to SSH.

[GitHub's official
documentation](https://help.github.com/articles/changing-a-remote-s-url/)
