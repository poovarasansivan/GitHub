# Topic - Git Stash

- Git stash is a way switch between the branches without Commit a work in a present working directory branch. It reduces the unnecessary Commits.

# Performed Steps

1. Created a sample html file to perform the git stash task.
2. Modified this sample html file from other branch (branch1).
3. Used a git stash to save the changes in a present working directory without Committing It.
4. Switched back to main branch and added a line of content then commited.
5. Used git stash list to list out the saved stash.
6. Used git stash pop to restore the saved work by removing it from stash list.
7. Then Committed the changes in both braches.

# Commands Learned

```
git stash 
```
- To save the unstagged and uncommitted work in present working directory.

```
 git stash list 
```
- To list out the stored stash.

```
git stash pop 
``` 
- To restore the stored work.

``` 
git stash apply stash@{n} 
```
- To restore the work based on stash list order number(n).

```
git stash clear 
```
- To clear all the stash store.

```
git stash -u 
```
- To store the untracked file.

```
git stash drop stash@{n}
```
 - To drop the particular stored stash entry.