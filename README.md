# Ex02 Django ORM Web Application
## Name:Pragadeeswaran L
## Reg.No:212223240120
## Date:25/09/2024

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM



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
```py
Models.py 
from django.db import models
from django.contrib import admin
# Create your models here.

class Bank(models.Model):
    customer_id = models.IntegerField(primary_key=True)
    customer_name = models.CharField(max_length=50)
    account_type = models.CharField(max_length=50)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)  
    monthly_interest = models.DecimalField(max_digits=5, decimal_places=2)  
    due_date = models.DateField()

class Loandetails(admin.ModelAdmin):
    list_display= ('customer_id','customer_name','account_type','loan_amount','monthly_interest','due_date')

admin.py 
from django.contrib import admin
from .models import Bank,Loandetails

# Register your models here.
admin.site.register(Bank,Loandetails)
```

## OUTPUT

![368414666-8fd93979-1450-420a-b0a9-bf63ccf32958](https://github.com/user-attachments/assets/dd010494-4e85-4ae8-868f-27a5e01bb260)



![368414723-452a8212-3d1a-4590-8ef0-3150021e064d](https://github.com/user-attachments/assets/438894b5-67dd-47e9-93dc-5641a39e639b)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
