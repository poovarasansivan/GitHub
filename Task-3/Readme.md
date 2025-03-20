# Commands Learned

```git restore <filename> 
```
- To discard the changes in a file before staging it.

```
git reset HEAD <filename>
```
- To unstage the files that are alreadys staged and before commiting it on remote repository

```
git reset --soft HEAD~1
```
- It will undo the last commit but keeping changes staged

```
git reset --mixed HEAD~1
```
- It will undo the last commit but keeps the changes unstaged

```
git reset --hard HEAD~1
```
-It will completely erase the last change and commits

```
git revert <commit-hash>
```
- It will used to undo the commit safely in a shared project 


# Difference Between git revert and git reverse 

-  ```git revert``` - It is used to undo a commit in a shared project safely and creating a new commit that reverse the previous one
-  ```git reset``` - It is a command used to undo the changes and commits in different ways (unstage, undo commit, erase changes permanently )



# Practiced Steps:

1. ```git init```  - Initialized the repository
2. ```git add <filename>``` - Created a Sample index.html file and added it for tracking
3. ```git restore <filename>``` - Modified the same index.html file and then restored it before staging it 
4. ```git reset HEAD <filename>``` - Modified files is staged and then undo the last commit before commiting it.
5. ```git reset --soft HEAD~1``` - Undo the last commit by keeping the changes staged
6. ```git reset --mixed HEAD~1``` - undo the last commit and keeping the changes unstaged
7. ```git reset --hard HEAD~1``` - undo the last commit and changes
8. ```git revert <commit-hash>``` - undo a commit safely from a shared project



