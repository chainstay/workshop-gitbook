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
 * Debugger PIN: 124-918-479
```

That's better! Now, try changing one of your `return` statements in `app.py`.

```text
 * Detected change in '/Users/YOUR_USERNAME/flask-server/app.py', reloading
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 124-918-479
```

Look at that! Flask found a change in your `app.py` so it reloaded automatically. Pretty nifty.

{% hint style="info" %}
When you set an `environment variable` with the command above, it will only last as long as your current `terminal` session lasts. In other words, if you quit, you will have to re-set the `environment variable`.

It is possible to persist `environment variables` so you don't have to re-set them every time. Check out these guides for how to do so on [Mac](https://medium.com/@himanshuagarwal1395/setting-up-environment-variables-in-macos-sierra-f5978369b255) and [Windows](http://www.forbeslindesay.co.uk/post/42833119552/permanently-set-environment-variables-on-windows)
{% endhint %}



