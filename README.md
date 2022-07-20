# Git_cheat_sheet2
# Collaboration 
## 1. Cloning a repository
```
$ git clone url
```
## 2. syncing with remotes
#fetches master from origin
```
$ git fetch origin master
```
#fetches all objects from origin
```
$ git fetch origin
```
#shortcut for "git fetch origin"
```
$ git fetch
```
#fetch + merge
```
$ git pull
```
#pushes master to origin
```
$ git puch origin master
```
#shortcut for "git push origin master"
```
$ git push
```
## 3. Sharing tags
#pushes tag vl.0 to origin
```
$ git push origin vl.0
```
``` 
$ git puch origin --delete vl.0
```
## 4. sharing branches
#shows remote tracking branshes
```
$ git branch -r
```
#shows local & remote tracking branches
```
$ git branch -vw
```
#pushes bugfix to origin
```
$ git push -u origin bugfix
```
#removing bugfix from origin
```
$ git push -d origin bugfix
```
## 5. Managing remoting
#shows remote repos
```
$ git remote
```
#adds a new remote repos
```
$ git remote add upstream url
```
#remotes upstream
```
$ git remote rm upstream
```

# Rewriting history
## 6. undoing commits
#removes the last commit ,keeps changed staged
```
$ git reset --set HEAD^
```
#unstages the change as well
```
$ git reset --mixes HEAD^
```
## 7. reverting commit
#reverts the given commit
```
$ git revert 72856ea
```
#reverts the last three commits
```
$ git revert HEAD~3..
```
```
$ git revert --no-commit HEAD~3
```
## 8. recovering lost commits
#shows the history of HEAD
```
$ git reflog
```
#shows the hostory of bugfix pointer
```
$ git reflog show bugfix
```
## 9. Amending the last commit
```
$ git commit --amend
```
## 10. Interactive rebasing
```
$ git rebase -I HEAD~5
