# Python IDE hints

## PyCharm

### Suppress unwanted inspection comments

```python
# noinspection PyUnusedLocal
def load_tests(loader, tests, ignore):
    tests.addTests(doctest.DocTestSuite(somemodule))
    return tests
```

[Full list of directives](
https://www.jetbrains.com/help/pycharm/disabling-and-enabling-inspections.html#suppressing-comments
)

## Visual Studio Code

### `pylint` doesn't seem to work

Check the value of `python.linting.pylintUseMinimalCheckers`.
By default it is set to `true`. Change it to `false` to enable all messages.
[More here](https://code.visualstudio.com/docs/python/linting#_pylint).

### Suppress unwanted `pylint` messages

```python
# pylint: disable=unused-argument
def load_tests(loader, tests, ignore):
    tests.addTests(doctest.DocTestSuite(somemodule))
    return tests
```

[Full list of messages](
https://github.com/janjur/readable-pylint-messages/blob/master/README.md
)
