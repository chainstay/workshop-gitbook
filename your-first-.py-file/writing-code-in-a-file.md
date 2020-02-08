# Writing code in a file

Writing code in your terminal works great for small amounts of code, but what if you want to save your work?

## Enter the .py file

When you write code, you will write it in a file with a Python-only file extension `.py`

Open the text editor that you installed earlier in the workshop, and write a new file.

{% code title="code.py" %}
```python
print('hello code.py')
```
{% endcode %}

Save that file as `code.py` in a place that you can remember.

Now, using your terminal, find that file

{% tabs %}
{% tab title="Mac" %}
```bash
ls
```
{% endtab %}

{% tab title="Windows" %}
```text
dir
```
{% endtab %}
{% endtabs %}

Once you've found your file, open it _using the Python programming language._

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

{% hint style="success" %}
If you see `hello code.py` in your terminal, congrats! You've now _written and run_ your first Python program.
{% endhint %}

