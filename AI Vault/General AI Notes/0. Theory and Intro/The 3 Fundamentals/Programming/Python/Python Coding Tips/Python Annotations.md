This article covers the `->` symbol in python. It can be a little confusing to see at first, but it turns out that it's actually just purely for documentation purposes and has no impact whatsoever on the code.
```python
def example_function() -> str:
    return "Hello, world!"

result = example_function()
print(result)  # Output: Hello, world!
```

it also literally does not matter what the actual output type is when you run the code, it will still run even if it does not match your annotation.
```python
def example_function() -> str:
    return 1.026

result = example_function()
print(result)  # Output: 1.026
```

>[!tldr] TL;DR
>The only point of annotations are to let other developers know the output type of a function so they do not waste time writing `print(type(my_output))` to figure it out.

