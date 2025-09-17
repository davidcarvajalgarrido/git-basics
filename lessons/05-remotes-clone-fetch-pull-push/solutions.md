# Lección 5 — Soluciones

## Ejercicio 1: Solución — Publicar main

```
git remote add origin git@github.com:tuusuario/tu-repo.git
git push -u origin main
git branch -vv
git remote -v
```
Estado esperado: `main` muestra `origin/main` como upstream; `git remote -v` lista fetch/push.

## Ejercicio 2: Solución — Clonar y sincronizar

```
git clone git@github.com:tuusuario/tu-repo.git repoA
git clone git@github.com:tuusuario/tu-repo.git repoB
cd repoA
echo "cambio" >> a.txt && git add a.txt && git commit -m "Cambio en A"
git push
cd ../repoB
git fetch origin
git pull --ff-only
git log --oneline --graph --decorate --all
```

## Ejercicio 3: Solución — Ramas remotas

```
# En A
git switch -c feature/demo
echo "demo" > demo.txt
git add demo.txt && git commit -m "Crea demo"
git push -u origin feature/demo

# En B
git fetch origin
git switch --track origin/feature/demo
git branch -vv
```
Estado esperado: en B, `feature/demo` sigue a `origin/feature/demo`.
