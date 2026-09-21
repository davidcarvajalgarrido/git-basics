# Lección 2 — Soluciones

## Ejercicio 1: Solución — Instala y verifica Git

```
git --version
git help -g
```
Estado esperado: se imprime un número de versión de Git y un listado de guías disponibles.

## Ejercicio 2: Solución — Configura tu identidad

```
git config --global user.name  "Tu Nombre"
git config --global user.email "tu@ejemplo.com"
git config --global --list
```
Estado esperado: la lista incluye `user.name` y `user.email` con los valores establecidos.

## Ejercicio 3: Solución — Origen de la configuración

```
git config --list --show-origin
git config --get user.email
```
Estado esperado: cada línea del primer comando muestra la ruta del archivo (normalmente `~/.gitconfig`) junto al valor; el segundo comando imprime solo tu correo.

## Ejercicio 4: Solución — Autenticación SSH

```
ssh-keygen -t ed25519 -C "tu@ejemplo.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub   # Copia y registra en GitHub
ssh -T git@github.com       # Debe saludar con tu usuario
```
Estado esperado: GitHub responde con un saludo confirmando tu usuario. SSH evita introducir usuario/contraseña o token en cada operación con el remoto, ya que la autenticación se basa en el par de claves.
