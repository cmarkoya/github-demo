## GitHub Demo Repo
This is a demo of how to work with Github

This is a new line

# About the Project
**Some description**

# Resources
data not available 

# add file to staging
git add REPORT.md
git add . (add all of the changed files)

# restore or reset from staging
git restore --staged REPORT.md
git reset . (reset all changed files)

# check status
git status

# commite changes
all commits need a message, stating what changes you made.
git commit -m "update git notes"
**it will ask you who you are**
git config --global user.email "you@example.com"
git config --global user.name "myname" (this is your Github username)

# view your previous commits
git log
(or concise version)
git log --oneline

# go back to a previous commit
git checkout (hashcode of the commit you want to stay)
e.g. git checkout b02bece
