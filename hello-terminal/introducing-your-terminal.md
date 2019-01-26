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

![The icon for your terminal](../.gitbook/assets/image%20%2811%29.png)
{% endtab %}

{% tab title="Windows" %}
![](../.gitbook/assets/image%20%287%29.png)

1. Press the `Windows` key
2. Type `cmd`
3. Click on `Command Prompt`
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

Our second command `ls`, is short for "list". By default, `ls` will list the contents of your present working directory, that is, the current folder in your terminal. When we ran the command, your present working directory was the `Documents` folder in your `home` directory, or `~/Documents` for short.

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
1. You should see a `C:\Users\YOUR_USERNAME`. This means that your computer is ready to accept a command, as text.
2. Type `cd C:\` and press `enter` on your keyboard.
3. Type `dir` and press `enter`.
   1. At this point, you should see some familiar directories, e.g. `Program Files`
4. Now type `mkdir code` and press `enter`.
5. Run the `dir` command again
6. You should see a new directory, called `code`

#### What just happened?

We ran three commands. The first command was `cd`, which is short for "Change Directory". When you see "Directory" think "Folder". Your terminal is always "in" one directory at a time. Commands that you run will execute "within" that directory.

Our second command `dir`, is short for "directory". By default, `dir` will list the contents of your present working directory, that is, the current folder in your terminal. When we ran the command, your present working directory was the `code` folder in your `root` directory.

Lastly, we ran `chdir`. That output something that looks like this:

```bash
C:\>chdir
C:\
```

What you see there is a `file path`. File paths are what you will use to navigate in the terminal. As you learn more about programming, you'll grow much more comfortable with the terminal.
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
1. `cd C:\code`
2. `mkdir folder_1`
3. `cd ./folder_1`
4. `dir`
5. You should see `0 File(s)`, that's good
6. `echo. > file_1.txt`
7. `dir`
8. You should see a new file, `file_1.txt`
9. `mkdir folder_2`
10. `cd folder_2`
11. `dir`
12. You're in an empty directory, so you should see no files
13. `cd ..`
14. `dir`
15. Now, you're back in your `folder_1` directory
16. Confirm with `chdir`
17. `cd C:\code`
18. Now you're back in the `code` directory
19. `dir ./folder_1`
20. You should see your `file_1.txt` and `folder_2`

#### Phew.

Here's what just happened:

1. You created a new directory in your `root` directory called `folder_1`
2. You entered the `folder_1` directory and created an empty file called `file_1.txt`
3. You created `folder_2` _within_ `folder_1`
4. You returned to your home directory

In this exercise, you practiced using `relative paths`. Contrary to `absolute paths`, relative paths are _relative to your present working directory_. Running a command with a single `.` will refer to your present working directory. On the contrary, running it with `..` refers to the _parent_ directory. In the example above, `folder_1` is the parent directory of `folder_2`, and `C:\` or `root` is the parent directory of `folder_1`.
{% endtab %}
{% endtabs %}

{% hint style="success" %}
You should now have some basic familiarity with how to move around directories in the terminal. Don't worry if it still feels unclear, you'll get many opportunities to practice!
{% endhint %}

