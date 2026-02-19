[video1](https://www.youtube.com/watch?v=iiQifErhGAM)  [video2](https://www.youtube.com/watch?v=7oZBfpI_hxI)

## Dictionary of constants
If you are using a lot of repeated attributes such as the color of a button or text size in Tkinter, you can make a dictionary object in a separate folder, import it to your main file, then just reference the dictionary once and it will pass in all of the attributes you want to an item. This is very similar to a styles guide.

Don't use magic numbers.

## Consistency
Use consistent indentations, name conventions, and overall style.

## Convention
Use coding convention (PEP 8) [[https://peps.python.org/pep-0008/]]

## Bake in Intent
Try to make your code almost read like English. If you have some sort of function, name it what it does. If you have a long line of code that does something, but it is not super clear to another person what it may do, put it in a function that describes it. It should be so that a person who does not even know how to code can read over your work and get some kind of an idea about what's going on. Include units in the names of your variables if applicable.

## Cut out the Fat
If you bake in your intent and make all of your functions and variable names super readable, you will never need a comment to explain what something is doing.

## Docstrings
A [docstring](https://peps.python.org/pep-0257/) is a multi-line comment in python. Usually you put it at the top of your python file or in the first line of a function. Conventionally, a docstring will state the purpose of your function first, then what the inputs and outputs are.

Example:
```python
def complex(real=0.0, imag=0.0):
    """Form a complex number.

    Keyword arguments:
    real -- the real part (default 0.0)
    imag -- the imaginary part (default 0.0)
    """
    if imag == 0.0 and real == 0.0:
        return complex_zero
    ...
```

While your code should be as self explanatory as possible, it can save you even more time to just read the docstring and see what is going on without even checking the code.

### Use OOP
Create classes where it makes sense. Not only does this improve your organization and readability, but it also makes it easier to code. When you create a function, you can just pass the class into it instead of 100 variables that should belong to the class anyway.

Below is an example for a video game. I want to spawn a meteor on my screen. In order to do that, I need to know a lot of info about the meteor (dimensions, position, movement). All of this would need to be passed into the function and managed in my main file. 
As you can see just from the function, this is already looking messy.
```python
    def spawn(meteor_pos, meteor_width, meteor_height, meteor_drift, meteor_ydrift):
        meteor_pos.y = randint(-1000, -500)
        meteor_pos.x = randint(0, SCREEN_WIDTH)
        meteor_width = randint(50, 250)
        meteor_height = meteor_width + randint(-30, 30)
        meteor_drift = randint(-5, 5)
        meteor_ydrift = randint(-5, 3)
```

Now if I define a class `meteor` and give it all of these parameters, all I need to do is pass `self` (if it is a function within the class, otherwise I would pass in `meteor`).
```python
    def spawn(self):
        self.pos.y = randint(-1000, -500)
        self.pos.x = randint(0, SCREEN_WIDTH)
        self.width = randint(50, 250)
        self.height = self.width + randint(-30, 30)
        self.drift = randint(-5, 5)
        self.ydrift = randint(-5, 3)
```