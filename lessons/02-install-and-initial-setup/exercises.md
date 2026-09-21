# Lección 2 — Ejercicios

## Ejercicio 1: Instala y verifica Git

1. Instala Git en tu sistema (o comprueba que ya lo tienes).
2. Verifica la versión instalada con `git --version`.
3. Consulta el índice de guías con `git help -g`.

## Ejercicio 2: Configura tu identidad

1. Define tu `user.name` global.
2. Define tu `user.email` global.
3. Lista toda la configuración global y confirma que ambos valores aparecen.

## Ejercicio 3: Revisa el origen de tu configuración

1. Ejecuta `git config --list --show-origin` y localiza el archivo donde vive cada valor.
2. Consulta un único valor concreto (por ejemplo, tu `user.email`) sin listar todo lo demás.

## Ejercicio 4 (avanzado, para espabilados): Autenticación SSH

Esto no lo hemos visto en clase, así que toca investigar por tu cuenta:

1. Genera una clave SSH `ed25519` con un comentario identificativo.
2. Añádela al agente SSH de tu sistema.
3. Registra la clave pública en tu proveedor (por ejemplo, GitHub) y prueba la conexión.
4. Investiga qué ventaja tiene usar SSH frente a HTTPS para autenticarte con un remoto.
