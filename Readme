## Ex-03-Admin-user-using-function based views 

## Aim: 

Create a Django website with five users using function based views 

## Step 1: 

Create five users. 

## Step 2: 

Two staff users and three non-staff users 

## Step 3: 

Setting e-mail for all users 

## Step 4: 

Setting the first name and last name for all users. 

## Code: 

## In views.py:- 
```
from django.contrib.auth.models import User
from django.views import View 
from django.shortcuts import render

def create_users(request):
    # Create staff users (including admin)
    admin_user = User.objects.create_user(username='admin', password='adminpass')
    admin_user.is_staff  = True
    admin_user.is_superuser = True
    admin_user.email = 'admin@example.com'
    admin_user.first_name = 'Admin'
    admin_user.last_name = 'User'
    admin_user.save()

    staff_user1 = User.objects.create_user(username='staff1', password='staffipass')
    staff_user1.is_staff = True
    staff_user1.email='staffi@example.com'
    staff_user1.first_name = 'Staff'
    staff_user1.last_name = 'User1'
    staff_user1.save()

    #Create non-staff users
    user1 = User.objects.create_user(username='user1', password='user1pass')
    user1.email = "user1@example.com'
    user1.first_name = 'User'
    user1.last_name = 'One'
    user1.save()

    user2 = User.objects.create_user(username='user2', password='user2pass')
    user2.email='user2@example.com'
    user2.first_name = 'User'
    user2.last_name = 'Two'
    user2.save()

    user3 = User.objects.create_user(username='user3', password='user3pass')
    user3.email ='user3@example.com'
    user3.first_name = 'User'
    user3.last_name = 'Three'
    user3.save()

    return render(request, 'myapp/user_creation_success.html')
```
## In a template create a Html File: 
```
<html> 

    <body> 

        <h1>Successfully Created</h1> 

    </body> 

</html> 
```

## In Urls.py:- 
```
from django.contrib import admin 
from django.urls import path 
from saiapp import views 
from saiapp.views import create_users 
urlpatterns = [ 

    path('admin/', admin.site.urls), 
    path('home/',views.home,name='home'),
    path('create_users/', views.create_users, name='create_users'), 

] 
```
## In Settings.py:- 
```
INSTALLED_APPS = [ 

    "django.contrib.admin", 

    "django.contrib.auth", 

    "django.contrib.contenttypes", 

    "django.contrib.sessions", 

    "django.contrib.messages", 

    "django.contrib.staticfiles", 

    'saiapp', 

] 
 ```

## OUTPUT: 
![Screenshot 2023-11-22 103715](https://github.com/saiganesh2006/EX-03-Admin-user-using-function-based-views/assets/145742342/db469eb4-e6b7-4bbf-b495-c7cdd505e849)

 ![Screenshot 2023-11-22 103701](https://github.com/saiganesh2006/EX-03-Admin-user-using-function-based-views/assets/145742342/6d548f3a-8746-459f-b403-541a19e105ca)
 
## RESULT: 

Developed Admin User using Function based views successfully executed. 

 
 

 

 

 
