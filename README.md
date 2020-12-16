# Git_Practice
### Test Repository to Test Git Practices


### Git Basic
```bash
# checks the current status of the git repository
git status
```
### Git Init
```bash
# Initializes empty git repository to in the current folder
git init
```
### Git Bare
```bash
# initializes the bare repository (remote)
git init --bare
```
### Git Clone
```bash
# clones the remote repository to local
git clone git@github.com:nviswanathareddy/Git_Practice.git
```
### Git Configure username and email
```bash
# lists the cofiguaration file
git config --list

# configuring username
git config --global user.name "nviswanathareddy"

# shows the  username
git config user.name

# shows the email
git config user.email

# configuring email
git config --global user.email "viswanathareddynagireddy@gmail.com"
```
### Git Diff
```bash
# shows all the edited files in working area
git diff

# shows edited content of single file
git diff index.html

# shows edited content in staging area
git diff --staged test.html

# compares the changes between two commit id's
git diff cid cid

# compares the changes between two latest commit id's
git diff HEAD HEAD~1

```
### Git Remote
```bash
# adding the remote repository to local repository
git remote add origin git@github.com:nviswanathareddy/Git_Practice.git

# shows short name of remote repository
git remote

# shows full url
git remote show origin

# shows the content related to origin
git remote -v

# renames the tracked file
git rename

# removes the remote repository url attached to origin in local repository
git remote remove origin
```
### Git Log
```bash
# shows log history
git log

# shows log history in oneline
git log --oneline

# shows the log related to the specific author
git log --author "nviswanathareddy"

# shows the files that are committed in that particular commit
git show --pretty="" --name-only fe038f2

#
git log --stat

#
git log -p

#
git show

#
git reflog
```
### Git Add
```bash
# adds the single file to staging area
git add index.html

# adds all the files to staging area
git add .

# adds the total git repository to staging area
git add -A
```
### Git Restore
```bash
# discards the changes in working directory
git restore

# removes the files from staging area to working area
git restore --staged test.html

# removes un tracked files from working area
git clean

# removes the un tracked files for directories from working area 
git clean -df
```
### Git Commit
```bash
# commits the changes to local repository, have to add the commit message in the editor
git commit

# commits the code from staging area to local repository
git commit - m "added index.html file"

# adds and commits the file in single command
git commit -a -m "commit message"

# same as git commit -a -m
git commit -am "commit message"

# re writes the commit message
git commit --amend -m "commit message"
```
### Git Reset
```bash
#
git reset --soft cid

#
git reset --mixed cid

#
git reset --hard cid
```
### Git Revert
```bash
#
git revert cid

#
git revert -n
```
### Git Push
```bash
# pushes the code from local repository to remote repository
git push origin main
```
# Git Branches

```bash
# shows the branches in local repository
git branch

# shows the branch details
git branch -v

# creates a new branch
git branch feature

# shows the both local and remote repository
git branch -a

# changes the branch
git checkout feature

# switches the branch
git switch feature

# creates and switches the branch at a time
git checkout -b feature-b

# renames the branch
git branch -m feature feature-a

# renames the current branch
git branch -m

# shows the branches in the remote repository
git branch -r

# deletes the branch if the branch is committed
git branch -d feature

# deletes the branch forcefully
git branch -D feature

# shows the differences between branches
git diff main feature

# merges the branch to the current branch
git merge feature

# to check what branches are merged
git branch --merged

# pushes the branch to remote repository
git push origin feature

# deletes the branch from remote repository
git push origin --delete feature
```