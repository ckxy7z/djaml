-*- markdown -*-

Djaml is template Loader for Django that allows you to use [HamlPy](https://github.com/jessemiller/HamlPy) in your templates

It is based on the [django-shpaml-template-loader project](http://bitbucket.org/jiaaro/django-shpaml-template-loader),
and is licensed under the GPL.

## Requirements

* [Django](http://www.djangoproject.org) -- I've tested it using Django 1.2.3 and the version of Django that is included with the [djangoappengine](http://www.allbuttonspressed.com/projects/djangoappengine) project
* HamlPy -- tested using version as of December 4, 2010

## Installation

Sorry, no setup.py file yet so you must copy djaml into the root of your Django project.

Having done that, you need to add djaml as the first item in TEMPLATE_LOADERS 
    
    TEMPLATE_LOADERS = (
        'djaml.filesystem',
        ...
    )

If you don't put djaml first, then the standard Django template loaders will try and process
it first.

Make sure your templates have a .haml extension, and put them wherever you've told Django
to expect to find templates.

If you have any questions or comments, send some email to chartjes@littlehart.net
