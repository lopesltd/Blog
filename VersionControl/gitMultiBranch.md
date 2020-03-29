# Git Multiple Branch

    Usually, in the multi-person collaborative development environment,we need to constantly pull and merge local branch to the master branch without affecting development.

    
- New Branch
``` git
# Pull the latest code from the remote master branch

git clone xxx.git

# Switch to the master branch and pull

git checkout master
git pull

# New branch and switch to it

git checkout -b develop-wxy-0329

# Push the new branch to the remote repository

git push origin develop-wxy-0329

# Establish a mapping between local branch and remote branch

git branch --set-upstream-to=origin/develop-wxy-0329
git pull

```

- Merge remote branch code to local branch
``` git
# Switch to the local branch

git checkout develop-wxy-0329

# Pull the latest remote master branch to the local branch

git fetch origin master 

# Merge the latest remote master branch to the local branch

git merge origin/master

# Push to remote local branch repository
git add .
git commit -m "update"
git push

```

- Merge the local branch to remote branch
``` git
# Switch to the remote branch

git checkout master

# Merge the local branch to current remote branch

get merge develop-wxy-0329

# Push to the remote master branch repository

git push --set-upstream origin master

```