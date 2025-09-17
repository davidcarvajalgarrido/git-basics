# 02. Instalación y configuración inicial

- [Introducción](#introducción)
- [Instalar y verificar](#instalar-y-verificar)
- [Identidad, editor y rama por defecto](#identidad-editor-y-rama-por-defecto)
- [SSH y credenciales: panorama rápido](#ssh-y-credenciales-panorama-rápido)
- [Ignorar archivos con .gitignore (local y global)](#ignorar-archivos-con-gitignore-local-y-global)
- [Recursos adicionales](#recursos-adicionales)

## Introducción
Instala Git, valida la versión y deja lista tu identidad, editor y preferencias básicas. Cierra con la configuración de .gitignore para mantener el repo limpio.

## Instalar y verificar
Descarga Git desde el sitio oficial e instala según tu sistema. Verifica que todo está en orden ejecutando:

```
git --version
git help -g   # índice de guías disponibles
```

Si ves un número de versión y no hay errores, ya puedes continuar. Mantener Git actualizado evita incompatibilidades y te da acceso a mejoras de usabilidad como `git switch` o `git restore`.

## Identidad, editor y rama por defecto
Antes del primer commit, define tu identidad global. Así quedará registrada en el historial de cada cambio que confirmes:

```
git config --global user.name  "Tu Nombre"
git config --global user.email "tu@ejemplo.com"
```

Configura también el editor y colores. Y, muy recomendable, establece el nombre por defecto de la rama inicial como `main`:

```
git config --global core.editor "code --wait"
git config --global color.ui auto
git config --global init.defaultBranch main
```

Puedes inspeccionar lo configurado y dónde se guardó cada opción:

```
git config --list --show-origin
```

## SSH y credenciales: panorama rápido
Al trabajar con remotos, autenticarse sin contraseñas planas es clave. La vía habitual es SSH. Crea una clave y añádela a tu proveedor (p. ej. GitHub):

```
# Genera una clave moderna (ed25519) con comentario
ssh-keygen -t ed25519 -C "tu@ejemplo.com"
# Inicia el agente y añade tu clave
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

Copia la clave pública y regístrala en tu cuenta. Más detalles en la guía oficial de GitHub sobre SSH.

## Ignorar archivos con .gitignore (local y global)
Mantén fuera del historial archivos generados (builds, dependencias, temporales). Empieza con una plantilla sensata y adáptala:

```
# .gitignore del proyecto
node_modules/
dist/
.DS_Store
*.log
```

También puedes crear un `.gitignore` global para todos tus repos:

```
git config --global core.excludesfile ~/.gitignore_global
echo ".DS_Store" >> ~/.gitignore_global
echo "Thumbs.db"  >> ~/.gitignore_global
```

## Recursos adicionales
> **Enlaces externos**: Los enlaces se abren en la misma pestaña. Usa Ctrl+Click (Windows/Linux) o Cmd+Click (Mac) para abrirlos en pestaña nueva.

- <a href="https://git-scm.com/docs/git-config" target="_blank">git-config</a>
- <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh" target="_blank">Connecting to GitHub with SSH</a>
- <a href="https://github.com/github/gitignore" target="_blank">github/gitignore (plantillas)</a>
