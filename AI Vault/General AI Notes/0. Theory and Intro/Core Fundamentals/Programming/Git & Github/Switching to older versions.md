Sometimes you want to check out another branch or an older version of the code. Here's how to do it the right way.

##### 1. Check and stash uncommitted changes
If you are in the middle of working on something you don't want to push, you can save a backup of your changes locally for later.

Check your uncommitted changes:
`git status`
Save them for later:
`git stash`
##### 2. Switch to an old version
Now we are going to look up and restore an old version of the code.

Look up old versions:
`git log`
Copy the hash of the version you want to restore.

Change your workspace to that version:
`git checkout <commit-hash>`
If you want to create a new branch from this version of the code:
`git checkout -b <new-branch-name> <commit-hash>`

Now you can test and work on this version of the code. It should automatically change when you `checkout`
##### 3. Return to your work
To return back you your work, switch back to your old branch and restore your changes
`git checkout <my-original-branch>`
`git stash apply`

That's it!