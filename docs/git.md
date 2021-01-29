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



## SSH Key

From https://fabacademy.org/2019/docs/FabAcademy-Tutorials/week01_principles_practices_project_management/git_simple.html

1. Check if you have an SSH KEY already cat ~/.ssh/id_rsa.pub (If you see a long string starting with ssh-rsa, you can skip the ssh-keygen step) 

```andrew@andrew Git % cat ~/.ssh/id_rsa.pub
cat: /Users/andrew/.ssh/id_rsa.pub: No such file or directory
```


2. Generate your SSH key ssh-keygen -t rsa -C "$your_email"

```
ssh-keygen -t rsa -C "$andrew.sleigh@gmail.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/andrew/.ssh/id_rsa):
```


Press enter to accept default name

Enter passphrase (empty for no passphrase):


3. Now let's see your keygen 

`cat ~/.ssh/id_rsa.pub `

I’m not sure why it has that fragment of my email at the end….
https://askubuntu.com/questions/801997/purpose-of-email-at-the-end-of-ssh-public-key
I think its just a comment and can be left out



4. Copy your key

`pbcopy < ~/.ssh/id_rsa.pub`



### Adding your SSH public key to GitLab
https://docs.gitlab.com/ee/gitlab-basics/create-your-ssh-keys.html


### Store passphrase in Keychain so you don't have to enter it each time

`sudo pico ~/.ssh/config`

Add these lines:

```
Host *
    UseKeychain yes
```
