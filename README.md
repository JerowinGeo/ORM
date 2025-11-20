# Ex02 
# Django ORM Web Application


## AIM
To develop a Django application to store and retrieve data from Movies Database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM
<img width="1240" height="651" alt="image" src="https://github.com/user-attachments/assets/11c197fe-d068-497f-9448-363bc8b71256" />

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

### admin.py
```python
from django.contrib import admin
from .models import Movie,MovieAdmin
admin.site.register(Movie,MovieAdmin)
```
### models.py
```python
from django.db import models
from django.contrib import admin
class Movie(models.Model):
	Movie_name=models.CharField(max_length=50)
	Ratings=models.FloatField(primary_key="Ratings")
	Cast=models.CharField(max_length=50)
	Release_year=models.DateField()
	Genre=models.CharField(max_length=50)
class MovieAdmin(admin.ModelAdmin):
	list_display=('Movie_name','Ratings','Cast','Release_year','Genre')
```


## OUTPUT
<img width="1257" height="783" alt="image" src="https://github.com/user-attachments/assets/a8239d72-744b-4ef2-9e79-6936e7905da4" />


## RESULT
Thus the program for creating a database using ORM hass been executed successfully.
