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

- **Move/Delete** : Move/Delete the file from one location to another

On Bash : 
```
git mv new-file2.txt folder1/
git rm file.txt
```

- **Revert** : Revert contents of file

On Bash : 
```
git checkout file.txt
```

- **Remove changes** : Remove the staged files

On Bash : 
```
git checkout HEAD -- file.txt
```

- **Move HEAD Pointer** : Move HEAD pointer to the given commit-ID. This can be soft, mixed and hard.
1. **--soft** :Reset the HEAD pointer only without destroying anything.
2. **--mixed** :Reverts those changes from the staging area that have not been committed yet.
3. **--hard** :Reset the HEAD pointer with clearing staging area.

On Bash : 
```
git reset --soft HEAD~	# Pointer to the prev commit
```

- **Tag** : Tag the commit with tag(version)

On Bash : 
```
git tag -a 'Release_1_0' -m 'Tagged basic string operation code' HEAD	# Add Tag
git tag -d Release_1_0		# Delete Tag
```

- **Branch** : Make new-branch and operations

On Bash : 
```
git branch new_branch		# Make new branch
git branch			# Get branches with current starting with *(asterisk)
git checkout new_branch		# Switch to branch
git branch -D test_branch	# Delete the branch
git branch -m new_branch branch1	#Rename the branch
```

- **Merge/Rebase** : Merge/Rebase two branches

On Bash : 
```
# master commits : A -> B -> C -> D
# new_branch commits : A -> B -> X -> Y

git merge origin/new_branch	# Merge contents of branch, destination will be current branch
# Result: A -> B -> C -> D -> X -> Y	i.e.branch commit will be head

git rebase origin/new_branch	# Rebase contents of branch, destination will be current branch
# Result: A -> B -> X -> Y -> C -> D	i.e.your commit will be head
```
