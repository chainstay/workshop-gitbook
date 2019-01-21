---
description: A web server is the fundamental building block of the Internet
---

# What is a web server?

## Web servers make the Internet happen

_Web servers are really good at one job: sending data to many different people at once._

Most of the time, that data is going to be HTML, CSS, and JavaScript files.

{% hint style="info" %}
Check out the other workshops or these free courses to learn more about: [HTML, CSS](https://www.udacity.com/course/intro-to-html-and-css--ud001), and [JavaScript](https://www.udacity.com/course/intro-to-javascript--ud803)
{% endhint %}

In this workshop, you'll write a very simple web server. It will set the foundation for you to expand upon within your own projects.

### How do servers work?

Web servers speak a specific language: `HTTP`. When your `client` is communicating with the `server`, you will make an `HTTP` `request`, and the server will provide an `HTTP` `response`.

### HTTP Requests

`GET https://www.google.com/search?q=hackher413`

There are five parts to this HTTP Request, but we are only going to focus on three:

* `GET`: This is the `METHOD`. `HTTP` has many methods, but the only ones we need to focus on now are `GET` and `POST`
  * `GET`: Retrieve data from the server
  * `POST`: Change data on the server
* `google`: This is the `hostname`. For our work today, your `hostname` is going to be `localhost`
  * `localhost` is a special hostname. It will never access the internet. It will only ever `resolve` to your personal computer. We'll learn more about `localhost` later in the workshop.
* `/search`: This is the `path`. When you build a server later in the workshop, you will define your own paths. They are usually named after the action you are trying to take at a specific `url`. 
* `?q=hackher413`: This is the `query`. The query for google.com is a `q`, but it can be anything you want. We'll learn more about the `query` later in the workshop.

The three parts that we will not be covering in this workshop are:

* `https://`: This is a secure extension of the `HTTP protocol`. We won't be covering this today, but see resources below to learn more.
* `www`: This is called the `subnet`. This is an advanced topic, so we will not cover it here.
* `.com`: When you add `.com` to `google`, you get Google's `domain name`. This becomes important when you want to make your server available on the Internet, but don't worry about it for now.

{% hint style="info" %}
You won't need to learn about `HTTP` AND `HTTPS` protocols, or the `subdomain` for some time as they are advanced concepts. If you're 
{% endhint %}

{% hint style="success" %}
At this point, you should be able to identify the `hostname`, `path`, and `query` \(if present\) for the following URLs:

* `http://www.kitty.com/cat`
* `https://duck.duck.com/goose`
* `https://www.dog.com/breeds?breed=golden_retriever`
{% endhint %}

### HTTP Responses

`HTTP` `responses` are far more varied than requests, so the response will look different depending on the server's purpose. However, there are two parts of the response that you'll need to be aware of for this workshop. Here is an example of an `HTTP` `response`:

```markup
200 OK
<html>
    <body>
        <p>Hello, world</p>
    </body>
</html>
```

Let's break this down.

* `Line 1: 200 OK`: That's the `status code` and `status message`. Your server is capable of reporting many status codes, but let's translate the three most common in english:
  * `200 OK`: This means "Okay, here's the thing you asked for!"
  * `404 NOT FOUND`: This means "I don't know what to do with that URL"
  * `500 SERVER ERROR`: This means "My code broke. Please fix me!"
* `Lines 2-6`: This is called the `body`. This is where your `server` will store data that it wants your `client` to receive.

{% hint style="info" %}
If the `<html>` `<body` and `<p>` tags don't mean anything to you yet, hold tight. You'll learn more about those later in the workshop.
{% endhint %}

{% hint style="info" %}
There are many HTTP status codes, though only a few are often used. Check out the [Wikipedia page](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes) for more thorough descriptions of these and others, including `418 IM A TEAPOT`.
{% endhint %}

{% hint style="success" %}
We won't be working directly with `HTTP responses` in this workshop, but do keep them in mind. They become very important later, as you learn more about web development.
{% endhint %}

