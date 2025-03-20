## Topic - Working with Remote Repositories and Collaboration

- Creating a Remote Collaborative Repository and work with branches, commit the work with a new branch, and make a pull request to perform code review and merge with the main branch.
- Learned how to work on collaborative projects and manage pull and merge requests. How to perform code reviews.

## Steps Performed

``` 
git add . 
```

- Staging the files of the current working directory.

```
git commit -m "Sample file added using main branch"
```
- Committed the staged content on the local repository.
```
git remote add origin main <repo_url>
```
- To configure the remote repository with the local repository.
```
git branch -M main
```
- Renaming the branch name from Master to main.
```
git push origin main
```
- Push the local files and content to the remote repository.
```git checkout -b feature-branch
```
- Created a new branch named feature-branch and switched to that branch. Then modified a file content.
```
git add .
```
- Performed stage to track the changes.
```
git commit -m "Modified content from feature branch"
```
- Committed the staged content.
```
git push origin feature-branch
```
- Pushed the changes to the remote repository using the feature-branch.
- Then navigated to the GitHub repository and checked for a pull request.

- Self-assigned the review and merged it with the main branch (message: New feature).
```
git pull origin main
```
- To pull the remote repository changes to the local repository (current working directory).