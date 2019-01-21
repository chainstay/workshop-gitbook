# Configuring our Server



Let's dive a little deeper into what Flask just told us:

* `line 1`: This is the command to start your Flask server. When you run this command, in the same directory as your `app.py`, it will start running Flask for you.
* `lines 2-5`: You can ignore these for now. They become important later, when you are getting ready to run your server on the Internet.
* `line 6`: This line is important. It tells you how to access your server!
  * See the URL there, `http://127.0.0.1:5000/`? That looks different than URLs you are familiar with. Here are its parts:
  * `http://`: We've seen this before, it's the `protocol`. You can ignore it for now.
  * `127.0.0.1`: This is an `ip address`. Every website has one, but you don't see it because it's masked by a `domain name`. This specific `ip address` is special. We'll talk more about this address in a moment.

