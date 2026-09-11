# Git

## Commands

Delete all branches except `develop`:

```
git branch | grep -v "develop" | xargs git branch -D
```

Create git command alias:

```
git config --global alias.st status
```

| Command                 | Description                           |
| :---------------------- | :------------------------------------ |
| git reset --soft HEAD~N | squash N last commits                 |
| git reset --soft parent | squash all commits from parent branch |
