# Steps Executed

- Created a Sample text file with some content
```
git add <filename> 
```
- To stage the changes

```
git commit -m "Initial commit with sample.txt"
```
- To commit the changes

```
[main 4885496] Initial Commit with sample.txt
 1 file changed, 1 insertion(+)
 create mode 100644 Task-4/sample.txt
```

```
git checkout -b conflicts 
```
- Created a new branch named conflicts

```
Switched to a new branch 'conflicts'
```

- Modified the sample.txt file by adding new line of content.

```
git commit -am "Updated sample.txt" 
```
- a (auto stage Modified files) and m (commit message). Quick solution to stage and commit in single command.

```
[conflicts a6b01c1] Updated sample.txt
 1 file changed, 1 insertion(+)
```

- Again switch back to main branch
```
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
```
- Again Created a new branch (conflict2) and switched to that branch.
```
Switched to a new branch 'conflict2'
```
```
git commit -am "Updated sample.txt" 
```
- Modified the file and commited it.

```
[conflict2 e6ef574] Updated sample.txt
 1 file changed, 1 insertion(+)
```

- Again switch back to main branch
```
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
```

```
git merge conflicts 
```
- Merging the main and conflicts branch.

```
Updating 4885496..a6b01c1
Fast-forward
 Task-4/sample.txt | 1 +
 1 file changed, 1 insertion(+)
```

```
git merge conflict2
```
 - Merging the conflict2 branch

```
Auto-merging Task-4/sample.txt
CONFLICT (content): Merge conflict in Task-4/sample.txt
Automatic merge failed; fix conflicts and then commit the result.
```

```
git status 
```
- To see the status and issues

```
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   sample.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Steps.txt

no changes added to commit (use "git add" and/or "git commit -a")

14. git diff - to see the  difference between branches

diff --cc Task-4/sample.txt
index 2f65f69,93d0bdc..0000000
--- a/Task-4/sample.txt
+++ b/Task-4/sample.txt
@@@ -1,2 -1,2 +1,6 @@@
  This is sample text file to work with merge conflicts
- This is sample text added using a new branch.
 -This is the Sample text added by branch conflict2.
++<<<<<<< HEAD
++This is sample text added using a new branch.
++=======
:
```

```
 git add sample.txt 
```
- Fixed the conflict part of lines and staged it.

```
git commit -m "Conflict Resolved" 
```
- Commiting the changes after solving the conflicts.


```
 git push origin main
 ```
 
  - To push the changes to remote repository
