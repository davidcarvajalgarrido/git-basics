# Lección 3 — Soluciones

## Ejercicio 1: Solución — Primer repo

```
mkdir mi-repo && cd mi-repo
git init
echo "# Mi proyecto" > README.md
git add README.md
git commit -m "Crea README inicial"
git log --oneline --graph --decorate
```
Estado esperado: un commit en `main` con mensaje “Crea README inicial”.

## Ejercicio 2: Solución — Confirma con intención

```
echo "A" > a.txt
echo "B" > b.txt
git add -p a.txt   # selecciona hunks intencionalmente
git commit -m "Añade parte inicial de a.txt"
git show
```
Estado esperado: el commit incluye solo los fragmentos elegidos de `a.txt`.

## Ejercicio 3: Solución — Amend

```
echo "Detalle extra" >> README.md
git add README.md
git commit --amend -m "Crea README inicial y añade detalle"
git log -1 --stat
```

## Ejercicio 4: Solución — Deshacer seguro

```
echo "cambios" >> a.txt
git restore a.txt
git add b.txt
git restore --staged b.txt
git status
```
