---
description: Let's add some cat (and dog!) images to our server
---

# The internet is made of cats

So far, our server has only been capable of returning text. Let's liven up our server by sending back some images!

{% hint style="info" %}
While we could configure our server to actually send image files, that gets into a little too much complexity for now. Instead, we'll be sending `HTML` to tell the browser to get an image from a different website. So, while our server will be sending back text data, your web browser will use that text to display an image on your page. Nifty!
{% endhint %}

## Let's find some images

For this exercise, do a quick search to find the URLs of two images. One of a cat, and another of a dog. You will need the URL of the image itself, not of the page where the image is found. For example:

Dog image examples:

* [https://ybxzcgnc7b-flywheel.netdna-ssl.com/wp-content/uploads/2017/11/cute.jpg](https://ybxzcgnc7b-flywheel.netdna-ssl.com/wp-content/uploads/2017/11/cute.jpg)
* [https://d17fnq9dkz9hgj.cloudfront.net/uploads/2018/04/Frenchie\_05.jpg](https://d17fnq9dkz9hgj.cloudfront.net/uploads/2018/04/Frenchie_05.jpg)
* [https://gfnc1kn6pi-flywheel.netdna-ssl.com/wp-content/uploads/2017/09/cute1.jpg](https://gfnc1kn6pi-flywheel.netdna-ssl.com/wp-content/uploads/2017/09/cute1.jpg)

Cat image examples:

* [http://www.smashingphotoz.com/wp-content/uploads/2012/11/11\_cat\_photos.jpg](http://www.smashingphotoz.com/wp-content/uploads/2012/11/11_cat_photos.jpg)
* [https://data.whicdn.com/images/298844185/large.jpg?t=1507433077](https://data.whicdn.com/images/298844185/large.jpg?t=1507433077)
* [https://assets3.thrillist.com/v1/image/2558908/size/tmg-article\_tall.jpg](https://assets3.thrillist.com/v1/image/2558908/size/tmg-article_tall.jpg)

{% hint style="info" %}
You need not limit yourself to dogs and cats. Your server is capable of a great many things.
{% endhint %}

{% hint style="success" %}
Once you've found an image URL of a dog, and another of a cat, you're ready to move on.
{% endhint %}

## Add some logic to our form data

Currently, when we accept form data at `/say_hello`, we simply parrot back the data that we receive. Instead, let's inspect the data, and use it to control actions that our server takes.

```python
# abbreviated

@app.route('/say_hello', methods=('GET', 'POST'))
def hello():
    if request.method == 'GET':
        return '''
            <form method="POST">
                <label for="formAnimal">Animal Name: </label>
                <input name="animal" type="text" id="formAnimal" />
                <input type="submit" value="Send POST" />
            </form>
        '''
        
    animal = request.form['animal']
    if not animal:
        return 'Error: No animal provided'
    
    # new code below
    
    # we're not sure which image URL to use yet, so set it to a blank string.
    image_url = ''
    # check which animal the user requested
    if animal == 'dog':
        # the user requested a dog, so set the image URL to be a dog image
        image_url = 'https://ybxzcgnc7b-flywheel.netdna-ssl.com/wp-content/uploads/2017/11/cute.jpg'
    elif animal == 'cat':
        # the user requested a cat, so set the image URL to be a cat image
        image_url = 'http://www.smashingphotoz.com/wp-content/uploads/2012/11/11_cat_photos.jpg'
    else:
        # we don't know what animal this is, so show the user a platypus
        image_url = 'https://img.purch.com/h/1000/aHR0cDovL3d3dy5saXZlc2NpZW5jZS5jb20vaW1hZ2VzL2kvMDAwLzAwOS82Nzkvb3JpZ2luYWwvMDkwNTExLXBsYXR5cHVzLTAyLmpwZw=='

    # say hello, with the user's animal name included
    return '''
        <h1>Hello {animal_name}!</h1>
        <image style="width: 100%" src="{image_src}" />
    '''.format(animal_name=animal, image_src=image_url)

# abbreviated

```

{% hint style="info" %}
In your code, inject your chosen dog image URL on `line 25`, and your cat image URL on `line 28`. Feel free to copy-paste the URLs, there's nothing to be learned by manually typing long URLs.
{% endhint %}

We've made two big changes here, so let's break it down once more.

The new code between `line 20` and `line 31` interrogates the form data from our user. Here, we make use of Pythons `if`, `elif`, and `else`, keywords to specify which image URL corresponds to which animal.

Once we have a value for `image_url`, we inject it into what's called a `format string`. Essentially, `format strings` allow you to take data and `interpolate` \(or, inject\) it into a template. When Flask creates the `HTTP` `response`, the data sent back will include the value of `animal` in the place of `{animal_name}`, and the value of `image_url` in the place of `{image_src}`.

{% hint style="info" %}
If the `HTML` is confusing to you now, don't worry. Once you spend some time learning it, `HTML` is a straight-forward language to work with.
{% endhint %}

{% hint style="info" %}
If you're wondering what the difference is between a `'single-quote string'` and a `'''triple-quote string'''`, they are roughly equivalent. However, when you use three quotes `'''`, you can add line-breaks within the `string`, and it will not break your Python code.
{% endhint %}

## Let's see some pictures

Now, when you submit your form at `/say_hello`, you should see a picture!

![](../.gitbook/assets/image%20%281%29.png)

![d&apos;awwww](../.gitbook/assets/image%20%284%29.png)

**Say, you submit an animal that your server doesn't understand**

![](../.gitbook/assets/image%20%2812%29.png)

Your server can handle it! ✅

{% hint style="success" %}
You did it!
{% endhint %}

