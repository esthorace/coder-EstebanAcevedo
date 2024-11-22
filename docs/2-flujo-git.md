# Flujo de trabajo con Git

## Preparación del proyecto

- Crear un repositorio en GitGub, activando README.md y agregando una plantilla Python en .gitignore, en las opciones de GitHub.

- Clonar el repositorio remoto, para tener un repositorio local:

        git clone coderhouse

- Acceder a la carpeta:

        cd coderhouse

- Abrir Visual Studio Code:

        code .

Nota: si no llegara a abrirse VSCode, abrirlo de la forma habitual, y luego en el menú elegir 'Archivo' y 'Abrir Carpeta', y buscar la carpeta creada por git clone.

- Con `uv` crear el entorno virtual y agregar django y las dependencias necesarios.

[Leer: Adminstración de proyectos y entornos virtuales](1-proyectos-y-entornos.md)


## Uso de Git

Crear una rama o branch llamada dev, que es una abreviatura de development, es decir, desarrollo:

    git branch dev

Cambiar a esa rama:

    git switch dev

Listar las ramas para ver que se esté bien parado.

    git branch

Hacer los cambios necesarios y enviarlos al staging area.

    git add archivo

O, si queremos pasar todos los archivos, hacer:

    git add .

Luego, crear un commit con un mensaje:

    git commit -m "Comentario sobre los cambios hechos"

[Leer: Convenciones de mensajes de commit](3-mensajes-commit.md)

Una vez que se terminaron de hacer todos los commits necesarios y se los quiere fusionar a la rama principal, tener cuidado de no dejar archivos con cambios sin commit. Pararse en la rama principal:

    git switch main

Fusionar los commits de la rama dev en main:

    git merge dev

Se puede seguir trabajando en dev:

    git switch dev

O se la puede borrar:

    git branch -D dev

Cuando se quieran subir los cambios a la nube, es decir, a GitHub, cambiarse a la rama principal:

    git switch main

Y luego "empujar" todos los commits nuevos a la rama main de GitHub (se llama origin/main)

    git push
