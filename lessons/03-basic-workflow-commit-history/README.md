# 03. Flujo básico: crear repos, añadir, confirmar e historial

- [Introducción](#introducción)
- [Crear un repositorio (o clonar) y entender el estado](#crear-un-repositorio-o-clonar-y-entender-el-estado)
- [Preparar con intención y confirmar](#preparar-con-intención-y-confirmar)
- [Inspeccionar cambios e historial](#inspeccionar-cambios-e-historial)
- [Deshacer seguro en el día a día](#deshacer-seguro-en-el-día-a-día)
- [Recursos adicionales](#recursos-adicionales)

## Introducción
Del directorio vacío al primer historial útil. Aprenderás a preparar cambios con intención, confirmar con mensaje claro e inspeccionar lo que ha ocurrido.

## Crear un repositorio (o clonar) y entender el estado
Para empezar desde cero en un directorio existente:

```
git init
git status   # Verás 'No commits yet' y archivos no trackeados si existen
```

`git status` es tu panel de control: te dice qué está sin seguimiento, qué está preparado y en qué rama estás. Si vienes de un repositorio existente, `git clone <url>` te deja listo con historial y ramas remotas configuradas.

## Preparar con intención y confirmar
El área de *staging* te permite decidir exactamente qué entra en el siguiente commit. Puedes añadir por archivo o por fragmento:

```
git add README.md
git add -p src/app.js
git commit -m "Añade README inicial y configuración básica de app"
```

Piensa cada commit como una unidad lógica mínima: si mañana alguien revisa el historial, debería entender qué aporta y por qué.

## Inspeccionar cambios e historial
Antes de confirmar, compara lo que hay en juego:

```
git diff            # cambios en el directorio de trabajo
git diff --staged   # cambios ya preparados
```

Y navega el historial con diferentes niveles de detalle:

```
git log --oneline --graph --decorate
git show            # Detalle del último commit
```

## Deshacer seguro en el día a día
Cometer errores es normal; la clave es deshacer sin perder trabajo. Para retirar un archivo del staging:

```
git restore --staged archivo.txt
```

Para descartar cambios locales en un archivo (si aún no los confirmaste):

```
git restore archivo.txt
```

Y para corregir el mensaje o incluir algo olvidado en el último commit:

```
git commit --amend
```

## Recursos adicionales
> **Enlaces externos**: Los enlaces se abren en la misma pestaña. Usa Ctrl+Click (Windows/Linux) o Cmd+Click (Mac) para abrirlos en pestaña nueva.

- <a href="https://git-scm.com/docs/git-init" target="_blank">git-init</a>
- <a href="https://git-scm.com/docs/git-add" target="_blank">git-add</a>
- <a href="https://git-scm.com/docs/git-commit" target="_blank">git-commit</a>
- <a href="https://git-scm.com/docs/git-log" target="_blank">git-log</a>
- <a href="https://git-scm.com/docs/git-restore" target="_blank">git-restore</a>
- <a href="https://git-scm.com/docs/git-diff" target="_blank">git-diff</a>
