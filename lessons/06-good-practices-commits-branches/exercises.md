# Lección 6 — Ejercicios

## Ejercicio 1: Mejora un mensaje de commit

1. Localiza un commit reciente con mensaje pobre.
2. Reescríbelo con `git commit --amend` agregando contexto.
3. Confirma que el nuevo mensaje aparece en `git log -1`.

## Ejercicio 2: Agrupa cambios relacionados en un solo commit

1. Realiza dos commits pequeños que pertenecen a la misma idea.
2. Usa `git reset --soft HEAD~2` para combinarlos y crea un único commit bien explicado.

## Ejercicio 3: Limpia artefactos y configura el ignore

1. Agrega un directorio `dist/` con archivos de prueba.
2. Deja de versionarlo con `git rm -r --cached dist/` y añade `dist/` a `.gitignore`.
3. Verifica que `git status` quede limpio tras construir de nuevo.
