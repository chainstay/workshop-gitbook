---
description: 'We''ve implemented a GET, now let''s implement a POST'
---

# Accepting user input

## Sending data to our server

So far, we have figured out how to `GET` data from our server. We send a `request` to `/say_hello`, and the server sends back a `Hello, world!` in the `response`. However, `GET` will only _get_ us so far \(pun intended\).

Enter, `POST`. `POST` is a new `HTTP` `method` for sending `requests`. When we `GET`, we ask for data from the server. When we `POST`, we provide data to the server. Once the server has our data, it can do anything with it, for example:

* `POST` your username and password to log in to a website
* `POST` a new image to upload it to Instagram
* `POST` your credit card number to make a purchase on Amazon

Let's write a basic `POST` endpoint to retrieve `form` data.

{% hint style="info" %}
There's a lot of code to write here and it may not make sense at first. Remember that you can avoid typing the `# comments` and try to avoid copy-pasting.
{% endhint %}

{% code-tabs %}
{% code-tabs-item title="app.py" %}
```python
# new code here:
from flask import Flask, request

app = Flask(__name__)

# new code here:
# allow either a GET or a POST
@app.route('/say_hello', methods=('GET', 'POST'))
def hello():
    # check if request is a GET
    if request.method == 'GET':
        # if we receive a GET, then allow the user to provide
        # the name of an animal
        #
        # don't worry if you haven't learned HTML yet. For now,
        # read the code below and make guesses about what it means.
        return '''
            <form method="POST">
                <label for="formAnimal">Animal Name: </label>
                <input name="animal" type="text" id="formAnimal" />
                <input type="submit" value="Send POST" />
            </form>
        '''

    # at this point, we know that the method is a POST, because it is not a GET
    # we can find the user's animal name by looking it up by the input name
    # from the form above
    animal = request.form['animal']
    if not animal:
        return 'Error: No animal provided'

    # say hello, with the user's animal name included
    return 'Hello {}!'.format(animal)

@app.route('/')
def index():
    return 'Welcome to the server root'

```
{% endcode-tabs-item %}
{% endcode-tabs %}

That's a lot to take in. Let's break it down.

1. In order to accept `POST` `requests` to our `/say_hello` path, we need to instruct Flask to allow `POST`s on `line 8`
2. Then, when we receive a request at `/say_hello`, we check if the request is a `GET`, which requires less processing time for our server
3. * If it is a `GET`, provide the user with an `HTML` `form` for sending a `POST` back to the server at the same URL
   * If it is not a `GET`, then we know it is a `POST` because those are the only two `methods` allowed
4. We need to extract the `form` data from the `POST` sent by the user, we do so on `line 28`
   * Notice that we look up the `animal` by the same `key` as the `<input name="">` from the form on `line 20`
   * For example, if our form had an `<input name="species">`, then we could look up the value of that input with `request.form['species']`
5. The user may send the form without writing anything in the `<input>`. We want to control for this possibility, and let the user know that the Animal Name is required data. This control happens on `lines 29-30`.
6. By `line 33`, we know that we have an animal name provided by the user, so we can finally say hello!

## How has our server changed?

Now, when you go to `localhost:5000/say_hello`, you should see an `HTML` `form`

![](../.gitbook/assets/image%20%2813%29.png)

Type in a name to the input box, and click `Send POST`

![](../.gitbook/assets/image%20%2815%29.png)

Hello, dog!

![](../.gitbook/assets/image%20%289%29.png)

![](../.gitbook/assets/image%20%2810%29.png)

{% hint style="success" %}
If everything goes well, you should see a new type of server log statement in your terminal!

```bash
127.0.0.1 - - [THIS_DATE THIS_TIME] "GET /say_hello HTTP/1.1" 200 -
127.0.0.1 - - [THIS_DATE THIS_TIME] "POST /say_hello HTTP/1.1" 200 -
```
{% endhint %}

