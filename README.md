# Git-Note

Git note.

## Connect GitHub and Local

### Procedure

1. Create repository.
2. Open terminal.
```shell
git init
git remote add origin git@github.com:[your repository]
```
3. Before first commit, you should type in the code below.
```shell
git pull --rebase origin master
```
4. Update all files.
```shell
git add .
git commit -m "message"
git push -u origin master
```

## Logging

```shell
git log --all --decorate --online --graph
```

If you want it to be a shortcut, you can do it this way.

```shell
alias graph="git log --all --decorate --online --graph"
graph
```

## Delete Unpushed Git Commit

All the local committed changes would be dropped and local will be reset to the same as remote origin/master branch.
```shell
git reset --hard HEAD~1
```

## Clone a Specific Branch

```shell
git clone -b <branch> <remote_repo>
```
## Overwrite Existing Tags

Reference from [GitHub Docs](https://docs.github.com/en/github/authenticating-to-github/removing-sensitive-data-from-a-repository).
```shell
git filter-branch --force --index-filter "git rm --cached --ignore-unmatch PATH-TO-YOUR-FILE-WITH-SENSITIVE-DATA" --prune-empty --tag-name-filter cat -- --all
```
