echo "A" > a.txt
echo "B" > b.txt
git add -p a.txt   # selecciona hunks intencionalmente
git commit -m "Añade parte inicial de a.txt"
git show
echo "Detalle extra" >> README.md
git add README.md
git commit --amend -m "Crea README inicial y añade detalle"
git log -1 --stat
echo "cambios" >> a.txt
git restore a.txt
git add b.txt
git restore --staged b.txt
git status
# Lección 3 — Soluciones

## Ejercicio 1: Solución — Crea tu primer repositorio

```
mkdir mi-repo && cd mi-repo
git init
echo "# Mi proyecto" > README.md
git status
git add README.md
git status
git commit -m "Crea README inicial"
git status
git log --oneline
```
Estado esperado: un commit en la rama principal con el mensaje “Crea README inicial”.

## Ejercicio 2: Solución — Añade y modifica archivos

```
echo "Uno" > uno.txt
echo "Dos" > dos.txt
git add uno.txt dos.txt
git commit -m "Añade uno.txt y dos.txt"
echo "Cambio en uno" >> uno.txt
git diff
git add uno.txt
git commit -m "Actualiza uno.txt"
git log --oneline
git status
```
Estado esperado: historial con dos commits y ambos archivos confirmados.

## Ejercicio 3: Solución — Explora el historial y cambia de versión

```
echo "Extra" > extra.txt
git add extra.txt
git commit -m "Añade extra.txt"
git log --oneline
# Apunta el id del commit anterior
git checkout <id-del-commit>
ls   # El archivo extra.txt no debe estar
git checkout main  # O la rama principal correspondiente
git diff <id1> <id2>  # Opcional: compara cambios entre commits
```
