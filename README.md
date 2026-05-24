# Ex01 Django ORM Web Application
## Date: 

## AIM
To develop a Django application to manage an online food delivery platform like Zomato/Swiggy using Object Relational Mapping (ORM).

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
## models.py
```python
from django.db import models
from django.contrib import admin

class FoodDelivery_DB(models.Model):
    Order_ID = models.IntegerField(primary_key=True)
    CustomerName = models.CharField(max_length=30)
    OrderDate = models.DateField()
    ItemName = models.CharField(max_length=100)
    OrderQty = models.IntegerField()
    UnitPrice = models.FloatField()
    TotalAmount = models.FloatField()
    DeliveryAddress = models.CharField(max_length=200)

class FoodDelivery_DBAdmin(admin.ModelAdmin):
    list_display = (
        'Order_ID',
        'CustomerName',
        'OrderDate',
        'ItemName',
        'OrderQty',
        'UnitPrice',
        'TotalAmount',
        'DeliveryAddress'
    )
```
## admin.py
```python
from django.contrib import admin
from .models import FoodDelivery_DB, FoodDelivery_DBAdmin

admin.site.register(FoodDelivery_DB, FoodDelivery_DBAdmin)
```
## OUTPUT

Include the screenshot of your admin page.
<img width="1322" height="629" alt="image" src="https://github.com/user-attachments/assets/168e7473-6d75-4f21-a361-1373adc689b2" />


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
