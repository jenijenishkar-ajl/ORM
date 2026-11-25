# Ex02 Django ORM Web Application
## Date:
24-11-26 

## AIM
To develop a Django Application to store and retrieve data from a Vehicle Service Database platform using Object Relational Mapping(ORM).

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Detect changes and create migration files that describe how to modify the database schema

### STEP 5:
Execute the migration files and update the database schema to match your Django models

### STEP 6:
Create a superuser with full access rights to all models and data through the admin interface.

### STEP 7:
Apply the migration files of the created app to the database

### STEP 8:
Execute Django admin using localhost and create details for 10 entries

## PROGRAM

```

models.py

from django.db import models
from django.contrib import admin
# Create your models here.
class  Car(models.Model):
    name = models.CharField(max_length=100)
    model = models.CharField(max_length=100)
    year = models.IntegerField()
    price = models.DecimalField(max_digits=10, decimal_places=2)
class CarAdmin(admin.ModelAdmin):
    list_display = ('name', 'model', 'year', 'price')


admin.py

from django.contrib import admin
from .models import Car,CarAdmin

admin.site.register(Car, CarAdmin)

```

## OUTPUT

![alt text](<Screenshot 2026-11-25 160300.png>)

## RESULT
Thus the program for creating vehicle service Database using ORM hss been executed successfully.
