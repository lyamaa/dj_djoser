# djoser

REST implementation of Django authentication system. djoser library provides a set of Django Rest Framework views to handle basic actions such as registration, login, logout, password reset and account activation. It works with custom user model.

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

Creating project and apps:

    django-admin startproject core
    python manage.py startapp accounts

Configuring Settings.py:

```
# Installed Apps

DJANGO_APPS = [
"django.contrib.admin",
"django.contrib.auth",
"django.contrib.contenttypes",
"django.contrib.sessions",
"django.contrib.messages",
"django.contrib.staticfiles",
]

PROJECT_APPS = ["accounts"]

THIRD_PARTY_APPS = [
"rest_framework",
"drf_yasg",
"djoser",
"corsheaders",
"social_django",
"rest_framework_simplejwt",
"rest_framework_simplejwt.token_blacklist",
]

INSTALLED_APPS = DJANGO_APPS + PROJECT_APPS + THIRD_PARTY_APPS

MIDDLEWARE = [
"social_django.middleware.SocialAuthExceptionMiddleware", # Middleware for social auth
"django.middleware.security.SecurityMiddleware",
"django.contrib.sessions.middleware.SessionMiddleware",
"corsheaders.middleware.CorsMiddleware", # middleware for cors-headers
"django.middleware.common.CommonMiddleware",
"django.middleware.csrf.CsrfViewMiddleware",
"django.contrib.auth.middleware.AuthenticationMiddleware",
"django.contrib.messages.middleware.MessageMiddleware",
"django.middleware.clickjacking.XFrameOptionsMiddleware",
]
```
