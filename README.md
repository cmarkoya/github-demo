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

**when committing without a message**
it will prompt you to type a message, then you will need to press "Esc" and then type :wq to exit the editor.
w means write, q means quit

# view your previous commits
git log
(or concise version)
git log --oneline

when the log shows, usually there is a colon after the log. You will need to type q in the command to quit the log.

# go back to a previous commit
git checkout (hashcode of the commit you want to stay)
e.g. git checkout b02bece

# undoing changes
git reset --soft hashcode 
(soft means you still can keep it if you want to get it back)
git reset --hard hashcode 
(hard measn completly getting rid of it)

# detached head --how to fix
Detached head means you are no longer on a branch, you have checked out a single commit in the history (in this case the commit previous to HEAD, i.e. HEAD^).

If you want to keep your changes associated with the detached HEAD
Run **git branch tmp** - this will save your changes in a new branch called tmp.
Run **git checkout master** - if you are in main branch, run **git checkout main**
If you would like to incorporate the changes you made into master, run **git merge tmp** from the master branch. You should be on the master branch after running git checkout master.
If you want to delete your changes associated with the detached HEAD
You only need to checkout the branch you were on, e.g.

**git checkout master** or **git checkout main**
Next time you have changed a file and want to restore it to the state it is in the index, don't delete the file first, just do

git checkout -- path/to/foo
This will restore the file foo to the state it is in the index.