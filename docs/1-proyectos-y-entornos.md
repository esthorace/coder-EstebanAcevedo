# Adminstración de proyectos y entornos virtuales

## Instalación de `uv`

Usaremos `uv`, que es un moderno y el más rápido administrador de proyectos para Python, escrito en Rust. Ver la [página oficial](https://docs.astral.sh/uv/).

Instalación para Windows:

    powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

Instalación para macOs y Linux:

    curl -LsSf https://astral.sh/uv/install.sh | sh

Luego de la instalación, reiniciar la terminal.

## Creación de un proyecto

Una vez clonado un repositorio, accedemos a la carpeta, y parados dentro de ella, ejecutamos:

    uv init

Esto creará algunos archivos. Nunca deberemos eliminar `pyproject.toml` y `uv.lock`. 

## Creación del entorno virtual

    uv venv

En Visual Studio Code aparece "Hemos observado que se ha creado un nuevo entorno. ¿Desea seleccionarlo para la carpeta del área de trabajo? Damos click en sí.

Si no aparece este cuadro, hacer clic en `hello.py` y veremos que en la parte inferior derecha aparecerá la versión de Python y el nombre del entorno virtual ej: 3.13.0 ('.venv')

Podemos borrar `hello.py`

## Ver dependencias instaladas

    uv tree

## Instalación de dependencias

Ahora agregaremos los paquetes que usaremos en el proyecto, por ejemplo, vamos a instalar Django:

    uv add django

## Sincronización de un proyecto Python

Si abrimos un proyecto existente y no tenemos el entorno virtual creado, no es necesario crear el entorno e instalar las dependencias una por una, sino que, gracias al archivo `pyproject.toml`, podemos crear el entorno virtual e instalar las dependencias que están configuradas con el siguiente comando:

    uv sync

## Problemas con los permisos de Windows

Si llegara a aparece un problema de permisos a la hora de instalar `uv`, intenta ejecutar en la terminal de `Microsoft PowerShell`:

    Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope CurrentUser 

Reiniciar la terminal para que los cambios tengan efecto.

Si aún continúa, por única vez, abrir `Microsoft PowerShell` en modo **administrador**, y ejecutar el comando:

    Set-ExecutionPolicy Unrestricted

Reiniciar la terminal para que los cambios tengan efecto.
