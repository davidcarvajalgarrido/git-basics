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
