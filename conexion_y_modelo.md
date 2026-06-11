Instrucciones
Crea una carpeta llamada actividad_m7_l2. Dentro de ella, realiza los siguientes pasos y documenta el proceso
en un archivo llamado conexion_y_modelo.md.

1. Conexión a PostgreSQL
• Instala el paquete necesario para conectarse a PostgreSQL:
pip install psycopg2-binary

• Crea una base de datos vacía en PostgreSQL llamada libreria.
• En el archivo settings.py de tu proyecto Django, reemplaza la configuración de base de datos por:

DATABASES = {
    "default": {
        "ENGINE": "django.db.backends.postgresql",
        "NAME": "libreriadb",
        "USER": "usuario",
        "PASSWORD": "1234",
        "HOST": "localhost",
        "PORT": "5432",
    }
}


2. Definición de un modelo
• En la app principal, crea un modelo Libro con los siguientes campos:

class Libro(models.Model):
	titulo = models.CharField(max_length=100)
	autor = models.CharField(max_length=50)
	anio_publicacion = models.IntegerFeld()
	disponible = models.BooleanField(default=True)

• Indica qué campo actuaría como clave primaria por defecto.
• Explica cómo se definiría una clave primaria compuesta si se quisiera hacer manualmente.

3. Aplicar migraciones
• Ejecuta los siguientes comandos desde consola y explica qué hace cada uno:

python manage.py makemigrations
python manage.py migrate

4. Operaciones CRUD (puede ser en shell o vista)
Utilizando el ORM, realiza las siguientes acciones y describe en el .md los comandos o código utilizados:
• Crear un nuevo libro
• Listar todos los libros
• Buscar un libro por su título
• Actualizar el campo disponible de un libro
• Eliminar un libro
Puedes hacerlo desde el shell de Django:

python manage.py shell