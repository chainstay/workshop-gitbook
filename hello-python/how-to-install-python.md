---
description: Let's make sure you can run Python code on your computer
---

# How to Install Python

## Let's install Python

{% tabs %}
{% tab title="Mac" %}
{% hint style="warning" %}
Homebrew is the easiest install method for Python, but things can still go wrong. If while following these steps you see something that doesn't look quite right, please ask for help!
{% endhint %}

#### Install Homebrew

{% hint style="info" %}
Homebrew is what programmers call a "Package Manager". It's purpose is to simplify the process of running other people's code. It can also be used to install programming languages, like Python.
{% endhint %}

1. Open your `terminal` \([return here](../hello-terminal/introducing-your-terminal.md) if you need help with this step\)
2. You may need to install OSX Developer Tools. Run the following command: `xcode-select --install`. You'll get an error if it's already installed, but you can proceed nonetheless.
3. Run the following command to install Homebrew: 

```text
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Once that finishes, you should have Homebrew installed.

You can confirm by running `brew --version` in your terminal. Your output should look similar to this:

```bash
$ brew --version
Homebrew 1.8.6
Homebrew/homebrew-core (git revision 90e693; last commit 2018-12-19)
Homebrew/homebrew-cask (git revision 859b1; last commit 2018-12-19)
```

#### Install Python

Now that Homebrew is installed, we can use it to install Python.

In your terminal, run `brew install python3`

Let that run, it will take some time. Once it completes, run `python3`

```bash
$ python3
Python 3.7.1 (default, CURRENT_DATE, CURRENT_TIME) 
[Clang 10.0.0 (clang-1000.10.44.4)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

Type `quit()` and press `return` to exit.

🔥Now you're cooking with gas! 🔥
{% endtab %}

{% tab title="Windows" %}
The easiest way to install Python on Windows is to use the installer published by the Python maintainers.

1. Go to this link: [https://www.python.org/downloads/release/python-372/](https://www.python.org/downloads/release/python-372/)
2. Scroll down to `Files` and select `Windows x86-64 executable installer`
3. Wait until the installer finishes downloading, then run it
4. In the installer, **check** `Add Python 3.7 to PATH` and **uncheck** `Install launcher for all users`

Let that run, it will take some time. Once it completes, run `py` in your `terminal` 

```bash
C:\>py
Python 3.7.2 (tags/v3.7.2:9a3ffc0492, CURRENT_DATE, CURRENT_TIME) [MSC v.1916 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

Type `quit()` and press `enter` to exit.

🔥Now you're cooking with gas! 🔥
{% endtab %}
{% endtabs %}

{% hint style="success" %}
Once you have Python installed, you're almost ready to write some code!
{% endhint %}

