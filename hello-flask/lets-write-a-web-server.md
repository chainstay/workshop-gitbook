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
* The ability to open Python in your terminal, with the `python3` command for Mac, or the `py` command for Windows.

If you don't have all of these pre-requirements ready to go, refer back to previous articles or ask for help. You'll need all four requirements to proceed.
{% endhint %}

During this workshop, we'll be working with `Flask`. Flask is a `web framework`, used to simplify the process of creating a web server. It does one job very well: translate `HTTP` `requests` to python code, then translate python code to `HTTP` `responses`.

{% hint style="info" %}
For a refresher on HTTP requests and responses, look back to [What is a web server?](../hello-world/what-is-a-web-server.md)
{% endhint %}

Let's create a new directory to store your project.

{% hint style="warning" %}
We're going to be typing a lot of commands in your terminal. To save space, the commands will be explained with `# code comments`. **If you were to type the command below, you would only need to type `cd my_folder`**

`cd my_folder  # create my_folder your present working directory`
{% endhint %}

{% tabs %}
{% tab title="Mac" %}
```bash
cd  # start from your home directory
mkdir flask_workshop # create a directory for your code
cd flask_workshop # enter your new directory, so you can work in it easily
echo "# write your code here" > app.py  # this is where your code will be written
```

Now use your preferred text editor to open your new `app.py` file.
{% endtab %}

{% tab title="Windows" %}
```bash
# start from your code directory
cd C:\code
# create a new file for your Python code
# by convention, Flask applications are named app.py
echo "# write your code here" > app.py
```

Now use your preferred text editor to open your new `app.py` file.
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Python files have their own extension: `.py`. You'll also see the `.pyc` extension after you run your code, but these files can be ignored for now. Any Python file you write should have the `.py` file extension at the end.
{% endhint %}

### How code is written

You can write code in one of two ways:

1. Directly in your terminal
2. In a file

For the rest of the workshop, you will be writing your code inside your `app.py` file.

### How code is executed

Once you have code written in your `app.py` file, you will instruct Python to run the code written in that file. Python will open the file, and `interpret` the code as instructions.

{% hint style="info" %}
Some code is `interpreted` while other code is `compiled`. This depends on the programming language you are using, but the difference between the two is not relevant for this workshop. Check out this [Wikipedia article](https://en.wikipedia.org/wiki/Interpreted_language) for the technical details between the two paradigms.
{% endhint %}

### How to get started

Let's install a new python package called `Flask` that we will need later to run our server. Install it using your `terminal` like so:

{% tabs %}
{% tab title="Mac" %}
`pip3 install Flask`
{% endtab %}

{% tab title="Windows" %}
`py -m pip install Flask`
{% endtab %}
{% endtabs %}

Before we input any more commands, let's outline the steps we will need to take before you can run your code:

1. Create a file with a `.py` extension. Today, this should be `app.py`.
2. Open `app.py` using your text editor.
3. When you see large code blocks with `app.py` at the top, write that code into your `app.py` file, as it is written.
4. Save your file.
5. Navigate to the location of `app.py` file using your `terminal`. You can accomplish this with in `cd ~/flask_workshop` for Mac computers and `cd C:\code` for Windows computers.
6. Use `python3` or `py` to run your `app.py` file

Let's do it.

### Writing your app.py file

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
    #
    # We want to make sure everything is working, so let's return
    # some data!
    # Flask will take the data after return, and translate it into
    # an HTTP response.
    return 'Hello, World!'

```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Running your server

If you haven't already, open your `terminal` and `cd` into the location of your `app.py` file.

{% hint style="warning" %}
For those of you using Windows computers, the next command, `flask run` may not work. If you do not see output resembling what is written below, then you will need to launch flask using the following command:

`py -m flask.cli run`

Use that command, instead of `flask run` any time you are running your server. Sorry. Coding is sometimes harder on Windows.
{% endhint %}

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

![Yes, you can!](../.gitbook/assets/image%20%2817%29.png)

