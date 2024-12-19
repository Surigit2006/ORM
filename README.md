# Ex02 Django ORM Web Application
# Date:19/10/2024
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
Models.py
```
from django.db import models
from django.contrib import admin

class ElectricityBill(models.Model):
    customer_id = models.CharField(max_length=20, primary_key=True)
    customer_name = models.CharField(max_length=100)
    bill_no = models.IntegerField()
    bill_amount = models.IntegerField()
    bill_date = models.DateField()


# Define the admin configuration
class ElectricityBillAdmin(admin.ModelAdmin):
    list_display = ('customer_id', 'customer_name', 'bill_no', 'bill_amount', 'bill_date')


```
admin.py
```
from django.contrib import admin
from .models import ElectricityBill, ElectricityBillAdmin

admin.site.register(ElectricityBill, ElectricityBillAdmin)
```
urls.py
```
from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),
]
```
# OUTPUT

![Screenshot 2024-12-19 093146](https://github.com/user-attachments/assets/cec8875a-b643-4b90-843f-310833d3a845)

# RESULT
Thus the program for creating a database using ORM hass been executed successfully
