---
description: And what does code even do?
---

# What is a Programming Language?

## What is code?

Code is like a recipe for computers. It's a _specific_ set of _instructions_ in a _language_. There is a lot to learn in a programming language, so let's focus on a very small portion: the `print` function.

Let's take the following example and break it down:

```python
print('Hello, world')
```

Can you read this code and guess what it might do?

We can see a blue word: `print` with a set of `()` immediately following. Enclosed in those parentheses is a phrase surrounded by `''`: `Hello, world`.

{% hint style="info" %}
You'll see the phrase `Hello, world` a lot in programming. [Here's why](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program)!
{% endhint %}

* `print`: This is called a `function`. For now, think of a `function` like a shortcut. The `print` function is a shortcut for:
  1. Take the text I just gave you, in this case `'Hello, world'`
  2. Get ready to write that text on the screen
  3. Write the text to the screen
  4. Stop writing text to the screen
* `()`: These parentheses contain the `arguments` given to the function. For now, think of `arguments` as customizations.
  * If your code is `print('dog')`: your program will write "dog" on your screen
  * If your code is `print('cat')`: your program will write "cat" on your screen
  * If your code is `print('I wrote Python code')`: your program will write "I wrote Python code" on your screen
* `''`: These quotes create what's called a `string`. Strings let you tell the computer to differentiate between code, and words.
  * For example `print` is a function, but `'print'` is a string. Python will execute the `print` function, but it will not execute the `'print'` string, it will treat it as data.
* `'Hello, world'`: This is a `string` with the value `Hello, world`. 
  * Strings can have almost any text value, you will get a lot of practice with strings later in the workshop.

{% hint style="warning" %}
If this is your first time learning these concepts, they may not make sense. That's perfectly normal, these things take time to learn. You may want to take a quick detour to practice writing `print` statements with different `string` values here in this [Python sandbox](https://www.python.org/shell/).
{% endhint %}

![You may want to take some time practicing with print statements. Use the link above.](../.gitbook/assets/image%20%2816%29.png)

{% hint style="success" %}
Feel free to move on even if this material doesn't make complete sense. We'll be reinforcing these ideas all throughout the workshop. Just remember the following core concepts:

* A `function` is a set of one or more instructions, in code
* A `function` can be customized with`arguments`
* A `string` is a set of one or more letters that is treated as data, not as code
{% endhint %}

## Why is code important?

Everything that a computer does is controlled by code. _Everything_. Every time you press a key on your keyboard, or scroll on this web page, there are _over 100,000 lines_ of lines of code that are run. Thankfully, you'll be benefiting from the work of those who came before you.

The software that we'll be using in this workshop simplifies the creation of a web server. You'll have everything you need to experiment, batteries-included.

Once you grow more comfortable with writing and running code, you'll have everything you need to _contribute_ to the Internet itself. Your contribution will go beyond an Instagram post, or a Tweet. You will be making the internet _larger_ by adding another server to the network.

{% hint style="success" %}
You can do amazing things with code, expanding the reach of the Internet itself.

Let's learn how.
{% endhint %}

