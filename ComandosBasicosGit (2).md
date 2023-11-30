# COMANDOS GIT

## LOCAL

``` bash

# Indica la versión instalada de git (se usa para verficar la instalación de git)
git --version

# Inicializa un nuevo repositorio git de control de versiones en la carpeta actual (crea una carpeta .git)
git init

# Indica el estado de los cambios realizados en el directorio
# Muestra los cambios pendientes de agregar (add) a staged en rojo y los cambios que ya estan en staged listos para ser comprometidos en verde
git status

# Añade todos los archivos al staged
git add .

 # Añade los archivos especificados al staged
git add nombre(s) archivo(s)

# Restaura un archivo del staged al arbol de trabajo (working tree)
# OJO!! no solo quita del staged un archivo sino que revierte los cambios realizados en el(los) archivo(s) indicado(s), tomando como base la versión previa del último commit
git restore nombre_archivo

# Compromete los cambios locales
git commit -m "Mensaje commit"

 # Muestra las ramas creadas
git branch

# Crea una nueva rama con el nombre "nombre_rama" y posiciona dentro de esa rama
git checkout -b nombre_rama

# Cambia a la rama indicada como "nombre_rama"
git checkout nombre_rama

# Renombrar una rama local, desde la rama principal
git branch -m nombre-antiguo nombre-nuevo

# Posiciona el HEAD en el commit especificado por el hash_commit
git checkout hash_commit

# Muestra el historial de commits de la rama actual (gran cantidad de info.)
git log

# Muestra el historial en un formato corto (recomendado)
git log --oneline

# Muestra el contenido de un archivo de un commit específico (hash_commit)
git show hash_commit:Carpeta/Archivo.ext
```

## REMOTO

``` bash
 # Conecta el proyecto del repositorio remoto al directorio local
git remote add origin <URL proyecto repositorio remoto>

# Obtiene los cambios de la rama main (principal) actuales del repositorio remoto
git pull origin nombre_rama

# Carga/envía los cambios locales al repositorio remoto en la rama main o la que se especifique (los push se realizan sobre una rama en específico)
git push -u origin nombre_rama

# Para obtener otras ramas existentes en el repositorio remoto, seguir los siguientes pasos:
    # 1. Crear localmente la rama (respetar el nombre exacto de la rama)
    git checkout -b nombre_rama_remota

    # 2. Obtener o verificar la información de los últimos cambios en el repositorio después del último pull realizado, sin modificar la rama local
    git fetch

    # 3. Obtener (copia) los cambios en la rama remota, fosiona los cambios con la rama local
    git pull origin nombre_rama_remota
```
