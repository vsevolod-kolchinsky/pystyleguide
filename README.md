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
1. Maintain methods lowest cyclomatic complexity: avoid `if` statements when possible (write branchless code), never use nested `if`.
1. Don't concatenate strings with `+` it's slower.
1. Prefer `operator.itemgetter`, `.attrgetter`, etc. to `lambda` due to speed.
1. The lesser indent your code has, the better.
1. Use `pyflakes`, `isort`, `black` to format your code


