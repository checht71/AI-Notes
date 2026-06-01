Tells git what files and file types to ignore when committing.

### Creating a gitignore file
Simply go to your repo and create a new file called `.gitignore`

## Adding Files & Folders
Open `.gitignore` in any text editor.
###### Specific File:
To ignore a specific file, provide the path to it relative to `.gitignore`
In the same folder: `file_i_want_to_ignore.py`
In a subfolder: `folder/.../file_i_want_to_ignore.py`

###### File types
To ignore any file ending in an extension, just write out the extension with a `*` in front.
`*.png`
`*.jpeg`

###### Folders:
Just write `/` after the folder name. It's that simple.
`bin/`
`folder_i_hate/subfolder_i_hate/`

### Comments:
You can add comments for organization using `#`.
```
# Image Files
*.jpeg
*.jpg
*.png

# Other Stuff
folder/whatever
```

#### Some Things to Ignore:
__pycache__
Pycache files help a code execute more quickly when running on your computer, but they only take up space in your repo. Always add them to gitignore