
# Chapter 1: Introduction, Code Formatting, and Tools

PEP-8 establishes the convention that, when passing arguments by keyword to a 
function, we don't use spaces, but we do when we assign variables. For that
reason, we can adapt our search criteria (no spaces around the = on the first
search, and one space on the second) and be more efficient in our search.

## Docstrings and annotations

One important distinction; documenting the code is not the same as adding comments on it.
Comments are bad, and they should be avoided. By documentation, we refer to the fact of
explaining the data types, providing examples of them, and annotating the variables.

Having comments in the code is a bad practice for multiple reasons. First, comments
represent our failure to express our ideas in the code. If we actually have to explain why or
how we are doing something, then that code is probably not good enough.

### Annotations

The basic idea of them is to hint to the
readers of the code about what to expect as values of arguments in functions

    class Point:
        def __init__(self, lat, long):
            self.lat = lat
            self.long = long

        def locate(latitude: float, longitude: float) -> Point:
        """Find an object in the map by its coordinates"""
        

can get an idea of these expected types. Python will not check these types nor enforce them.

We can also specify the expected type of the returned value of the function. In this case,
Point is a user-defined class, so it will mean that whatever is returned will be an instance
of Point.

´__annotations__` This will give us access to a dictionary that maps the name of the
annotations (as keys in the dictionary) with their corresponding values,

**Type hinting with Mypy**

is the main tool for optional static type checking in Python.

it will analyze all of the files on your project,
checking for inconsistencies on the use of the types. This is useful since, most of the time, it
will detect actual bugs early, but sometimes it can give false positives.

instalation: 

    $ pip install mypy

for ignore false positive lineas: 
  
  type_to_ignore = "something" # type: ignore

**Checking the code with Pylint**

checking the structure of the code (basically, this is compliance with PEP-8) in Python, such as pycodestyle (formerly known as PEP-8),

    $ pip install pylint

Detect errores

It is possible to configure Pylint via a configuration file named pylintrc.
In this file, you can decide the rules you would like to enable or disable, and parametrize
others (for example, to change the maximum length of the column).

For fix automatically this linting errores there is a tool named "Black"

    pip install black



