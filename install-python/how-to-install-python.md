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
Homebrew is what programmers call a "Package Manager". Its purpose is to simplify the process of running other people's code. It can also be used to install programming languages, like Python.
{% endhint %}

{% hint style="warning" %}
If this is your first time installing software using your terminal, you may be confused when your computer asks for your password. When it does, type in your computer's login password. Even though you won't see characters appearing in your terminal, they are in fact being entered. Press `return`, once you've entered all the characters of your password, to proceed.
{% endhint %}

**Open your `terminal`** \([return here](introducing-your-terminal.md) if you need help with this step\)

**You may need to install OSX Developer Tools**. Run the following command: `xcode-select --install`. You'll get an error if it's already installed, but you can proceed nonetheless.

{% hint style="info" %}
When running `xcode-select` you may see some popups outside of your terminal. These are perfectly normal, go ahead and click through them to install `xcode-select`.
{% endhint %}

**Copy-paste the following command, in its entirety, to install Homebrew**. You can copy the whole command by clicking the gray box to the right-hand side of the text below.

```text
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Once that finishes, you should have Homebrew installed.

**You can confirm by running `brew --version`** in your terminal. Your output should look similar to this:

```bash
$ brew --version
Homebrew 1.8.6
Homebrew/homebrew-core (git revision 90e693; last commit 2018-12-19)
Homebrew/homebrew-cask (git revision 859b1; last commit 2018-12-19)
```

#### Install Python

Now that Homebrew is installed, we can use it to install Python.

In your terminal, run `brew install python3`

Let that run, it will take some time. Once it completes, run `python3` from any directory in your `terminal`

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
The easiest way to install Python on Windows is to use the Microsoft Windows store.

1. Press the `Windows` key, or click the Windows Icon at the bottom left-hand corner of your screen
2. Type `store` and press `enter`
3. Search for Python 3.8. Install it!

![](../.gitbook/assets/image%20%2818%29.png)

Once the installation is finished, run `python3.8` from any directory in your `terminal` 

```bash
C:\Users\YOUR_USERNAME>python3.8
Python 3.8.1 (tags/v3.8.1:1b293b6, TODAY'S DATE) [MSC v.1916 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

Type `quit()` and press `enter` to exit.

🔥Now you're cooking with gas! 🔥
{% endtab %}
{% endtabs %}

{% hint style="success" %}
Once you have Python installed, you're ready to write some code!
{% endhint %}



