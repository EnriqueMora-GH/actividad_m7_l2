# actividad_m7_l2
Actividad N° 2 – Conexión a Base de Datos y Uso del ORM en Django
# Primeros pasos
# **Creacion de ambiente:**
# crear entorno virtual
python -m venv venv
# se activa entorno virtual
source venv/bin/activate
# Instalacion de django
pip install django

# Se actualiza pip (ver comando sugerido)

upgrade pip----

# creacion del proyecto
django-admin startproject config .

# Creacion de la Aplicacion
python manage.py startapp librería

# Se levanta Servidor django
python manage.py runserver

# Se abre una nueva shell para instalar psycopg2 que conectará django con la base Postgres
en nueva shell---> 
**ojo ejecutar:**
source venv/bin/activate
# Instalacion de psycopg2
pip install psycopg2-binary