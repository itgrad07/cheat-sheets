# Git

## Dealing with branches

| Command              | Description         |
| :------------------- | :------------------ |
| git branch           | show local branches |
| git branch -D branch | delete local branch |

Delete all branches except `develop`:

```
git branch | grep -v "develop" | xargs git branch -D
```

## Dealing with commits

| Command                         | Description                                |
| :------------------------------ | :----------------------------------------- |
| git add .                       | stage all changes                          |
| git commit -m "msg"             | commit staged changes                      |
| git commit --amend -m "new msg" | change last local commit message           |
| git log --oneline               | show commits history (one commit per line) |
| git push                        | push local commits on remote               |
| git push --force                | force push                                 |
| git reset --soft HEAD~N         | squash N last commits                      |
| git reset --soft parent         | squash all commits from parent branch      |
| git reset --hard commitId       | reset current branch to certain commit     |

The command `git reset --soft HEAD~2` tells Git to "go back 2 commits from the current one." However, because these are the **very first commits** in your repository, there is no "commit zero" to go back to. Git doesn't know what to do when you ask it to go before the beginning of time.

```
git rebase -i --root
```

Change the word pick on the second line to squash

```
pick a1b2c3d First commit message
squash e4f5g6h Second commit message
```

## Configuring

Create git command alias:

```
git config --global alias.st status
```

Two different ways to compare branches: `git diff` (compares real changes) and `git log` (compares commits)
