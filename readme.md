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
use `git branch -D <branch-name>` to delete an unmerged branch.

use `git checkout master` to make HEAD pointer to master.

if a file was modified in differrent branches, it will get conflict, you can edit these files manual to resolve it.

use `git stash` to save current uncommited or unadded workspace, then checkout to other branch, do something like fix a bug with stable release and then checkout to stash branch, use `git stash pop` to restore uncommited workspace.

use `git tag <tag-name> [other-commit] -m 'log'` to create a tag pointer to HEAD or other commit id. tag is associated to commit, if commit exists in multiple branches, the tag will exist in these branches.

use `git tag -d <tag-name>` to delete a tag.

use file **.gitignore** to ignore files dont want to commit, can use wildcard like `*.pyc`.

## remote commands
These commands can be used to push to or pull from remote repository.

if use github, we can generate a ssh key, use command to generate a ssh key: `ssh-keygen -t ras -C '<your email address[D>'`
and add rsa_pub all contents to github account sshkey.

use `git clone <url>` to clone repo to local machine, it is **origin** as default.

use `git remote -v` to check remote version information.

use `git push [branch-name]` to push branch to remote server, master as default.

use `git checkout -b branch-name origin/branch-name` to create a branch to local machine and remote server.

use `git pull` to pull modify from other person to local machine.

if other person create a branch and pushed before, you have to use `git branch --set-upstream-to <branch-name> origin/<branch-name>` to make local branch link to remote branch.a

use `git push origin tag <tag-name>` to push tag to remote server.

use `git push origin tag :refs/tag/<tag-name>` to remove a tag from remote server.

