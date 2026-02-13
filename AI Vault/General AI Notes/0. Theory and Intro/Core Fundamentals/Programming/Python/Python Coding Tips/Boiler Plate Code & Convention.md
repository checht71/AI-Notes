
##### `if name  == "__main__":`
This makes the piece of code inside the statement only execute if you are specifically executing the code as the main module of the program.

##### utils.py
This file is found in many repositories. If you are reusing a ton of different functions in your code, it's good to store them in a single file that you can quickly import. This is supposed to make your workflow easier.
You can also break this down into a folder called `utils/`. Then you can have python files for specific utilities inside.

##### constants.py
This is where you can store the constants you use in your code so that you don't have magic numbers. This makes all of your code more readable and allows you to change your constants easily. Always name your constants something descriptive and never `*` import.