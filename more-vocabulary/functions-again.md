# Functions \(again!\)

## Write your own function

Make a new file!

{% code title="my\_function.py" %}
```python
def say_hello():    # define your function
    print('hello')
    

say_hello()         # call your function
```
{% endcode %}

This function:

* Has no arguments
* Does one thing

## Something more useful

{% code title="my\_function.py" %}
```python
def say_hi_three_times():    # Write a new function
    print('hi')
    print('hi')
    print('hi')
    

say_hi_three_times()         # Notice, we call the function by its name
```
{% endcode %}

This function:

* Has no arguments
* Does one thing... three times

## DRY up your code

{% hint style="info" %}
DRY stands for "don't repeat yourself"
{% endhint %}

{% code title="my\_function.py" %}
```python
def say_hi_three_times():
    for i in range(3):     # Loops are great!
        print('hi')
    

say_hi_three_times()
```
{% endcode %}

## Something more flexible

{% code title="my\_function.py" %}
```python
def say_hi(num_times):          # Our first argument!
    for i in range(num_times):
        print('hi')
    

say_hi(3)                       # It does the same thing as before :)
```
{% endcode %}

This function:

* Accepts 1 argument
* Does one thing _any number of times_

{% hint style="info" %}
What happens when you change the number passed to `say_hi`? Formulate your hypothesis, test it, and observe the results.
{% endhint %}

## Even MORE FLEXIBLE

{% hint style="warning" %}
This one is a challenge. YOU GOT THIS.
{% endhint %}

{% code title="my\_function.py" %}
```python
def repeat_after_me(phrase, times):
    for i in range(times):
        print(phrase)

repeat_after_me('hi', 3)
```
{% endcode %}

{% hint style="info" %}
Notice how our function name describes _everything_ that happens in the function.
{% endhint %}



