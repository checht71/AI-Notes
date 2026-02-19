It is super important to write good commit messages.

The best practices to follow for good committing can be found on [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

Here's an overview:

### Simple Commit
```git
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

Examples:
```
feat(lang): add Polish language
```

```
feat(api)!: send an email to the customer when a product is shipped
```

```
fix: collision detection between player and asteroid
```

Here's the commit notes from VSCodium:
![[VSCodium_commits.png]]

### Multi-line commits
There are two ways to add multi-line comments to commits:
1. Don't use the `-m` tag.
Just use `git commit`. This will open a window for you that will allow you to write out a full commit message. When you're done, hit `ctrl + x`.

2. Use a ton of `-m` tags.
Every time you type `-m` after `commit`, you are creating a new line in your commit message. This allows you to give much more detailed update logs.
 
``` bash
git commit -m "Title" -m "Description." -m "More Description." -m "Trailer, or Footer, or whatever."
```


### Type
type is used to specify what kind of update you are doing.
- **build**: Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
- **ci**: Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs)
- **docs**: Documentation only changes
- **feat**: A new feature
- **fix**: A bug fix
- **perf**: A code change that improves performance
- **refactor**: A code change that neither fixes a bug nor adds a feature
- **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- **test**: Adding missing tests or correcting existing test

### Scope:
The part of your code that your update is affecting. Optional. Must be put in parentheses.
Common examples:
- release
- core
- common
- upgrade
- **changelog**: used for updating the release notes in CHANGELOG.md


### Other Notes:
Write in imperative. Use _add_ instead of _added_ or _adds_.


[YouTube video on Conventional Comments](https://www.youtube.com/watch?v=OJqUWvmf4gg)