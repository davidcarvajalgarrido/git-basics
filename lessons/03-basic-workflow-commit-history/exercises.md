# Lección 3 — Ejercicios

## Ejercicio 1: Tu primer repo y primer commit

1. Crea un directorio e inicialízalo con `git init`.
2. Ejecuta `git status` y observa el mensaje de "no commits yet".
3. Crea `README.md`, añádelo y confirma con un mensaje claro.
4. Ejecuta `git status` de nuevo y comprueba que el árbol de trabajo está limpio.

## Ejercicio 2: Un segundo commit, paso a paso

1. Modifica `README.md` y crea un nuevo archivo.
2. Ejecuta `git status` antes de añadir nada.
3. Añade los cambios y vuelve a ejecutar `git status` para ver cómo cambia lo que aparece en staging.
4. Confirma con un segundo commit.

## Ejercicio 3: Compara commits con diff

1. Modifica de nuevo algún archivo sin confirmar todavía.
2. Usa `git diff` para ver los cambios en el directorio de trabajo.
3. Añade los cambios y usa `git diff --staged` para ver lo mismo ya preparado.
4. Confirma el cambio y usa `git diff` entre los dos últimos commits para comprobar la diferencia.

## Ejercicio 4: Explora el historial

1. Ejecuta `git log` y revisa la información detallada de cada commit.
2. Ejecuta `git log --oneline` y compara la legibilidad frente al anterior.
3. Añade `--graph --decorate` a `git log --oneline` y observa qué información nueva aparece.

## Ejercicio 5 (avanzado, para espabilados): Recupera el hilo con el reflog

Esto no lo hemos visto en clase, así que toca investigar por tu cuenta:

1. Investiga qué es y para qué sirve `git reflog`.
2. Haz un par de commits más y luego consulta el reflog: ¿qué diferencia hay con `git log`?
3. Averigua cómo usarías el reflog para volver a un commit anterior si te "pierdes" en el historial.
