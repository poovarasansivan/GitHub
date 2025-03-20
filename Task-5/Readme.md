# Topic - Interactive Rebasing for Clean Commit History

- Interactive Rebasing is a way to clean up commit history by squashing, reordering, and editing messages.
- It helps to remove unnecessary commit history
- Keeps the commit history clean and clear understandable format


# Steps Performed
1. Create a sample index.txt file.
2. git add . - initialize the repository and Staging the file
3. git commit -m "Initial content text file"
```
[main 2cc3cc5] Initial content text file
 1 file changed, 2 insertions(+)
 create mode 100644 Task-5/Index.txt
```

4. git add . - Staging the changed file

5. git commit -m "Added one more line"
```
[main 9ce42aa] Added one more line
 1 file changed, 2 insertions(+), 1 deletion(-)
```

6. git add . - Staging the changed file

7. git commit -m "Added another one more line"
```
[main 75fefd9] Added another one more line
 1 file changed, 2 insertions(+), 1 deletion(-)
```
8. git add .

9. git commit -m "Added last line" 

```
[main 5c3e575] Added last line
1 file changed, 2 insertions(+), 1 deletion(-)
```

10. git log --oneline - last 4 commit history
```
5c3e575 (HEAD -> main) Added last line
75fefd9 Added another one more line
9ce42aa Added one more line
2cc3cc5 Initial content text file
```

11. git rebase -i HEAD~4  - Represents the number of commits we want to modify
```
pick 2cc3cc5 Initial content text file
pick 9ce42aa Added one more line
pick 75fefd9 Added another one more line
pick 5c3e575 Added last line
```

12. After squash the commits 
```
pick 2cc3cc5 Initial content text file
squash 9ce42aa Added one more line
squash 75fefd9 Added another one more line
squash 5c3e575 Added last line
```

13. git rebase -i HEAD~4
```
[detached HEAD 2122d5c] Initial content text file
 Date: Wed Mar 19 20:40:28 2025 +0530
 1 file changed, 5 insertions(+)
 create mode 100644 Task-5/Index.txt
Successfully rebased and updated refs/heads/main.
```

14. git log --oneline
```
2122d5c (HEAD -> main) Initial content text file
```