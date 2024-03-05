# Ex02 Django ORM Web Application
## Date: 05.03.2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
```
admin.py
from django.contrib import admin

# Register your models here.
from .models import bookdetail,bookdetailAdmin
admin.site.register(bookdetail,bookdetailAdmin)

models.py
from django.db import models
from django.contrib import admin

class bookdetail(models.Model):
    student_name=models.CharField(max_length=20);
    reg_no=models.IntegerField();
    dep=models.CharField(max_length=30);
    book_name=models.CharField(max_length=30,primary_key=True);
    author_name=models.CharField(max_length=30);
    book_refno=models.IntegerField();
    dateof_taken=models.DateField();
    dateof_return=models.DateField();

class bookdetailAdmin(admin.ModelAdmin):
    list_display=("student_name","reg_no","dep","book_name","author_name","book_refno","dateof_taken","dateof_return")    

```

## OUTPUT

![alt text](<Screenshot 2024-03-05 221228.png>)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
