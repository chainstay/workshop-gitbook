# Conditionals

## If

{% code title="code.py" %}
```python
operation = 'add'
result = 1

if operation == 'add':
    result = result + 2

print(result)
```
{% endcode %}

{% code title="code.py" %}
```python
operation = 'multiply'  # try a different operation
result = 1

if operation == 'add':
    result = result + 2

print(result)
```
{% endcode %}

## If else

{% code title="code.py" %}
```python
operation = 'multiply'
result = 1

if operation == 'add':
    result = result + 2
else:                    # If not add, multiply instead
    result = result * 2

print(result)
```
{% endcode %}

## If else if!

{% code title="code.py" %}
```python
operation = 'multiply'
result = 1

if operation == 'add':
    result = result + 2
elif operation == 'multiply':  # Let's be more explicit :)
    result = result * 2
elif operation == 'subtract':   # Now we can support more operations!
    result = result - 2
elif operation == 'divide':
    result = result / 2
else:
    print("I don't know how to do that!")

print(result)
```
{% endcode %}

