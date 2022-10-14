# location of git key
/Users/juan/.ssh'



## Terms
Directory: folder
cd: change directory/folder
reposatory: git folder/place where your project is kept
github: website to host your reposatory
.git file: stores files that save your commits. contains all changes recorded

# git commands terms
clone: bring a reposatory that is hosted somewhere like github into a folder on your local machine
add: track your files and changes in git
commit: save your files in git
push: up;pad git commits to a remote repo, like github
pull: download changes from remote repo to your local machine


## git commands

# see hidden files
ls -a

# make a local folder a reposatory
git init

# link github reposatory to local reposatory
-url: url of github reposatory
git remote add origin url

# shows all fields created/updated and have not been saved in a commit
git status

# add all files that have not been tracked in a commit
git add .
git add --all

# add specific file that has not been tracked in a commit
git add fileName

# captures a snapshot of the project's currently staged changes. its a save, like a checkpoint save
git commit -m "changeTitle" -m "changeDescription"


# send code to cloud [1]
- origin: location of gitreposatory
- master:
git push origin master

# send code to cloud [2]
- requires origin to be set, see # link github reposatory to local reposatory
git push -u

# send code to cloud
git push --set-upstream URl BRANCH_NAME
ex:
git push --set-upstream https://github.com/casas1010/flutter_firebase_vendor_management main

# add tags
git tag "someText"
git push --tags

# config git
git config --global

# show branches and the branch that I am on
git branch

# create a new branch
-nameOfBranch: name of the branch, usually starts with feature or bug, then a mini description
git checkout -b nameOfBranch

# switch between branches
git checkout nameOfBranch


# get difference between branches
- switch to one of the branches you want to compare, the compare with branchName
git diff branchName


# merge branch by creating a pull request
- switch to feature/bug branch
- branchName: name of branch
git push --set-upstream origin branchName
- open the link provided in the terminal
- resolve comments if any
- click 'merge pull request'
- you need to then pull the master branch from github to local










