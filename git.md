# GIT

## Branches:
- list remote branches
```
git branch -a
```

```
git diff to see what is still unstaged
git diff --cached to see what you’ve staged so far:
git log -p -2
```

Adding a change to last commit
```
git commit -m 'commit missing a file'
git add forgotten_file
git commit --amend
```

```
git diff master~5:./Test.java ./Test.java
```

Delete a file from GIT, but keep local copy
```
git rm --cached <file>
```

Stash including untracked files
```
git stash -u
```

http://scotch.io/bar-talk/git-cheat-sheet

To use a previous tag :
clone download in local all tags
```
git tag -l
git checkout tags/<tag_name>
```

How to use a previous revision
```
git checkout [revision]
```

To come back at the last version : 
```
git checkout master
```

Create a new branch and checkout
```
$ git checkout -b iss53
Switched to a new branch 'iss53'
```


This is shorthand for:

```
git branch iss53
git checkout iss53
git push origin branchName
```

Merge
```
git checkout master
git merge iss53
```

Delete a branch local
```
git branch -d iss53
```

To get new master code in a branch
```
git checkout dmgr2      # gets you "on branch dmgr2"
git fetch origin        # gets you up to date with origin
git merge origin/master
```

Remote
As of Git v1.7.0, you can delete a remote branch using

```
git push origin --delete <branchName>
```

which is easier to remember than

```
git push origin :<branchName>
```

List remote branches:
```
git ls-remote --heads origin
```
```
git remote -v
git remote set-url origin https://github.com/username/repository.git
git remote -v
```

Push on 2 branches :
```
git push origin master releases/1.0
```

Save credentials linux
```
git config credential.helper store
```


Remove one commit:
```
git reset --hard to the commit we come back to
git push -f to push to the remote server
```

revert several commit:
A -> B -> C -> D -> HEAD
Goal is to come back to A commit
```
git revert --no-commit D
git revert --no-commit C
git revert --no-commit B
git commit -m "the commit message"
```

Setting user name and email
```
git config --global user.name "John Doe"
git config --global user.email "your_email@example.com"
```

Change the user name and email of a commit
```
git commit --author="John Doe <your_email@example.com>"
```

Stage
```
git add -A stages all
git add .  stages new and modified, 	without deleted
git add -u stages modified and deleted, without new

git add -A <=> --all
git add -u <=> --update
```


### Change email address in last 100 commits
```
git filter-branch -f --env-filter "GIT_AUTHOR_NAME='new name'; GIT_AUTHOR_EMAIL='new email'; GIT_COMMITTER_NAME='old name'; GIT_COMMITTER_EMAIL='old_email';" HEAD~100..HEAD
```

Show a file on another branch
```
git show <branch>:<file>
```