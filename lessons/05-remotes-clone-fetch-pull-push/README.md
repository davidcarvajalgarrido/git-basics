# 05. Repositorios remotos: clonar, fetch, pull y push

- [Introducción](#introducción)
- [Qué es un remoto y cómo se nombra](#qué-es-un-remoto-y-cómo-se-nombra)
- [Clonado inicial](#clonado-inicial)
- [Traer y mezclar cambios: fetch vs pull](#traer-y-mezclar-cambios-fetch-vs-pull)
- [Publicar trabajo: push y upstream](#publicar-trabajo-push-y-upstream)
- [Recursos adicionales](#recursos-adicionales)

## Introducción
Aprende a conectar tu repo local con un remoto, sincronizar cambios y compartir trabajo con el equipo con seguridad.

## Qué es un remoto y cómo se nombra
Un remoto es un repositorio accesible por red (o ruta local) que actúa como punto de sincronización. Por convención, `origin` es el nombre del remoto principal. Puedes tener varios remotos para diferentes fines (backup, forks).

Lista y examina remotos:

```
git remote -v
git remote add origin git@github.com:tuusuario/tu-repo.git
git remote rename origin primary
```

## Clonado inicial
Para empezar desde un proyecto existente:

```
git clone git@github.com:org/proyecto.git
cd proyecto
git branch -vv         # ver ramas locales y su upstream
```

El clon configura `origin` y crea una rama local que sigue a la rama por defecto del remoto.

## Traer y mezclar cambios: fetch vs pull
`git fetch` descarga objetos y referencias sin tocar tu rama actual; `git pull` es un fetch seguido de merge o rebase. Empezar con `--ff-only` evita merges accidentales:

```
git fetch origin
git log --oneline --decorate --graph --all
git pull --ff-only
```

Si hay divergencia, revisa y decide cómo integrar antes de continuar.

## Publicar trabajo: push y upstream
Para subir tu rama y establecer el seguimiento remoto:

```
git push -u origin main
```

A partir de ahí, basta con `git push` y `git pull` sin parámetros desde esa rama. Para nuevas ramas:

```
git switch -c feature/api
git push -u origin feature/api
```

## Recursos adicionales
> **Enlaces externos**: Los enlaces se abren en la misma pestaña. Usa Ctrl+Click (Windows/Linux) o Cmd+Click (Mac) para abrirlos en pestaña nueva.

- <a href="https://git-scm.com/docs/git-remote" target="_blank">git-remote</a>
- <a href="https://git-scm.com/docs/git-clone" target="_blank">git-clone</a>
- <a href="https://git-scm.com/docs/git-fetch" target="_blank">git-fetch</a>
- <a href="https://git-scm.com/docs/git-pull" target="_blank">git-pull</a>
- <a href="https://git-scm.com/docs/git-push" target="_blank">git-push</a>
- <a href="https://www.atlassian.com/git/tutorials/syncing" target="_blank">Atlassian — Remotes</a>
