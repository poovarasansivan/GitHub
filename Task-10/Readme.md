# Topic - Working with Forced Pushes and RecoveryObject

- Learned about how to recover the lost commit history with reflog.

# Steps Performed

1. Created a repository and configured it will local project folder.
2. Created a sample text file and pushed it on remote repository using main branch.
3. Created a Three new branches(feature-branch,bux-fix,release-branch) other than main branch.
3. Committed and pushed this all branches into remote repository.
4. Modified the text file and pushed it into remote repository using feature branch.
5. Again modified the text file and pushed it into remote repository.
6. Now deleted the last commit history with a help of a command ```git reset --hard HEAD~1 ```
7. Pushed the changes to remote repository by stagging and committing it.
8. Now using a ```git reflog``` to see all the commit history with hashes. 
9. Finding the lost commit hash and used to recover the commit with the help of ```git reset --hard 644ae33```
10. Finally pushing the recovered commit history to the remote repository.

# Commands

``` 
git add . 
``` 
- To Stage the changes into local repository.

``` 
git commit -m "message" 
```
- To commit the stagged changes into local repository.

``` 
git push origin main 
```
- To Push the local repository content to remote repository.

```
git reset HEAD~1
```
- To Delete the Last commit history and data.

```
git reflog
```
- To find the lost commit history hash and data.

```
git reset --hard <hash>
```
- To recover the lost commit history and data.

```
git push origin main
```
- Updates the recovered data and commit history to remote repository.


# Why forced pushes needs to be handled with care?
- Forced pushes needs to be handled with care because it can overwritte remote commits and cause irreversible data loss for collaborators.
- It have a risk of overwritting others work and cause a loss of work and data.
- Loss of commit history make it difficult to track changes.
- To overcome this need to use ```git push --force-with-lease``` to protect other collaborators work.

# How Git Reflog Becomes a Lifesaver?
- Git Reflog (Reference Log) is a lifesave when historys are rewritted, accidental reset, and performing a commit with force push. 
- It also helps to recover from mistakes like forced pushes, resets.

# Best Practices for collaborators.
- Always suggested to use a ```git push --force-with-lease``` instead of ```git push --force```. Because it will helps to protect other collaborators work.