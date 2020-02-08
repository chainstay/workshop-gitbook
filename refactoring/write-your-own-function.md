# Make your code reusable

## Where are we so far?

So far, we have a nice little snippet of code that does very few things.

{% code title="code.py" %}
```python
operation = 'multiply'
result = 1

if operation == 'add':
    result = result + 2
elif operation == 'multiply':
    result = result * 2
elif operation == 'subtract':
    result = result - 2
elif operation == 'divide':
    result = result / 2
else:
    print("I don't know how to do that!")

print(result)
```
{% endcode %}

## Let's refactor

{% hint style="info" %}
Refactoring means: "Change code without changing functionality." Your code should be _able_ to do the exact same thing before and after refactoring.
{% endhint %}

### Start with a function

{% code title="code.py" %}
```python
def do_math():
    operation = 'multiply'
    result = 1

    if operation == 'add':
        result = result + 2
    elif operation == 'multiply':
        result = result * 2
    elif operation == 'subtract':
        result = result - 2
    elif operation == 'divide':
        result = result / 2
    else:
        print("I don't know how to do that!")

    print(result)

do_math()
do_math()
do_math()
```
{% endcode %}

{% hint style="success" %}
Now you can run the same code multiple times
{% endhint %}

### Add an argument

{% code title="code.py" %}
```python
def do_math(operation):
    result = 1

    if operation == 'add':
        result = result + 2
    elif operation == 'multiply':
        result = result * 2
    elif operation == 'subtract':
        result = result - 2
    elif operation == 'divide':
        result = result / 2
    else:
        print("I don't know how to do that!")

    print(result)

do_math('multiply')
do_math('add')
do_math('subtract')
```
{% endcode %}

{% hint style="success" %}
Now you can run it multiple times and achieve different results
{% endhint %}

### Choose the starting number

{% code title="code.py" %}
```python
def do_math(base, operation):
    if operation == 'add':
        result = base + 2
    elif operation == 'multiply':
        result = base * 2
    elif operation == 'subtract':
        result = base - 2
    elif operation == 'divide':
        result = base / 2
    else:
        print("I don't know how to do that!")

    print(result)


do_math(2, 'multiply')
do_math(5, 'add')
do_math(0, 'subtract')
```
{% endcode %}

### Choose a modifier



{% code title="code.py" %}
```python
def do_math(base, modifier, operation):
    result = None
    if operation == 'add':
        result = base + modifier
    elif operation == 'multiply':
        result = base * modifier
    elif operation == 'subtract':
        result = base - modifier
    elif operation == 'divide':
        result = base / modifier
    else:
        print("I don't know how to do that!")

    print(result)

do_math(2, 2, 'multiply')
do_math(2, 2, 'add')
do_math(25, 5, 'subtract')

```
{% endcode %}

{% hint style="success" %}
Look at THAT function! IT DOES THINGS!
{% endhint %}

