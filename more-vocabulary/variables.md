# Variables

## Variables store data

You've already used them in your `for` loops! For example:

```python
for number in range(1000):  # define the variable: number
    print(number)           # reference the variable: number
```

In the above `for` loop, `number` is a variable. `for` loops work by storing a value for a specific _iteration_ of the loop.

You don't need a `for` loop to use variables, you can define your own!

## Define your own variables

```python
my_variable = 'some data'  # define your first variable
print(my_variable)         # reference it in the print function

my_name = 'David'          # define a new variable
print(my_name)             # reference that one too!

print(my_variable)         # refernece your first variable, too!

some_number = 55           # variables can store anything
a_big_number = 100000 * 2 
hackathon = 'Hack' + 'Her' + '413'

print(some_number)
print(a_big_number)
print(hackathon)
```

## Changing variables

```python
a_number = 1  # lets start low
print(a_number)
a_number = a_number + 1  # and bump up our value, a little
print(a_number)

a_number = a_number * 100
print(a_number)
```

