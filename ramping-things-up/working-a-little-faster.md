---
description: >-
  Web developers love to save time while coding. Let's learn a few tips and
  tricks.
---

# Working a little faster

## Running our server in Development mode

Currently, our server is running in `production` mode.

{% hint style="info" %}
When you hear a programmer mention `production`, it usually means they're talking about running code in a way that's stable, secure, and scalable. Code usually runs differently during `development` versus in `production`. While `development mode` emphasizes productivity at the expense of security, `production mode` emphasizes stability at the expense of flexibility.
{% endhint %}

This means, among other things, that we have to restart the server every time we make changes. Let's fix that!

### The Environment

To run our server in `development mode`, we'll have to configure our `environment`. The `environment` is, while we're in this workshop, your `terminal`. As you learn more, you'll learn a lot more about the `environment` that software runs in. For now, think of it as something you can configure to run Flask with different settings.

### Environment Variables

In order to change Flask's behavior to run in `development mode` instead of `production mode` we need to `export` or `set` an `environment variable`.

{% hint style="warning" %}
If your server is still running in your terminal, quit your server with `ctrl-c` before moving on.
{% endhint %}

{% tabs %}
{% tab title="Mac" %}
```bash
export FLASK_ENV=development
```

`export` is a `terminal` command for setting an environment variable.
{% endtab %}

{% tab title="Windows" %}
#### For cmd.exe Terminals

```bash
set FLASK_ENV=development
```

#### For powershell Terminals

```bash
$env:FLASK_ENV = 'development'
```

`set` and `$env` are `terminal` commands for setting an environment variable.
{% endtab %}
{% endtabs %}

Now, when you run `flask run`, it will start in `development mode`

```text
flask run
 * Environment: development
 * Debug mode: on
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: XXX-XXX-XXX
```

That's better! Now, try changing one of your `return` statements in `app.py`.

```text
 * Detected change in '/Users/YOUR_USERNAME/flask-server/app.py', reloading
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: XXX-XXX-XXX
```

Look at that! Flask found a change in your `app.py` so it reloaded automatically. Pretty nifty.

{% hint style="info" %}
When you set an `environment variable` with the command above, it will only last as long as your current `terminal` session lasts. In other words, if you quit, you will have to re-set the `environment variable`.

It is possible to persist `environment variables` so you don't have to re-set them every time. Check out these guides for how to do so on [Mac](https://medium.com/@himanshuagarwal1395/setting-up-environment-variables-in-macos-sierra-f5978369b255) and [Windows](http://www.forbeslindesay.co.uk/post/42833119552/permanently-set-environment-variables-on-windows)
{% endhint %}

## localhost

Up until now, we've had to either copy-paste, or type `127.0.0.1` in order to access our server. This isn't the easiest thing to type, so let's use a shortcut: `localhost`.

`localhost` is a shortcut for the `ip address` `127.0.0.1`. While it's true that all computers on the internet have `ip addresses`, there are a few `ip ranges` that are reserved for specific purposes. The ip address `127.0.0.1` is a reserved address that will never access a computer on the internet. It will _only_ access a server running on your computer.

The `localhost` shortcut makes it easier to access your server, because it's much easier to remember `localhost` than it is to remember `127.0.0.1`.

Try accessing your Flask server with the following URL:

```bash
http://localhost:5000/
```

You should find that it works just the same way as `127.0.0.1`.

{% hint style="info" %}
For a list of all reserved IP addresses, check out [this Wikipedia page](https://en.wikipedia.org/wiki/Reserved_IP_addresses)
{% endhint %}

