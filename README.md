push-existed-project-to-github-repo
===

This repository demostrates how to push an existed local repository to GitHub

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

![Git Graph of merging two repositories which don't have related histories](git-graph.jpg)