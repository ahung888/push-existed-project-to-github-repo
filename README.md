This repository demostrates how to push an existed local repository to GitHub

## Push an existed local repo to GitHub

1. Create a GitHub repo on GitHub website

2. Be ready to merge your local repository on your machine

```bash
git init
git add .
git commit
```

3. Add a GitHub repo as a remote repo

```bash
git remote add origin git@github.com:[USER_NAME]/[GITHUB_REPO].git
```

4. merge local repo with GitHub repo and allow unrelated histories

```bash
git pull origin main --allow-unrelated-histories
```

5. push the merged version to GitHub

```bash
git push orign main
```

6. The final git graph will be looked like this

![Git Graph of merging two repositories which don't have related histories](images/git-graph-1.jpg)

## Switch default branch

*`[ this is optional ]`*

Sometimes your default branches of local repo and remote repo are not the same name. If you want to choose one of them, just simply delete one and continue push new version to another one.

If you want to choose the branch name from GitHub, like me, try to follow this step:


1. switch local branch to main (GitHub default branch)

```bash
git checkout main
```

2. merge master branch into main branch

```bash
git merge master
```

3. push

```bash
git push origin main
```

Then, the current git graph will be looked like this

![Git Graph of switch default branch](images/git-graph-2.jpg)

## Delete unused branch

*`[ this is optional ]`*

1. Delete local branch
```bash
git branch -d master
```

2. Delete remote branch
```bash
git push -d origin master
```

After that, the final git graph will be looked like this

![Git Graph of delete unused branch](images/git-graph-3.jpg)
