#### Task 1: Save Changes Temporarily with git stash

1.changes the file without commiting
```
  echo "hi">>file1.txt
```
2.view the changes history
```
  git status
```
3. stash the changes
```
   git stash   
```
4.view the stash changes
```
  git stash list
```

#### Task 2: Apply and Drop Stashed Changes

1.apply the most recent stash
  ```
  git stash apply
  ```
2.drop the most recent stash
 ```
 git stash drop
 ```
 3.Alternatively, to apply a specific stash:
 ```
 git stash apply stash@{1}
 ```

#### Task 4: Stash Untracked Files 

1.Stash changes, including untracked files: 
```  
  git stash -u
```
2Apply stashed changes including untracked files: 
```
git stash apply
``` 

#### Task 5: Canceling a Rebase

1.If a rebase goes wrong, abort it: 
```
git rebase --abort
```

#### Task 6: Use Interactive Rebase to Modify Commit History

1.view the last few commit
 ```
 git log --oneline
 ```

2.Start an interactive rebase for the last 3 commits:
```
git rebase -i HEAD~3
```

3.Modify the commits by changing pick to one of the following:

    squash (combine commits)
    reword (edit commit message)
    edit (edit commit content)
    drop (remove commit)

4.Example of squashing two commits:


    Change the second commit from pick to squash and save.
    Git will combine the commit messages for the squashed commit.


#### Task 7: Complete Interactive Rebase

1.After modifying the commits, save and close the editor.

2.Resolve any conflicts if prompted, then continue the rebase:
```
git rebase --continue
```

#### Task 8: Pick a Specific Commit

1.View the commit history to find the commit hash you want to cherry-pick:
```
  git log --oneline
  ```

2.Cherry-pick a specific commit by its hash:
```
  git cherry-pick <commit-hash>
```

3.Resolve conflicts if any, then commit the changes:
```
git add .
git cherry-pick --continue
```

#### Task 9: Tag a Commit

1.Tag the current commit with a version number:
```
  git tag -a v1.0 -m "Initial release"
  ```

2.List all tags:
```
  git tag
  ```

#### Task 10: Tag a Specific Commit

1.Tag a specific commit by its hash: 
```
  git tag -a v1.1 <commit-hash> -m "Bug fix"
  ```

#### Task 11: Push Tags to Remote

1.Push a specific tag to the remote repository:
```
  git push origin v1.0
  ```

  2.Push all tags to the remote repository:
```
  git push --tags
  ```


#### Task 12: Add a Remote Repository

1.Add a remote repository URL
```
  git remote add origin https://github.com/username/repo.git
```

#### Task 13: Fetch Changes from Remote

1.Fetch the repository without merging
```
git fetch origin
```

2.View fetched branches:
```
git branch -r
```

#### Task 14: Pull Changes from Remote

1.To pull the latest changes from the remote repository
```
  git pull origin main
```

#### Task 15: Push Changes to Remote

1.Push changes to the repository:
```
git push origin main
```

2.Push a new branch in the repository:
```
git push origin feature-branch
```

#### Task 16: Delete Remote Branch

1.To delete a remote branch:
```
git push origin --delete feature-branch
```

#### Task 17: Fork a Repository on GitHub

1.Open github and go to the repository and then click the "fork" button

2.Clone the repository into your local device

    git clone "url"

#### Task 18: Make Changes and Commit

1.Create a new branch in your repository
```
    git checkout -b feature
    ```

2.Make some changes and commit them
```
    git add README.md
    git commit -m "commited"
    ```

#### Task 19: Push Changes to Your Fork

1.Then after push the changes to your fork repository:
```
   git push origin fix-typo
   ```

#### Task 20: Create a Pull Request

1.Go to the forked repository and click "create pull request" and add some title and discription

#### Task 21: Sync Your Fork with the Original Repository

1.Add the original repository as a remote source:

  1.git remote add upstream url
  Fetch changes from the original repository:
```
  git fetch upstream
```

  2.Merge changes from the original repository into your local branch:
```
git checkout main
git merge upstream/main
```

3.Push the changes to your fork:
```
git push origin main
```
