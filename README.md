push-existed-project-to-github-repo
===

This repository demostrates how to push an existed local repository to GitHub

# Push an existed local repo to GitHub

## step 1

Create a GitHub repo on GitHub website

## step 2

Be ready to merge your local repository on your machine
```
git init
git add .
git commit
```

## step 3

Add a GitHub repo as a remote repo
```
git remote add origin git@github.com:[USER_NAME]/[GITHUB_REPO].git
```

## step 4

merge local repo with GitHub repo and allow unrelated histories
```
git pull origin main --allow-unrelated-histories
```

## step 5

push the merged version to GitHub
```
git push orign main
```

## final

The final git graph will be looked like this

![Git Graph of merging two repositories which don't have related histories](images/git-graph-1.jpg)

# Switch default branch

[ *this is optional* ]

Sometimes your default branches of local repo and remote repo are not the same name. If you want to choose one of them, just simply delete one and continue push new version to another one.

If you want to choose the branch name from GitHub, like me, try to follow this step:


1. switch local branch to main (GitHub default branch)
```
git checkout main
```

2. merge master branch into main branch
```
git merge master
```

3. push
```
git push origin main
```

Then, the current git graph will be looked like this

![Git Graph of switch default branch](images/git-graph-2.jpg)

# Delete unused branch

[ *this is optional* ]

- Delete local branch
```
git branch -d master
```

- Delete remote branch
```
git push -d origin master
```

After that, the final git graph will be looked like this

![Git Graph of delete unused branch](images/git-graph-3.jpg)
