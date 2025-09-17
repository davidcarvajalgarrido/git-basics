# Lección 6 — Soluciones

## Ejercicio 1: Solución — Mensaje mejorado

```
git log --oneline
git commit --amend -m "Corrige cálculo de totales en carrito evitando overflow"
git log -1 --pretty=full
```
Estado esperado: el último commit muestra el nuevo mensaje con contexto.

## Ejercicio 2: Solución — Combinar commits

```
echo "a" >> app.js
git add app.js && git commit -m "Añade función A"
echo "b" >> app.js
git add app.js && git commit -m "Añade función B"
git reset --soft HEAD~2
git commit -m "Implementa funciones A y B en un cambio coherente"
git log -1 --stat
```

## Ejercicio 3: Solución — Repo limpio

```
mkdir -p dist && echo "artefacto" > dist/out.txt
git add dist && git commit -m "Versiona artefacto (a propósito para el ejercicio)"
git rm -r --cached dist/
echo "dist/" >> .gitignore
git add .gitignore
git commit -m "Deja de versionar dist/ y actualiza .gitignore"
npm run build   # o comando de build equivalente
git status      # Debe permanecer limpio (dist/ ignorado)
```
