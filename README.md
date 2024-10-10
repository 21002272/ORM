# Ex02 Django ORM Web Application
## Date: 26-09-2024

## AIM
To develop a Django application to store and retrieve data from a Bank database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![image](https://github.com/user-attachments/assets/5bb20919-6c84-43b2-bea0-a4a15457c20c)

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 customers.

## PROGRAM

admin.py
```
from django.contrib import admin
from .models import Bankloan, BankloanAdmin  
admin.site.register(Bankloan, BankloanAdmin)
```
models.py
```
from django.db import models
from django.contrib import admin
class Bankloan(models.Model):
    customerid= models.IntegerField(primary_key=True)
    customerrate = models.IntegerField()
    age = models.IntegerField()  
    cust_no = models.IntegerField()
    customerloan_purpose =models.CharField(max_length=500)

class BankloanAdmin(admin.ModelAdmin):
    list_display = ('customerid', 'customerrate', 'age', 'cust_no', 'customerloan_purpose')

```

## OUTPUT
![Screenshot 2024-10-10 103934](https://github.com/user-attachments/assets/e7046c15-1e82-4f45-b6c9-9dbfb6fa3e78)




## RESULT
Thus the program for creating a database using ORM hass been executed successfully
