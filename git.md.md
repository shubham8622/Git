# To use git use these commands

- git init

- git status

- git add .
- git log **check the commits.**
- git log --oneline **check the commites in one line.**
- git diff **check the difference.**
- git diff filename **check difference of seperate file**
- git diff --staged **check the differnce of staged file**
- git restore filename **If you don't know what changes you have done and don't want to commit the changes just use this command.**
- git rm filename **It will delete file from commit and from localhost also.**
- git rm --cached filename **used for file which tracked after add file in .gitignore.**
- git commit -m "message" **commit all the changes.**
- git commit -am "message" **Tell the command to automatically stage files that have been modified and deleted, but new files you have not told git about are not affected.**
- git reset HEAD  **staging->filechange->untracked all the files on staging.**
- git reset HEAD filename **staging->filechange If you change in file and add it to staging. But now, you don't want to commit it. In that case use this command it will untracked this file from the staging.** 
- git checkout -- filename **It will check the file in repositery and replace this file with that file which was present in the repositery.**
- git commit --amend -m "message" **This command is used to change the last commit beacuse last commit is not depend on any other commit.**
- git checkout SHA-1 -- filename **commit->staging->changeFile  checkout with previous version. If your code is not running some reason but you know that before some day it was running and now you want to change the current file with that day of file. Then use this command.**

- git reset --soft
- git reset --mixed
- git reset --hard
- git reset HEAD~1
- git clean -n
- git clean -f

# Branch

- git branch **To check all the branches.**
- git branch branchName **To create new branch.**
or 
- git checkout -b branchName **It will create a new branch and switch to it.**

# Compare two branches

- git diff branchName..branchname **Check the difference b/w two branches.**

# Change name of branch

- git branch -m newBranch2 newBranch1

# Delete a branch

- git branch -d branchName

**if you have changed in branch like addFile and then you are trying to delete the branch. Then it will say that you didn't merge these changes if you still want to delete it run this command.**

- git branch -D branchName

# Check someone git logs since 2021-02-11

- git log --author="shubham" --since="2021-02-11"

# Lasted 5 commit made by someone

- git log --oneline 5 --author="shubham"

**or**

- git log --oneline -5

# Merge two branches

-  git merge branchname **Here it moves the SHA-1 to master branch.**

- git merge --no-ff branchname **Here it create new SHA-1 fot mergeing.**

- git merge --ff-only branchname

# Conflits during merging

- git merge --abort **if conflicts come and you want to abort the merge use this command.**


# Stashing

- git stash save "message" **Save a stash.**

- git stash list **get the list of the stash.**

- git stash show stash@{0}  **stash@{0} is stash id show stash.**

- git stash show -p stash@{0}  **show stash is detail.**

- git stash pop stash@{0}  **it will delete the stash and move save things in stash to the branch.**

- git stash apply stash@{0}  **it will make the copy and add to tehe file not delete it from the stash.**

- git stash drop stash@{0}  **drop particular stash.**

- git stash clear  **clear all the stash.**
