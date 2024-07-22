It is super important to write good commit messages.

The best practices to follow for good committing can be found on [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

Here's an overview:

### Simple Commit
```git
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

Example:
```
feat(lang): add Polish language
```

```
feat(api)!: send an email to the customer when a product is shipped
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