### Workflow Overview
##### 1. Create a new branch for a feature you want to implement
`git checkout -b "branch name"`
##### 2. Work on it and push to it
##### 3. Submit a pull request so someone can review your code (if you are part of a team)
go to github to do this
##### 4. Merge the branch with main and push the merged code to github

#### How to merge branches:
1. push your final updates to your branch
```
git push origin <my-branch>
```
2. Switch to main:
```
git checkout main
```
3. Update your local version of main with any changes others have made:
```bash
git pull origin main
```
4. Merge and resolve conflicts
```bash
git merge <feature-branch>
```
5. Push the merged version to main on github
```bash
git push origin main
```

