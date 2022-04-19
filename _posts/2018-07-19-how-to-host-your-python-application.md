---
layout: post
title: How to Host Your Python Application
author: john_doe
date: '2018-07-19 10:07:32'
---
Python is an incredibly popular language for web development. If you're interested in learning it or just want to experiment with incorporating Python into your projects, the quick-and-easy service PythonAnywhere will help get you started.

### Host Python Web App

To use PythonAnywhere, all you need is a web browser and about 5 minutes of your time (and if you're on a slow internet connection, maybe some patience as well). Just follow these simple steps:

Go to [PythonAnywhere](https://www.pythonanywhere.com/?affiliate_id=00535ced).

Sign up for a free account and fill out your details.

Then click on "open web apps".

[Click on open web apps](../../images/python-web-app.png)

Then click on "add a new web app".

[New web app](../images/python-new-web-app.png)

You'll see a page that lets you configure your app:

This page allows you to configure the Web framework you want to use. There are many different frameworks like Django, web2py, Flask, Bottle and others.

For simplicity, I'll go with Flask.

[Python Web framework](../images/python-web-framework.png)

Then it lets you select your Python version. Go for the newest version.

[Python version](../images/python-version.png)

Finally enter a Path for your Python file and click next. That sets up your Python web app and it is now hosted and online!

[Flask web app](../images/flask-web-app.png)

You can then open the source for of your web app. Either through the bash console or the web interface. They provide an online editor.

[Python flask](../images/python-flask.png)


### Flask web app

By creating a web app, they automatically created a template for the Flask web app. The template looks like this:

```python
# A very simple Flask Hello World app for you to get started with...

from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello from Flask!'
```

The first line of code simply loads the Flask module.

```python
from flask import Flask
```

Then the app is created

```python
app = Flask(__name__)
```

Then a route is created. A route is mapping of a link to a Python function. In the case the / link is called, Python will execute the function hello_world(). The return value is shown in the browser.

```python
@app.route('/')
def hello_world():
    return 'Hello from Flask!'
```

You can change this value to anything you want. If you return html tags, the browser will simply render html.

You can add as many routes as you want. Every web url has the map to a unique Python function, for example try this:

```python
@app.route('/')
def hello_world():
    return 'Hello from Flask!'

@app.route('/html')
def html():
    return '<h1>html</h1>'

@app.route('/image')
def image():
    return "<img src='https://wallup.net/wp-content/uploads/2019/10/355155-cat-meme-quote-funny-humor-grumpy-computer.jpg">'
`````

Of course there's a lot more you can do with the Python Flask framework, these are just the absolute basics.

