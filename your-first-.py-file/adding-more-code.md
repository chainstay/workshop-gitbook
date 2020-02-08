# Adding more code

Now that you have a file that you can modify, let's add some more code.

{% hint style="warning" %}
When you're writing code from this workshop, don't worry about copying the comments into your own files, they're for instructional purposes.

That said, I encourage you to write your own comments that are meaningful to you!
{% endhint %}

{% code title="code.py" %}
```python
print('I can count to 10!')
# don't worry, 11 is not a typo!
for number in range(11):
    print(number)
    
print('and I know the alphabet!')
for letter in ('abcdefghijklmnopqrstuvwxyz'):
    print(letter)
```
{% endcode %}

Save and run that file the same way as before

{% tabs %}
{% tab title="Mac" %}
```bash
python3 code.py
```
{% endtab %}

{% tab title="Windows" %}
```
python3.8 code.py
```
{% endtab %}
{% endtabs %}







