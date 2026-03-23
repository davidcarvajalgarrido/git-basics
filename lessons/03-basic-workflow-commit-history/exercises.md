# Lección 3 — Ejercicios

## Ejercicio 1: Crea tu primer repositorio

1. Crea un directorio nuevo y accede a él.
2. Inicialízalo con `git init`.
3. Crea un archivo `README.md`, añádelo al staging con `git add` y haz tu primer commit con un mensaje claro usando `git commit`.
4. Usa `git status` para comprobar el estado del repositorio antes y después de cada paso.
5. Muestra el historial de commits con `git log --oneline`.

## Ejercicio 2: Añade y modifica archivos

1. Crea dos archivos nuevos y añádelos al staging con `git add`.
2. Haz un commit con un mensaje descriptivo.
3. Modifica uno de los archivos y usa `git diff` para ver los cambios no confirmados.
4. Añade el archivo modificado al staging y haz un nuevo commit.
5. Usa `git log` y `git status` para revisar el historial y el estado actual.

## Ejercicio 3: Explora el historial y cambia de versión

1. Crea y confirma un nuevo archivo.
2. Usa `git log --oneline` para ver los identificadores de los commits.
3. Utiliza `git checkout <id-del-commit>` para moverte a un commit anterior y observa el contenido del directorio.
4. Vuelve a la última versión con `git checkout main` (o la rama principal que corresponda).
5. Usa `git diff` para comparar cambios entre commits si es necesario.
