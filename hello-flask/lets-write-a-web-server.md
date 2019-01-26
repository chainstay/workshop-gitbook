---
description: It's time to write some code.
---

# Let's Write a Web Server!

## Your first Python file

{% hint style="warning" %}
By this point, you should have a few things ready to go:

* Python installed on your computer
* Basic familiarity with your `terminal`
* Success installing `packages` with `pip`
* The ability to run Python in your terminal, with the `python3` command

If you don't have all of these pre-requirements ready to go, refer back to previous articles or ask for help. You'll need all four requirements to proceed.
{% endhint %}

During this workshop, we'll be working with `Flask`. Flask is a `web framework`, used to simplify the process of creating a web server. It does one job very well: translate `HTTP` `requests` to python code, then translate python code to `HTTP` `responses`.

{% hint style="info" %}
For a refresher on HTTP requests and responses, look back to [What is a web server?](../hello-world/what-is-a-web-server.md)
{% endhint %}

Let's create a new directory to store your project.

{% hint style="warning" %}
We're going to be typing a lot of commands in your terminal. To save space, the commands will be explained with `# code comments`. If you're typing commands yourself, you don't have to type the `#` or anything after it.

For example:

`cd my_folder  # make my_folder your present working directory`

In the above example, you only have to type `cd my_folder`.
{% endhint %}

{% tabs %}
{% tab title="Mac" %}


```bash
cd  # start from your home directory
mkdir flask_workshop # create a directory for your code
cd flask_workshop # enter your new directory, so you can work in it easily
touch app.py # by convention, Flask applications are named app.py
```

Now use your preferred text editor to open your new `app.py` file.
{% endtab %}

{% tab title="Windows" %}
```bash
# start from your code directory
cd C:\code
# create a new file for your Python code
# by convention, Flask applications are named app.py
echo. > app.py
```

Now use your preferred text editor to open your new `app.py` file.

{% hint style="warning" %}
If you are using Notepad as your text editor, you may not see `app.py` when you look into your `C:\code` directory. This is usually because Notepad, by default, only looks for `.txt` files and not `.py` files. Make sure that you are opening "All Files" and not just "Text Documents".
{% endhint %}
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Python files have their own extension: `.py`. You'll also see the `.pyc` extension after you run your code, but these files can be ignored for now. Any Python file you write should have the `.py` file extension at the end.
{% endhint %}

Write the following code in your `app.py` file. **Remember** that the `# code comments` are for you, the coder. They are ignored by Python, and don't have to be written in your `app.py` file.

{% code-tabs %}
{% code-tabs-item title="app.py" %}
```python
from flask import Flask  # Here, we load the Flask python package

# Now, let's create our app. A Flask application is created by running
# Flask(__name__) and assigning it to a variable. In this case: app
app = Flask(__name__)

# Now that our server is created, let's configure it.
# First, we'll create a server path.
# Our first path will be '/say_hello'
@app.route('/say_hello')  # This is how you create a path in Flask
def hello():  # Here, we create a function for the /say_hello path
    # Any code indented by four spaces from this point on will run
    # when a client requests our server at the '/say_hello' path

    # We want to make sure everything is working, so let's return
    # some data!
    # Flask will take the data after return, and translate it into
    # an HTTP response.
    return 'Hello, World!'
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Running your server

In order to run our server, we'll need the `Flask` package. Install it using your `terminal` like so:

{% tabs %}
{% tab title="Mac" %}
`pip install Flask`
{% endtab %}

{% tab title="Windows" %}
`py -m pip install Flask`
{% endtab %}
{% endtabs %}

Now that you have your first server written, let's run it!

```bash
flask run
 * Environment: production
   WARNING: Do not use the development server in a production environment.
   Use a production WSGI server instead.
 * Debug mode: off
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```

Your server is running! If you see the same thing in your terminal, you can access your server by entering this URL into your browser: 

```bash
http://127.0.0.1:5000/say_hello
```

You should see something like this:

![](../.gitbook/assets/image%20%283%29.png)

If you look at your terminal, you'll see a log of the request. You'll also notice an `http` `method`, `path`, and `status code`.

```bash
127.0.0.1 - - [CURRENT_DATE CURRENT_TIME] "GET /say_hello HTTP/1.1" 200 -
```

{% hint style="success" %}
If you can access your server and see "Hello World!", you're ready to move on.
{% endhint %}

![Yes, you can!](../.gitbook/assets/image%20%2816%29.png)

