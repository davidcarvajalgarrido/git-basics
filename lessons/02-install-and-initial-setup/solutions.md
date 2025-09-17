# Lección 2 — Soluciones

## Ejercicio 1: Solución — Configuración

```
git --version
git config --global user.name  "Tu Nombre"
git config --global user.email "tu@ejemplo.com"
git config --global init.defaultBranch main
git config --global core.editor "code --wait"
git config --list --show-origin
```
Estado esperado: la lista incluye las claves anteriores, con origen `~/.gitconfig`.

## Ejercicio 2: Solución — .gitignore global

```
echo -e ".DS_Store
Thumbs.db
*.log" >> ~/.gitignore_global
git config --global core.excludesfile ~/.gitignore_global
git config --global --get core.excludesfile
# Debe imprimir la ruta a ~/.gitignore_global
```

## Ejercicio 3: Solución — SSH

```
ssh-keygen -t ed25519 -C "tu@ejemplo.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub   # Copia y registra en GitHub
ssh -T git@github.com       # Debe saludar con tu usuario
```
