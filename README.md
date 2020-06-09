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

## Delete Unpushed Git Commit
All the local committed changes would be dropped and local will be reset to the same as remote origin/master branch.
```git reset --hard origin```
