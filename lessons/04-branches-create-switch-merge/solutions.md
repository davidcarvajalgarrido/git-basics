# Lección 4 — Soluciones

## Ejercicio 1: Solución — Fast-forward

```
git switch -c feature/saludo
echo "hola" > saludo.txt
git add saludo.txt
git commit -m "Añade saludo.txt"
git switch main
git merge feature/saludo
git log --oneline --graph --decorate
```
Estado esperado: no aparece un commit de merge; `main` avanza a la punta de `feature/saludo`.

## Ejercicio 2: Solución — Merge con --no-ff

```
git switch -c feature/log
echo "log A" > log.txt
git add log.txt && git commit -m "Añade log en feature"
git switch main
echo "otra cosa" > otra.txt
git add otra.txt && git commit -m "Añade cambio en main"
git merge --no-ff feature/log -m "Merge feature/log"
git log --oneline --graph --decorate
```
Estado esperado: aparece un commit explícito de merge.

## Ejercicio 3: Solución — Conflicto y resolución

```
# En main
echo "Línea común" > README.md
git add README.md && git commit -m "Línea base"
# Cambia la línea en main
echo "Línea en main" > README.md
git add README.md && git commit -m "Cambia línea en main"
# Rama con cambio distinto
git switch -c feature/conflicto HEAD~1
echo "Línea en feature" > README.md
git add README.md && git commit -m "Cambia línea en feature"
# Intento de fusión que genera conflicto
git switch main
git merge feature/conflicto
# Edita README.md para resolver, luego:
git add README.md
git merge --continue
git log --oneline --graph --decorate
```
