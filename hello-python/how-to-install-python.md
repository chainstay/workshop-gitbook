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
Python 3.7.1 (default, Nov 30 2018, 14:09:15) 
[Clang 10.0.0 (clang-1000.10.44.4)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

Type `quit()` and press `return` to exit.

🔥Now you're cooking with gas! 🔥
{% endtab %}

{% tab title="Windows" %}

{% endtab %}
{% endtabs %}

{% hint style="success" %}
Once you have Python installed, you're almost ready to write some code!
{% endhint %}

