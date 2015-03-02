Django/Angular Token Auth with Django Rest Framework
====================================
This is an update version of [zackargyle](https://github.com/zackargyle)'s [angularjs-django-rest-framework-seed](https://github.com/zackargyle/angularjs-django-rest-framework-seed) which is amazing. There were just a few tweaks that I needed to make in order to make the project work properly. Updates need to be made to the steps below in order for things to run smoother.

** NEW FEATURE **
```
I just added my version of how to implement persisted tokens using $cookieStore along side
Witold Szczerba's http-auth-interceptor. Every request is checked for authentication, and the
login screen is served if the user is not authenticated. Please let me know how you have 
implemented this in your projects, I don't assume my way is the only or best way out there.

THANKS
```

Seed for a cross domain Angularjs / Django Rest Framework Application

    INCLUDED
        - RESTFUL API service for User and Address models
        - Login to obtain django token
        - Http-auth-interceptor and $cookieStore for persisted tokens
        - Angularjs display of data pulled from Django Rest API

After cloning down the repository:

1.  pip install fabric
2.	cd Django
3.  fab install:version=2.7 (or whatever version of python you are using)
4.  You just installed Django's auth system, which means you don't have any superusers defined.
    Would you like to create one now? no
       - The authtoken table is not created yet, so be sure to respond no to this request.
5.  Setup your superuser

Bam, you're good to go.

Afterwards, to see it in action, here is a simple way:

1.	cd Django 
2.	python manage.py runserver 8001 
3.	Open new tab 
4.	cd Angular 
5.	nodejs scripts/web-server.js 
6.	Open browser to http://localhost:8001/admin 
7.	Add a few Addresses 
8.	Go to http://localhost:8000/app/index.html 
9.	Login, and bam. Hello data.

Please give feedback, or bug fixes.

Zack Argyle

<br>

    NOTES: 
    
    - I highly suggest using a virtualenv as to not mess with in-built dependencies

    - It would be a great idea to create a requirements.txt file to document your south,
      django, djangorestframework, and django-cors-headers versions

    - Check out
      1. http://django-rest-framework.org/
      2. http://angularjs.org/
