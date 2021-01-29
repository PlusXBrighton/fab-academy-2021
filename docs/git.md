# How to use git


## References

2021 recitations
http://academany.fabcloud.io/fabacademy/2020/recitations/version-control/

Cheat sheet
https://fabacademy.org/2019/docs/FabAcademy-Tutorials/week01_principles_practices_project_management/git_simple.html

GUI clients
https://git-scm.com/download/gui/mac



## Useful commands


Pull repo (git pull includes both git fetch and git merge in one handy short cut.)

`git pull`


Add new untracked files to staging. From https://stackoverflow.com/questions/572549/difference-between-git-add-a-and-git-add

`git add -A` stages all changes
`git add .` stages new files and modifications, without deletions
`git add -u` stages modifications and deletions, without new files



Check status of repo

`git status`

Commit  changes

`git commit -m "commit message here"`


Push to remote server

`git push`

## Remove files from Git repo that you have already deleted from the file system

https://stackoverflow.com/questions/492558/removing-multiple-files-from-a-git-repo-that-have-already-been-deleted-from-disk

`git status` to see a list of deleted files

`git add -u` to add the deleted files to the staging area,
then commit them:

`git commit -m "Deleted files manually"`

## Ignore some files

e.g. a generated 'site' folder

Add the directory to the .gitignore file. e.g. `site/`
