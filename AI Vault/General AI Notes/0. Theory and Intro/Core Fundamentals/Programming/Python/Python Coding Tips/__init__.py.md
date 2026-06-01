These files help with imports.

They will run whenever you import something within the same folder as it.

## Where to put __init__
You don't need to put these in every subfolder. All you need to do is place them at the top level
```
myproject
\ func
  - __init__.py
  - func1.py
  - func2.py
    \ subfolder
      - func3.py

\  classes
  - __init__.py
  - class.py
```
Notice how I don't need an init file for my subfolder with `func3.py`.  It's encapsulated by the higher level init.

## Using init from a top level folder
You need a *relative import*. This will tell python where to look.
Lets say that I have a module named `myfunc` in `a.py`. If my `__init__.py` is in the same folder, which is named `myfolder`, I would write the following line to add that to the package:
```python
from .a import myfunc
```

Now I can go to a script in a different folder and import like this:

```python
from myfolder import myfunc
```


### Importing to a sub-folder
Lets say that instead of my `main.py` in my root folder, I want to import *to* a module deep in my folder hierarchy *from* something higher up. You need a different type of relative import.



[Video Link](https://www.youtube.com/watch?v=VEbuZox5qC4)