# Python Code Style Guide

## Principles

1. [PEP-8 Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/)
1. [Explicit is better than implicit](https://www.python.org/dev/peps/pep-0020/)
1. [Do not repeat yourself](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)
1. [Keep things simple](https://en.wikipedia.org/wiki/KISS_principle)
1. [Keep things intuitive](https://en.wikipedia.org/wiki/Principle_of_least_astonishment)
2. [SOLID](https://en.wikipedia.org/wiki/SOLID)
3. [The Twelve-Factor App](https://12factor.net/)

## Code

1. Always prefer code maintainability and readability even if this might sacrifice some performance.
1. [Google Python Style Guide](https://google.github.io/styleguide/pyguide.html)
1. Keep functions and methods ideally less than 25 lines.
1. Maintain methods lowest cyclomatic complexity: avoid `if` statements when possible (write branchless code), never use nested `if`. Be [Never Nester](https://www.youtube.com/watch?v=CFRhGnuXG-4).
1. Don't concatenate strings with `+` it's [unprofessional, error-prone, slower](https://codecalamity.com/stop-using-plus-signs-to-concatenate-strings/), and might be confusing, prefer f-string or `"".join()`.
1. [The lesser indent your code has, the better](https://www.youtube.com/watch?v=CFRhGnuXG-4). 
1. Use `isort`, and `black` to format your code.
1. Use `pylint`, and `mypy` to check your code.

### Method signature

1. A method signature where the order of arguments "does not matter" (e.g. args are the same type) or the order is obvious is good for positional arguments:

```python
def add(a: float, b: float) -> float: ...
```

2. A method that expects non-interchangeable arguments is a good case to enforce keyword arguments, which will remove any ambiguity or wondering what should come first when calling the method:

 ```python
def set_token(self, *, domain: str, token: str, expires_in: int) -> None: ...
```

3. For a method around something you can combine positional and keyword arguments, using one positional for "something" and keyword arguments for everything else:

```python
def get_instance(self, instance_id: int, *, include_inactive: Optional[bool] = False) -> T: ...
```
