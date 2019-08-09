# Practice for Git operations

- **Clone** : Get the local copy of project using remote-url

On Bash : 
```
git clone https://github.com/adityapatil123/Git-practice.git
```

- **Add** : Stage the files for committing

On Bash : 

```
git add new-file.txt
```

- **Status** : Show the staged files and untracked files

On Bash : 
```
git status
```

- **Commit** : Commit the staged files, 'm' flag is for messaging and message should be in order-format(verb first)

On Bash : 
```
git commit -m "Add new file"
```

- **Log** : Show the commits

On Bash : 
```
git log
```

- **Show** : Show the code for commit-ID(get from log), here '+' is for addition and '-' for deletion of code

On Bash : 
```
git show 9627a480ed588867da984d28c0706d2c366bc07a
```

- **Diff** : Diff between the commits

On Bash : 
```
git diff
```

- **Amend** : Update only in prev commit instead of creating new one

On Bash : 
```
git commit --amend -m "Update the new-file replacing prev commit"
```

- **Push** : Push to remote repo (here branch is 'master')

On Bash : 
```
git push origin master
```

- **Pull** : Pull remote repo (pull first, handle conflicts and then push)

On Bash : 
```
git pull origin master
```

- **Stash** : Code which is not yet to commit and you have to work on different branch, hence for that keep in stash(draft) temporarily.

On Bash : 
```
git stash	# Make stash
git stash list	# Show stash-list
git stash pop	# Return on stashed stage again 
```
