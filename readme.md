# Start
This repository is used to learn git and remote repository.

use `git clone git@github.com:fightingyuman/learngit.git` to clone this repo.

git has workspace, stage, master, remote repository.

## local commands
These commands can be used without internet, can modify workspace, stage, master.

`git add <filen-ame>` add modifies to stage.

`git commit -m 'logs'` commit changes from stage to master.

`git reset --hard <version-id>` to revert to version.

`git checkout -- <file-name>` to discard changes from stage.

in git, HEAD is a pointer to workspace, its master as default. use `git checkout -b dev`to create a branch dev, switch into it to make HEAD pointer to dev.

use `git branch` to see which branch HEAD is pointing to.

use `git merge <branch-name>` to merge changes from branch to master.

use `git branch -d <branch-name>` to delete branch.

use `git checkout master` to make HEAD pointer to master.

if a file was modified in differrent branches, it will get conflict, you can edit these files manual to resolve it.

use `git stash` to save current uncommited or unadded workspace, then checkout to other branch, do something like fix a bug with stable release and then checkout to stash branch, use `git stash pop` to restore uncommited workspace.

## remote commands
These commands can be used to push to or pull from remote repository.

if use github, we can generate a ssh key, use command to generate a ssh key: `ssh-keygen -t ras -C '<your email address[D>'`
and add rsa_pub all contents to github account sshkey.
