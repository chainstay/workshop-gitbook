---
description: To infinity and beyond!
---

# What's next?

## You're doing great

So far, you have:

1. Learned about the fundamental components of the Internet
2. Learned the basics of programming languages
3. Installed Python onto your computer
4. Run your own Python code
5. Created the beginnings of your very own web server

## What's next?

From this point on, the content is going to become far more open-ended. You may have a totally different skillset and comfort with these topics than another person in this workshop, so you will have the opportunity to determine what feels like the best path forward for you, right now.

## Which statement best applies to you?

### "This was my first experience with programming"

Okay, first of all, _congratulations!_ It takes a lot of bravery to step into a new discipline. Not only that, but programming has a very specific set of vocabulary that can be very difficult to understand at first**.**

**Keep learning!**

#### **Here are some great resources to continue your journey**:

1. Get more comfortable writing and running Python code from scratch. The exercises at [Learn Python Pogramming](https://pythonbasics.org/) are a great place to start.
2. Watch some YouTube videos about fundamental programming concepts e.g. [MIT's Intro to Programming with Python](https://www.youtube.com/watch?v=ytpJdnlu9ug&list=PLUl4u3cNGP63WbdFxL8giv4yhgdMGaZNA)
3. Start working through the perennial programming book: [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/)

**That said, if you're looking to push yourself, take a look at the next prompt!**

### **"I am comfortable writing code, but I'm not experienced with Python or Flask"**

Awesome. You are in the perfect position to walk your way through the [Flask Tutorial](http://flask.pocoo.org/docs/1.0/tutorial/). This excellent tutorial, written by the Flask maintainers, is ideal for introducing you to web development with Python. You'll learn, how to:

* Connect Flask to a database
* Create a login/logout flow for Flask
* Keep your code [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) with `Blueprints` and `HTML` `Templates`
* Write unit tests to protect yourself from introducing bugs

### **"I've already written Python for the web before. Give me a challenge!"**

![Actual map of the Internet](../.gitbook/assets/image%20%283%29.png)

It's finally time to get your code running on the Internet.

#### Deployment

When a web developer \(that's you!\) wants to make their server available online, there are a few tasks that must be accomplished.

{% hint style="danger" %}
There is tremendous risk associated with deploying apps to the web.

Apps deployed to Heroku, and other cloud providers, are subject to thousands of foreign and domestic hackers attempting to hack your server and obtain secret information. If you get pwned, the hacker could take your account credentials, and within minutes have an army of servers mining Bitcoin, with server costs charged to your credit card.

Security for your web servers must be taken very seriously.

Before you deploy your Flask app, or any web server, to the internet, _read all documentation on how to run your server in production_. That documentation will ensure that you've taken all the necessary precautions to secure your server from common attacks.
{% endhint %}

If you are running a Flask app, like the one we worked on in today's workshop, read through the documentation for how to [productionalize Flask](http://flask.pocoo.org/docs/1.0/tutorial/deploy/). This will graduate you from the Flask development server, to a production-ready [WSGI](https://en.wikipedia.org/wiki/Web_Server_Gateway_Interface) server: `Waitress`.

Once you have Flask running with Waitress, it's time to build a Docker container for running your application. Docker is an invaluable tool to make sure that your app runs exactly the same way on the Internet as it does on your laptop.

#### [Run a Flask server in a Docker container](https://docs.docker.com/get-started/) 

{% hint style="success" %}
Once you can run your server in a container, and access it over `localhost`, you're ready to deploy that container image to Heroku.
{% endhint %}

There are many methods for running containers on the web. Heroku makes this process easy by providing an all-in-one solution with minimal configuration. Check out the tutorial below for instructions on how to run your container image on Heroku.

#### [Run a Docker container on Heroku](https://devcenter.heroku.com/articles/container-registry-and-runtime)

{% hint style="success" %}
If you've made it this far, well done. You have successfully expanded the reach of the internet. You've got everything you need to succeed as a web developer, and then some! There's one thing left to do:

Make cool stuff.
{% endhint %}



