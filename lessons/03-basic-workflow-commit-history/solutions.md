# Lección 3 — Soluciones

## Ejercicio 1: Solución — Primer repo y primer commit

```
mkdir mi-repo && cd mi-repo
git init
git status
echo "# Mi proyecto" > README.md
git add README.md
git commit -m "Crea README inicial"
git status
```
Estado esperado: el primer `git status` muestra "No commits yet" y `README.md` como sin seguimiento; el segundo muestra el árbol de trabajo limpio tras el commit.

## Ejercicio 2: Solución — Segundo commit paso a paso

```
echo "Más contenido" >> README.md
echo "Notas del curso" > notas.txt
git status
git add README.md notas.txt
git status
git commit -m "Añade notas y amplía el README"
```
Estado esperado: el primer `git status` lista ambos archivos como cambios no preparados; el segundo los muestra en staging, listos para confirmarse.

## Ejercicio 3: Solución — Compara con diff

```
echo "Una línea más" >> notas.txt
git diff
git add notas.txt
git diff --staged
git commit -m "Añade una línea a notas"
git diff HEAD~1 HEAD
```
Estado esperado: `git diff` muestra el cambio antes de preparar; `git diff --staged` muestra el mismo cambio ya en staging; `git diff HEAD~1 HEAD` muestra la diferencia entre los dos últimos commits.

## Ejercicio 4: Solución — Explora el historial

```
git log
git log --oneline
git log --oneline --graph --decorate
```
Estado esperado: `git log` muestra autor, fecha y mensaje completo de cada commit; `git log --oneline` condensa cada commit a una línea; añadir `--graph --decorate` muestra la topología de ramas y las referencias (como `HEAD -> main`).

## Ejercicio 5: Solución — Reflog

```
echo "cambio extra" >> notas.txt
git add notas.txt
git commit -m "Cambio extra en notas"
git reflog
```
Estado esperado: `git reflog` muestra un registro de todos los movimientos de `HEAD` (commits, cambios de rama, etc.), a diferencia de `git log`, que solo muestra el historial de commits alcanzables desde la rama actual. Para volver a un punto anterior, se puede usar `git reset --hard <hash-del-reflog>` una vez identificada la entrada deseada.
