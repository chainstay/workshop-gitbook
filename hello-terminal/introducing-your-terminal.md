---
description: >-
  We'll be working with your computer's terminal a lot, today. Let's get
  introduced!
---

# Introducing: Your Terminal

## What's a terminal?

A terminal is another way to use your computer. Back in the 1980's, before Mac and Windows could show images on your monitor, everything was written in your terminal. Back then, the terminal and the computer were synonymous.

## Let's open your terminal

{% tabs %}
{% tab title="Mac" %}
1. Click the 🔍on the right-hand corner of your screen
2. Search for: Terminal
3. Open the Terminal application, it should look like the image below 

![The icon for your terminal](../.gitbook/assets/image%20%2810%29.png)
{% endtab %}

{% tab title="Windows" %}

{% endtab %}
{% endtabs %}

### Terminal 101

{% tabs %}
{% tab title="Mac" %}
1. You should see a `$`. This means that your computer is ready to accept a command, as text.
2. Type `cd ~/Documents` and press `return` on your keyboard.
3. Now type `ls` and press `return`.
4. You should see the contents of your `Documents` folder.
5. Lastly, run the command `pwd`

#### What just happened?

We ran three commands. The first command was `cd`, which is short for "Change Directory". When you see "Directory" think "Folder". Your terminal is always "in" one directory at a time. Commands that you run will execute "within" that directory.

Our second command `ls`, is short for "list". By default, `ls` will list the contents of your present working directory, or the current folder in your terminal. When we ran the command, your present working directory was the `Documents` folder in your `home` directory, or `~/Documents` for short.

{% hint style="info" %}
In the terminal, the ~ is a special character. It is a shortcut to your `home` directory. This is a good place to keep your files. You can always return to the home directory by typing `cd ~`, or just `cd`
{% endhint %}

Lastly, we ran `pwd`. That output something that looks like this:

```bash
$ pwd
/Users/YOUR_USERNAME/Documents
```

What you see there is a `file path`. File paths are what you will use to navigate in the terminal. As you learn more about programming, you'll grow much more comfortable with the terminal.
{% endtab %}

{% tab title="Windows" %}

{% endtab %}
{% endtabs %}

### Navigating between directories 

{% tabs %}
{% tab title="Mac" %}
1. Open your terminal and run the following commands: 
2. `cd`
3. `mkdir folder_1`
4. `cd ./folder_1`
5. `ls`
6. You should see nothing returned, that's good
7. `touch file_1.txt`
8. `ls`
9. You should see a new file, `file_1.txt`
10. `mkdir folder_2`
11. `cd folder_2`
12. `ls`
13. You're in an empty directory, so you should see nothing
14. `cd ..`
15. `ls`
16. Now, you're back in your `folder_1` directory
17. Confirm with `pwd`
18. `cd`
19. Now you're back in the home directory
20. `ls ./folder_1`
21. You should see your `file_1.txt` and `folder_2`

#### Phew.

Here's what just happened:

1. You created a new directory in your home `~` directory called `folder_1`
2. You entered the `folder_1` directory and created a file called `file_1.txt`
3. You created `folder_2` _within_ `folder_1`
4. You returned to your home directory

In this exercise, you practiced using `relative paths`. Contrary to `absolute paths`, relative paths are _relative to your present working directory_. Running a command with a single `.` will refer to your present working directory. On the contrary, running it with `..` refers to the _parent_ directory. In the example above, `folder_1` is the parent directory of `folder_2`, and `~` or `home` is the parent directory of `folder_1`.
{% endtab %}

{% tab title="Windows" %}

{% endtab %}
{% endtabs %}

{% hint style="success" %}
You should now have some basic familiarity with how to move around directories in the terminal. Don't worry if it still feels unclear, you'll get many opportunities to practice!
{% endhint %}

