---
description: >-
  Packages are bundles of code written by other people. They're very important
  when coding with Python.
---

# How to Install Packages

## Installing your first Python Package

We'll be using a package called `Flask` to do most of our work today. But before we install Flask, let's have a little bit of fun.

### Introducing pip

`pip` is short for Python. It's an essential `terminal` command when working with Python code.

We need to make sure that `pip` is installed before we proceed. So run the following command in your terminal:

{% tabs %}
{% tab title="Mac" %}
`pip3 --version`

{% hint style="warning" %}
When referring to `pip`, we pronounce it pɪp or "pihp". However, the command you use to run `pip` will be different depending on how you install python.

For this workshop, use the `pip3` command to run `pip`.
{% endhint %}
{% endtab %}

{% tab title="Windows" %}
`py -m pip --version`

{% hint style="warning" %}
When referring to `pip`, we pronounce it pɪp or "pihp". However, the command you use to run `pip` will be different depending on how you install python.

For this workshop, use the `py -m pip` command to run `pip`. In other words, you run `python` with `py`, and you run `pip` with `py -m pip`.
{% endhint %}
{% endtab %}
{% endtabs %}

You should see a version number, similar to `10.0.1`.

### Install Asciimatics

You can use `pip` to install `packages` written by other Python developers. Let's install a Python package for making animations in your terminal.

{% tabs %}
{% tab title="Mac" %}
`pip3 install asciimatics`
{% endtab %}

{% tab title="Windows" %}
`py -m pip install asciimatics`
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Don't worry if you get a warning similar to: `You are using pip version ... however version ... is available.`

This warning is not important for the scope of this workshop, but feel free to ask about it if you're curious to learn more.
{% endhint %}



Now let's take a script that I wrote, and test that everything is working:

{% tabs %}
{% tab title="Mac" %}
Copy this command in its entirety, paste it into your terminal, and run it.

{% hint style="warning" %}
You can copy code blocks by clicking the rectangle box to the right of the visible text below.
{% endhint %}

```bash
curl -s https://raw.githubusercontent.com/chainstay/training-python-webserver/master/resources/hack_her_413_ascii.py > /tmp/ibeelong.py && python3 /tmp/ibeelong.py
```
{% endtab %}

{% tab title="Windows" %}
Copy this command in its entirety, paste it into your terminal, and run it.

{% hint style="warning" %}
You can copy code blocks by clicking the rectangle box to the right of the visible text below.
{% endhint %}

```bash
curl -s https://raw.githubusercontent.com/chainstay/training-python-webserver/master/resources/hack_her_413_ascii.py > C:\code\ibeelong.py && py C:\code\ibeelong.py
```
{% endtab %}
{% endtabs %}

{% hint style="success" %}
Alright! Once you can get the script above to work, your Python installation is good to go.
{% endhint %}

