# 04. Ramas: crear, cambiar y fusionar

- [Introducción](#introducción)
- [Ramas para aislar trabajo](#ramas-para-aislar-trabajo)
- [Crear y cambiar de rama](#crear-y-cambiar-de-rama)
- [Fusionar: fast-forward vs commit de fusión](#fusionar-fast-forward-vs-commit-de-fusión)
- [Resolver conflictos sin drama](#resolver-conflictos-sin-drama)
- [Recursos adicionales](#recursos-adicionales)

## Introducción
Trabaja en paralelo sin miedo: crea ramas para cada tarea, cambia de contexto con rapidez y fusiona con claridad, resolviendo conflictos cuando aparezcan.

## Ramas para aislar trabajo
Una rama te da un espacio seguro para desarrollar una tarea sin afectar `main`. La idea es simple: bifurca, trabaja, confirma, y al terminar fusiona de vuelta. Esto reduce riesgo y facilita la revisión incremental.

## Crear y cambiar de rama
La forma más directa hoy es `git switch`:

```
git switch -c feature/saludo   # crea y mueve a la rama
# ...trabaja y confirma...
git switch main                # vuelve a main
```

También puedes crearla sin moverte (`git branch feature/saludo`) y luego cambiar. Usa nombres descriptivos y cortos.

## Fusionar: fast-forward vs commit de fusión
Si `main` no avanzó desde que bifurcaste, la fusión puede ser un avance rápido (fast-forward), sin crear commits extra:

```
git switch main
git merge feature/saludo    # fast-forward si no hay divergencia
```

Si hubo cambios en ambas ramas, Git crea un commit de fusión para unir historias. Puedes forzarlo para dejar rastro explícito:

```
git merge --no-ff feature/saludo
```

## Resolver conflictos sin drama
Un conflicto indica que Git no puede decidir qué versión conservar. Abre el archivo y busca marcadores `<<<<<<<`, `=======`, `>>>>>>>`. Edita para quedarte con la combinación correcta, añade y continúa:

```
# tras el conflicto
git status
# edita archivos conflictivos
git add archivo.conflictivo
git merge --continue
```

Apóyate en tu editor o herramientas de diff para comparar con claridad antes de confirmar la resolución.

## Recursos adicionales
> **Enlaces externos**: Los enlaces se abren en la misma pestaña. Usa Ctrl+Click (Windows/Linux) o Cmd+Click (Mac) para abrirlos en pestaña nueva.

- <a href="https://git-scm.com/docs/git-branch" target="_blank">git-branch</a>
- <a href="https://git-scm.com/docs/git-switch" target="_blank">git-switch</a>
- <a href="https://git-scm.com/docs/git-merge" target="_blank">git-merge</a>
- <a href="https://git-scm.com/docs/git-status" target="_blank">git-status</a>
