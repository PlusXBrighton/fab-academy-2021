# How to use git


## References

2021 recitations
http://academany.fabcloud.io/fabacademy/2020/recitations/version-control/

In this recitation we are going to explain what version control is. Our focus is going to be Git, GitLab and plain HTML.

## Useful commands


Pull repo
(git pull include both git fetch and git merge in one handy short cut.)

> git pull


Add new untracked files to Git

> git add .

Check status of repo:

> git status

Commit  changes

> git commit -m "commit message here"


Push to remote server

> git push

## Remove files from Git repo that you have already deleted from the file system

https://stackoverflow.com/questions/492558/removing-multiple-files-from-a-git-repo-that-have-already-been-deleted-from-disk

'git status' to see a list of delted files

'git add -u' to add the deleted files to the staging area, then commit them

'git commit -m "Deleted files manually"'

## Ignore some files

e.g. a generated 'site' folder
