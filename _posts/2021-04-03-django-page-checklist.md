---
layout: post
title: Django Page Checklist
---
If you've never worked with Django, it's worth going through the [Django Girls Tutorial](https://tutorial.djangogirls.org/en/) or the one on the [Django Project](https://docs.djangoproject.com/en/3.1/intro/tutorial01/) website. If you're trying to add a page to your Django application, and aren't sure you're doing it right, make sure you have the following things.

> NOTE: I try to periodically update this article as new Django versions come out, but if you find that the links refer to an old version of Django, most of the Django docs site allows you to pick a different version using the "documentation version" menu in the bottom right corner.

* The page will need a [view](https://docs.djangoproject.com/en/3.1/topics/http/views/) function that will generate the page's data and render a template with that data filled in.
  - The view function may take [arguments](https://docs.djangoproject.com/en/3.1/intro/tutorial03/#writing-more-views) from the URL pattern.
  - The view may need to [query](https://docs.djangoproject.com/en/3.1/ref/models/querysets/) records from the database.
  - The view will need to raise appropriate errors if objects are not found.  [get_object_or_404](https://docs.djangoproject.com/en/3.1/topics/http/shortcuts/#django.shortcuts.get_object_or_404) is a common shortcut for finding a single resource.
* The view will need a [template](https://docs.djangoproject.com/en/3.1/intro/tutorial03/#write-views-that-actually-do-something) to render.
  - The template may need to [inherit](https://docs.djangoproject.com/en/3.1/ref/templates/language/#id1) off a shared base template.
  - If it's inheriting, the template will need to establish  [blocks](https://docs.djangoproject.com/en/3.1/ref/templates/language/#id1) to fill in the base template, and fill in any inherited material in the blocks with [block.super](https://docs.djangoproject.com/en/3.1/ref/templates/language/#template-inheritance).
  - Any static (CSS, JavaScript, image, etc.) files will need to have the correct [static](https://docs.djangoproject.com/en/3.1/howto/static-files/) base URL in front of them, and the template (or one of its parent templates) will need to include the [load static](https://docs.djangoproject.com/en/3.1/howto/static-files/#configuring-static-files) tag.
* The app's [urlpatterns](https://docs.djangoproject.com/en/3.1/topics/http/urls/#example) will need to have a listing for the page's URL.
* If the page is in a new app (which should be created with `$ manage.py startapp`), the app will need to be included in [settings.INSTALLED_APPS](https://docs.djangoproject.com/en/3.1/ref/settings/#installed-apps) and the app's `urls.py` will need to be [included](https://docs.djangoproject.com/en/3.1/topics/http/urls/#including-other-urlconfs) in the main project `urls.py`.


NOTE: the steps relating to views assume function-based views. Some Django applications use [class-based](https://docs.djangoproject.com/en/3.1/topics/class-based-views/) views instead. These are more advanced; don't worry about using them when you're first starting out. The other steps in this checklist will be the same regardless of what type of views you are using.

## Changelog: 

* Updated 03 April 2021 to change to Django 3. (My thanks to the Django docs team for organizing their documentation well enough that it was easy to do this.)
* Updated 10 June 2018 to change to Django 2.
