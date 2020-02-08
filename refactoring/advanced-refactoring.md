# Advanced refactoring

If I were going to write this function at work, this is how I would write it.

```python
def do_math(base, modifier, operation):
    if operation == 'add':
        return base + modifier
    elif operation == 'multiply':
        return base * modifier
    elif operation == 'subtract':
        return base - modifier
    elif operation == 'divide':
        return base / modifier
    else:
        raise ValueError(f'Operation "{operation}" is not supported')

print(do_math(2, 2, 'multiply'))
print(do_math(2, 2, 'add'))
print(do_math(25, 5, 'subtract'))

# This will cause an error, which is a good thing, in this case
do_math(1, 1, 'NOT MATH')
```

Now you compose multiple functions together!

```python
print(do_math(do_math(2, 2, 'add'), do_math(2, 2, 'add'), 'add'))
8  # (2 + 2) + (2 + 2)! 
```



