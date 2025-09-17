# Lección 4 — Ejercicios

## Ejercicio 1: Feature y fusión fast-forward

1. Crea `feature/saludo`, añade `saludo.txt` y confirma.
2. Vuelve a `main` y fusiona. Verifica que fue fast-forward.

## Ejercicio 2: Fuerza un commit de fusión

1. Crea `feature/log`, realiza un commit.
2. En `main`, realiza otro commit separado.
3. Fusiona `feature/log` con `--no-ff` y observa el commit de merge.

## Ejercicio 3: Provoca y resuelve un conflicto

1. En `main`, edita una misma línea de `README.md`.
2. En `feature/conflicto`, edita esa misma línea de forma distinta y confirma.
3. Intenta fusionar y resuelve el conflicto editando y continuando el merge.
