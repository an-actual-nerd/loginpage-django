# loginpage-django

A simple login page using django

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install django

```bash
pip install django
```

## Create App
```bash
django admin django-admin startproject loginapp
```
## Creating URL in project url.py
```bash
urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('loginapp.urls')),
]
```

## Creating url.py in loginapp
```python
from django.contrib import admin
from django.urls import path
from loginapp import views

urlpatterns = [
    path('', views.index, name='home'),
    path('login', views.loginuser, name='login'),
    path('logout', views.logoutuser, name='logout'),
```

## Creating end points views.py in loginapp
```python
def index(request):
def loginuser(request):
def logoutuser(request):
```

## Creating static and templates folder and mentioning it in a project setting.py
[django documentation](https://docs.djangoproject.com/en/3.2/howto/static-files/)

Mention templates dir in settings.py
```python
 'DIRS': [BASE_DIR / "templates"],
```
