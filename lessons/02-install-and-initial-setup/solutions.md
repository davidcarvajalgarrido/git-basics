git --version
git config --global user.name  "Tu Nombre"
git config --global user.email "tu@ejemplo.com"
git config --global init.defaultBranch main
git config --global core.editor "code --wait"
git config --list --show-origin
echo -e ".DS_Store
Thumbs.db
*.log" >> ~/.gitignore_global
git config --global core.excludesfile ~/.gitignore_global
git config --global --get core.excludesfile
ssh-keygen -t ed25519 -C "tu@ejemplo.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub   # Copia y registra en GitHub
ssh -T git@github.com       # Debe saludar con tu usuario
# Lección 2 — Soluciones

## Ejercicio 1: Solución — Instala Git

```
git --version
# Si no está instalado, descárgalo desde https://git-scm.com/downloads y sigue el asistente de instalación.
git --version
```
Estado esperado: el comando muestra la versión de Git instalada.

## Ejercicio 2: Solución — Configura tu identidad

```
git config --global user.name  "Tu Nombre"
git config --global user.email "tu@email.com"
git config --list
```
Estado esperado: aparecen las claves `user.name` y `user.email` en la lista.

## Ejercicio 3: Solución — Personaliza la configuración básica

```
git config --global init.defaultBranch main
git config --global core.editor "notepad"  # O el editor que prefieras
git config --list
```
Explicación:
- `init.defaultBranch main`: Establece 'main' como rama por defecto al crear nuevos repositorios.
- `core.editor`: Define el editor de texto que usará Git para mensajes de commit y otras tareas.
