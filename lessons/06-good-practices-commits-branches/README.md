# 06. Buenas prácticas iniciales

- [Introducción](#introducción)
- [Commits atómicos y mensajes que cuentan una historia](#commits-atómicos-y-mensajes-que-cuentan-una-historia)
- [Ramas sencillas y de vida corta](#ramas-sencillas-y-de-vida-corta)
- [Repo limpio: .gitignore, artefactos y limpieza](#repo-limpio-gitignore-artefactos-y-limpieza)
- [Atajos útiles con alias](#atajos-útiles-con-alias)
- [Recursos adicionales](#recursos-adicionales)

## Introducción
Pequeñas decisiones que marcan grandes diferencias: commits atómicos, mensajes útiles, ramas ordenadas y un repo sin ruido.

## Commits atómicos y mensajes que cuentan una historia
Un commit debería representar un cambio coherente y revisable. Si el título explica el qué y el cuerpo el porqué, el futuro tú (y tu equipo) lo agradecerán. Evita “arreglo cosas”; mejor “Corrige desbordamiento al calcular total en carrito”.

Antes de confirmar, pregúntate: ¿puedo dividir esto en dos cambios más pequeños? ¿He dejado pistas suficientes en el mensaje para entender la decisión?

## Ramas sencillas y de vida corta
Mantén `main` estable y crea ramas de feature para cada tarea. Cuanto más cortas, menos conflictos y más fácil revisar. Al fusionar, elimina ramas que ya no se usan para reducir ruido:

```
git branch -d feature/ya-fusionada
git push origin --delete feature/ya-fusionada
```

## Repo limpio: .gitignore, artefactos y limpieza
No subas artefactos generados. Si ya se colaron, sácalos del índice y evita futuros sustos:

```
git rm -r --cached dist/
echo "dist/" >> .gitignore
git commit -m "Deja de versionar artefactos de build"
```

Para hacer limpieza local (con cuidado):

```
git clean -ndx   # vista previa de lo que se borraría
git clean -fdX   # borra solo ignorados (no rastreados permanecen)
```

## Atajos útiles con alias
Define alias para comandos largos o combinaciones habituales. Esto acelera y estandariza:

```
git config --global alias.lg "log --oneline --graph --decorate --all"
git config --global alias.st "status -sb"
```

A partir de ahora, `git lg` y `git st` estarán disponibles en tu entorno.

## Recursos adicionales
> **Enlaces externos**: Los enlaces se abren en la misma pestaña. Usa Ctrl+Click (Windows/Linux) o Cmd+Click (Mac) para abrirlos en pestaña nueva.

- <a href="https://git-scm.com/docs/git-commit" target="_blank">git-commit</a>
- <a href="https://git-scm.com/docs/git-clean" target="_blank">git-clean</a>
- <a href="https://git-scm.com/docs/git-rm" target="_blank">git-rm</a>
- <a href="https://git-scm.com/docs/git-config" target="_blank">git-config (aliases)</a>
- <a href="https://www.atlassian.com/git/tutorials/saving-changes" target="_blank">Atlassian — Git Best Practices</a>
