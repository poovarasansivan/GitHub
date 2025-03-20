# Commands Learned

```
.gitignore
```

- This Command is used to ignore the file that should not be track by github.

```
 git status 
```
- This Command is used to check the status of files which is modified,added and deleted etc.

```
 git rm --cached filname
```
- To remote the uningored file from remote repository without deleting it locally

```
 git ls-files --ignored --exclude-standard -o 
```
- This Command is used to list out the ignored files

# Steps 

1. ```git init``` - Intialize the git repository.
2. ```git add . ``` - To add all the files in the current working directory. Added a image to the working folder and ignored it by using .gitignore.
3. ```git status``` - To check the status of the files.
4. ```git commit -m``` - To commit the changes from local to remote repository
5. ```git push origin main``` - To push the final changes to the remote repository