# djoser

REST implementation of Django authentication system. djoser library provides a set of Django Rest Framework views to handle basic actions such as registration, login, logout, password reset and account activation. It works with custom user model.

Requirements:

- Django
- MailHog (email testing tool for developers)

Project Setup:
create a virtual env.

    python -m venv env

    Activate
    ./env/Scripts/activte # for windows

    source env/bin/activate # linux user

Here i am using poetry you can use pip or pienv:
poetry Setup:

```
    poetry init
    poetry add django djangorestframework djoser djangorestframework_simplejwt django-cors-headers
    poetry add drf-yasg # for api docs
```
