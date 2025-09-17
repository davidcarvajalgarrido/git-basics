# Lección 2 — Ejercicios

## Ejercicio 1: Configura tu entorno

1. Verifica `git --version`.
2. Define `user.name` y `user.email` globales.
3. Establece `init.defaultBranch` a `main` y el `core.editor`.
4. Lista la configuración y su origen.

## Ejercicio 2: Prepara .gitignore global

1. Crea `~/.gitignore_global` con entradas para tu sistema.
2. Apunta `core.excludesfile` a ese archivo.
3. Comprueba que la ruta quedó registrada.

## Ejercicio 3: Habilita SSH

1. Genera una clave SSH `ed25519` con comentario.
2. Añádela al agente y registra la pública en tu proveedor.
3. Prueba la conexión (`ssh -T git@github.com`).
