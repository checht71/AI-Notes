While you're using git, you should not mess around with your files using your file browser or it will cause issues with git and github. You need to make sure git knows about the changes that you are making to files to avoid issues.

### Renaming Files
Renaming files to be more descriptive is a great way to improve readability, but make sure to use this command instead of using the file browser.
```bash
git mv <old-filename> <new-filename>
```


### Moving directory location
Sometimes when you want to organize your file-system, you have to move the folders that contain your projects. You should also use `git mv` for this.

```bash
git mv <old-folder-name> <new-folder-path>
```

Example:
```bash
git mv project-folder-name /new/location/project-folder-name
```
