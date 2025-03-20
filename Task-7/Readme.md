# Topic - Git Cherry Pick

- Git Cherry pick is way to bring in a changes from a specific commit from braches.
- We are able to choose one or more commits.

# Steps Performed

1. Created a sample text file to work on Cherry Pick task and added a one line of content.
2. Staggged the content and commited it from main branch.
3. Created a new branch named cherry-pick and added a some more lines.
4. Stagged and Committed the content from cherry-pick branch.
5. Switched back to main branch.
6. By using git cherry-pick <commit-hash> added the commited content of cherry pick.
7. Verified it by running git log --online.


# Commands Learned

```
git add . 
```
  - Stage the files
  
```
git commit -m "Message" 
```
- Commit the changes

```
 git checkout -b <brach-name> 
```
- Created a new branch and Switched to it.

``` 
git switch main 
``` 
- Switched back to main branch.

```
git log --oneline <branch-name>
```
 - To see the commit log of a selected branch.

```
git cherry-pick <commit-hash> 
```
- To apply the particular commit changes to main branch and commit it by main branch automatically.

```
git cherry-pick <commit-hash> -n 
```
- To only apply the particular commit changes and didn't make a commit (-n stands for no commit).

```
git cherry-pic <commit-hash> <commit-hash>
```
 - To apply the one or more commit changes.