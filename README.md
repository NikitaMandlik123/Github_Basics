# Git and Github_Basics

This repository contains basic essential functions of Git and Github.
Github Basics:

# Git

Version control.
Manage changes you make with time.
Save checkpoints(commits).
Branching(create alternate versions of code without changing the main branch)


Downloading Git: 
using Xcode or homebrew
Using terminal
VSCode
Node.js


# Setting up a project:
Step 1. Set up the configuration variable.(Git Config)
        Configuration command on terminal ->
        #git config command
        git config --global user.name "name"
        git config --global user.email "email id"

Step 2. Initialising Projects.
        Open folder on VSCode or any other editor
        command to initialize ->
        git init 
        Makes a git folder(can view it in terminal with the command-> ls -la)
 
Step 3. Staging Files -> to add them in the repository.
        Command to add a file->
        git add FILENAME
        (or git add .)
        Making a new Commit: 
        git commit -m "Name of the commit"
        to see the commit(First Commit) 
        git log 


Understanding Environments:

 States of git environment:
 1 Working Environment
 2 Staging Environment(before creating a new commit)(temp loc)
 3 Commit Environment (New log entry is created)

File states:
 I Tracked files(last commit )
   1 Unmodified
   2 Modified
   3 Staged (moved into staging)

 II Untracked files(New files)

Restore command:
git restore filename


Ignoring Files:
 Ignore files(not uploaded to GitHub)
   Sensitive info
   Personal notes
   System files
Using .gitignore

Deleting Files:
1 From file sys: direct select and delete
 git status
 git restore


2 git rm filename
  Directly moves the deletion to staging
  git restore --S filename
  (Restore file from staging to working)

Rename files
 1 Direct click and change
 git status: one deleted file and a new created file

 2 git mv originalfilename newfilename


Differences:
git diff
View Difference between the two files(edited and old)


Changing history:
1. Amending flag
  git commit -amend  
  git commit "New commit msg"

  First make a commit : "XYZ"
  Then : git -amend
  File editor will open : change the commit msg : ABC
  git log --oneline -> the commit will show ABC

2. Rebasing: 
   git rebase <branch>/<commit>


Creating branches:
git switch -c NAME(of the new branch)
git checkout -b NAME

git branch (to see which branches are in our repository )

git merge fix-classes( will merge the changes of the fix class branch to the master branch)
Now changes are made and being added to the main branch
So now we delete the other branch(fix-classes)

Deleting a branch:
git branch --delete name
git branch --delete fix-classes
(-D)or (-d)

This sequence (make a branch--make changes--merge it with the master--delete the new branch) is known as Git flow.


Merge Conflicts:
Two users are making changes on branch and trying to merge them with the same branch.
1-- make a new branch and make a change
2-- go to main branch ad make changes
3-- git merge new branch
Will run into merge conflict
Changes from main
Changes from new branch
Which you want(main or new)

Stash and Clean:
Stashing code(putting away code so that you can work on something else)
git stash
git stash list
git stash apply
git stash pop

Git clean:
git clean -n


-------------------------------------------------------------------------------------------------------------------------------------------

# GitHub 
  
It is a Cloud repository.
Collaborative platform for different users.
Used to Manage projects as well.

1 set up remote 
2 push changes
3 fetch and pull changes

Creating a repository(github.new)
Public or private
Readme doc
Gitignore file
License


Pushing to GitHub:

Remotes:
git remote add name url

Git push:
git push REMOTE BRANCH
git push --all

# GitHub options:
Tags: to add info about repo so that ppl can find your projects on GitHub)
Like html js etc

Issues:
Notes for self : to do -- assigned to Individual and thy can comment on it

Pull requests:

Actions:
Test
Send code 
Use actions made by others

Projects:
Todo

Wiki:
Documentation
Like website

Security:
Policies

Insights:
Ppl contributing to the projects
Traffic
Commits
Tools

Settings:
Convert repository to template.

Pull requests: sequence of events:
Change the title in a file: (edit) 
Preview the changes
Commit the change
Description
Commit to main or create a new branch

Pull request:
Change title and create pull request
Notes : comments to discuss with other ppl
Merge the pull request
Confirm the merge

Managing projects;
Contributors
Issues
Labels (purpose of the issues
Milestones 
Projects

Syncing GitHub:
Clone(copy on drive)
Fetch (the code from GitHub)
git pull 

Cloning 
  git clone link of the repo

Fetching
  git fetch 
  Download the code from GitHub
  
These are the notes I took while i learnt the basics of Git and Github.
