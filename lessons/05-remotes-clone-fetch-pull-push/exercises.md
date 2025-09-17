# Lección 5 — Ejercicios

## Ejercicio 1: Conecta un remoto y publica main

1. Crea o usa un repo local con al menos un commit.
2. Añade un remoto llamado `origin` (GitHub, GitLab o un bare local).
3. Haz `git push -u origin main` y verifica `git branch -vv`.

## Ejercicio 2: Clona y sincroniza

1. Clona el repo en otra carpeta.
2. Crea un commit en uno de los clones y publícalo.
3. En el otro, ejecuta `git fetch` y `git pull --ff-only`.

## Ejercicio 3: Crea y comparte una rama de feature

1. Desde el clon A, crea `feature/demo` y súbela con `-u`.
2. Desde el clon B, tráela y cámbiate a ella con seguimiento.
