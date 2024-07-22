[Video on getting started](https://youtu.be/RGOj5yH7evk)
[W3 Tutorial](https://www.w3schools.com/git/git_new_files.asp?remote=github)
## Overview

> [!abstract] What is Github?
> Github is a version management tool. This allows programmers to download versions of a project, make changes to them, and then upload those changes and merge them together into a single cohesive project.

### Terminology
Repo/Repository - An online folder that you upload your code to.
Fork - Create a completely different project from an existing project.
Branch - Create a new version of an existing project.
Clone - Download a project to work on it locally
Commit
Pull - Download the latest version of a project to a local copy.
Push - update main project

> [!info] Git vs Github
> Git and github are separate things. Git is a language for version control management. Github makes tools that use Git.

# Using Git Commands

## Publish Repository
1. Navigate to a folder where you are keeping your code.
2. Initialize Git
```bash
git init
```
Doing this will create a repository. This means that there is now a hidden folder keeping track of changes that you make to the code.
## Check Which Files are Being Tracked
Just because you create a repository does not mean that every file is necessarily being tracked. New files you create after running Git init may be seen by git, but changes to these files will not be recorded. To double check which files are being tracked use the following command:
```bash
git status
```
If a file is missing, you can add it to the tracked files using:
```bash
git add <filename>
```

you can also say `git add .` to add everything in your current file directory
## Create a Branch
[Source](https://akrabat.com/the-beginners-guide-to-contributing-to-a-github-project/)

```bash
git remote add origin <link to repo>
```

Pull files from the cloud to your local branch:
```bash
git pull origin master
```
Note: sometimes if you pull from a repo that you have included a license in it will give you an error. You can still pull from it with the `--allow-unrelated-histories` tag.
```bash
git pull origin main --allow-unrelated-histories

```


Commit your changes with a message
```bash
git commit -m "First release of Hello World!"
```

Push files from your local branch to the cloud:
```bash
git push -u origin master
```

Download a new copy of your repo:
```bash
git clone <repo>
```

## "Debugging"
### Force Push
Sometimes when pushing it will spazz out when you try and upload modified files. If you want to force push and overwrite what's in the remote, use the following command:
```bash
git push --set-upstream origin master --force
```

### Master -> Main
Sometimes github will set up the local version of a repo as "master" when you initialize it. This is an old convention and should be changed to "main", which is what the online repo will use. You can switch it over using the following command:
```bash
git branch -m master main
```