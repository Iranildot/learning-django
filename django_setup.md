# 🚀 FIRST DJANGO SETUP

A quick guide to setting up your first Django project and app.

---

## 🛠️ 1. Creating the Project

Run the following command to create a new Django project in the current directory:

```bash
django-admin startproject PROJECT_NAME .
```

> The `.` at the end places the project files in the current directory.

---

## 🧱 2. Creating an App

Next, create a new Django app inside your project:

```bash
python3 manage.py startapp APP_NAME
```

---

## 🧩 3. Registering the App

Open `settings.py` and add your app to the `INSTALLED_APPS` list:

```python
INSTALLED_APPS = [
    'APP_NAME',  # Replace with your app name, e.g., 'hello'
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]
```

---

## 🌐 4. Project URLs Configuration

Edit the main `urls.py` file to include your app’s routes:

```python
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path('admin/', admin.site.urls),
    path('hello/', include('hello.urls')),  # Replace 'hello' with your app name
]
```

---

## 🧭 5. App URLs File

Inside your app directory (e.g., `hello/`), create a new file called `urls.py` with the following content:

```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.index),
]
```

---

## 🧠 6. Creating the View

In the `views.py` file of your app, define a view to render a simple HTML template:

```python
from django.shortcuts import render

def index(request):
    return render(request, 'hello/index.html')  # Adjust path as needed
```

---

## 🗂️ 7. Creating the Template

1. Inside your app folder, create a directory structure like: `templates/hello/`
2. In that folder, create a file named `index.html` with the following content:

```html
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

---

## ✅ 8. Running the Server

To start the development server, run:

```bash
python3 manage.py runserver
```

Visit `http://localhost:8000/hello/` in your browser to see your first Django page!

---
