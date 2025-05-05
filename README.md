# Práctica 2 - Proyecto Django 
 1.- Creación del entorno virtual 

bash
python -m venv env

activamos el entorno
source env/Scripts/activate
2.- instalacion de django
pip install django
3.- iniciamos el proyecto
django-admin startproject practica2 .
4.- creamos la aplicacion
python manage.py startapp libros
5.-Registrar aplicación en settings.py
INSTALLED_APPS = [
    ...
    'libros',
]
6.- creamos el modelo 
# libros/models.py

from django.db import models

class Autor(models.Model):
    nombre = models.CharField(max_length=100)
    nacionalidad = models.CharField(max_length=100)
    edad = models.IntegerField()
7.- hacemos las migraciones 
python manage.py makemigrations
python manage.py migrate
8.- creamos el super usuario
python manage.py createsuperuser
10 iniciamos el servidor 
python manage.py runserver

