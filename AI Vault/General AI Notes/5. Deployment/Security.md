Keeping your deployment secure is an extremely high priority when it comes to deploying ML models. Here are some tips to help you keep everything more secure.


### Use Gitignore
Gitignore is something that you use so that github will never track specific files within your project. This is super helpful for sensitive files that contain things such as API keys. It is best practice to keep important and inflexible parameters such as API keys and filepaths within a json file that you include in `.gitignore.`
### 1. Avoid directly using file paths.
Usually you can load in a model or an image using a filepath you define within the code.
`my_file_path = "path/to/my/file"`
This is actually not a good thing to do for security. It can provide hackers with some information about your computer or indirectly expose security keys. The best thing to do to avoid this is to import these things using json files. You can include a template json file in your github code that other users can easily edit with their own info. This makes it easier for the end user and more secure for you.
