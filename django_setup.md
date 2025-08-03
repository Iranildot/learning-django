## FIRST DJANGO SET UP

#### Creating a Project

First of all you need to create a project.

```
django-admin startproject PROJECT_NAME .
```

#### Creating an App

Then you can create your web app running:

```
python3 manage.py startapp APP_NAME
```
#### Project urls.py

```
from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),
]

```

#### Put the app name into the settings.py INSTALLED_APPS

```
INSTALLED_APPS = [
    'testapp',
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]

```

#### Create a templates/testapp folder in testapp folder

#### Create a index.html template

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hello, World!</title>
</head>
<body>
    Hello, World!
</body>
</html>
```

#### Create a urls.py into testapp

```
from django.urls import path
from . import views

urlpatterns = [
    path('', views.index)
]
```

#### Add index view to views.py

```
from django.shortcuts import render

def index(request):
    return render(request, 'testapp/index.html')
```
