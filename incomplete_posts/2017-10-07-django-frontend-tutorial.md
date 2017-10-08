---
layout: post
title: Django for Frontend Developers
---

This tutorial will teach you to make web pages with Django. It is intended for people who have some experience with web development, but are unfamiliar with Django and Python, and want to contribute to an existing project. It's focused on getting web pages up and running fairly quickly, and uses function-based views.

If you are looking for more in-depth tutorials on Django, check out [Django Girls](https://tutorial.djangogirls.org/en/) or the [Django Project](https://docs.djangoproject.com/en/1.11/intro/tutorial01/).

If you want to learn the very basics of frontend development, check out the [MDN Learning Area](https://developer.mozilla.org/en-US/docs/Learn) and [JavaScript for Cats](http://jsforcats.com/).

I'm writing this article as a supplement to the documentation over at the [Women Who Code PDX website repo](https://github.com/wwcodeportland/wwc-website)--you might find the materials there useful as well.

## How to Use this Tutorial

This will walk you through the process of adding pages to a Django application. Each step will result in a valid Django page; you can stop following along at whatever point you end up with the kind of page you need. I'll be creating a sample app for a bakery, called `desserts`.

## Setup

This tutorial assumes the Django project is already set up. If you're creating a brand new project, use one of the more detailed tutorials linked above as a guide.

The example in this tutorial will take place in a project called `django_sandbox`.

Pages in Django are organized into apps. Check to see if there's an app where your page should go already. If there's not, create one with this command. (Run it from the directory that contains your `manage.py` file.)

```sh
$ ./manage.py startapp desserts
```
This will create the files necessary for a `desserts` application. You'll also need to add the app to INSTALLED_APPS in the `settings` file.

> django_sandbox/settings.py

```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'desserts',
]
```

Start your app so you can look at the page. (See if the project you're contributing to has instructions on how to set up the project so you can run the app.)

## Create and serve an HTML file

Sometimes all you need is to serve a basic HTML file. Django's not the best framework to use if that's all your site consists of, but it's a good start for your new page.

Add a new HTML file. This will usually go in a `templates` folder, then in a folder with the same name as the app it's in.

```
django_sandbox
|+ desserts
  |+ templates
    |+ desserts
      * index.html
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>Main Street Bakery | Home</title>
</head>
<body>
  <h1>Main Street Bakery</h1>
  <p>Welcome to our home page!</p>
</body>
</html>
```

Write a view function to render the HTML file.

> desserts/views.py

```python
def index(request):
    return render(request, 'desserts/index.html')
```

This uses the `render` function to generate a page based on a GET request and the template you just created. You're not passing in any more data, so the page will just display the HTML.

Next you need to tell Django to call `index` when someone visits the home page for the `desserts` app.

If you just made the new app, you'll have to set up the `urls.py` files. (Don't worry about this if you're adding a page to an existing app.) Create an `urls.py` page in the app where you're adding the page.

```
django_sandbox
|+ desserts
  |- migrations
  * urls.py
  * views.py
|- django_sandbox
```

```python
from django.conf.urls import url
from . import views

urlpatterns = [
]
```

Then make sure the app's urls file is included in the project's main `urls.py`.

```
django_sandbox
|- desserts
|+ django_sandbox
  * settings.py
  * urls.py
```

Whether you're creating a new app or adding to a new one, you'll need to add the view to the app's `urls.py`.

```python
urlpatterns = [
  url('^home$', views.index, name='bakery home'),
]
```

The arguments for `url` consist of a regular expression pattern and a view function. The `name` keyword argument is optional, but it's a good idea to include it so that other code in the project can look up this URL pattern.

> TODO: finish "static" page (and shorten if possible), add other sections
