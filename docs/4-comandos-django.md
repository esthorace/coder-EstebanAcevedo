# Django

## Creación de un proyecto

Clonar un repositorio

Crear entorno virtual

Instalar dependencias

Crear un proyecto:

    mkdir src
    cd src
    django-admin startproject config .

Ejecutar el servidor:

    python manage.py runserver

Cambiar el idioma en src/config/settings.py

    LANGUAGE_CODE = 'es'

## Creación de una aplicación

Crear una aplicación:

    python manage.py startapp core

Registrar la aplicación src/config/settings.py

    INSTALLED_APPS += [
        'core',
    ]
