# 01. Introducción al control de versiones y a Git

- [Introducción](#introducción)
- [Qué problema resuelve el control de versiones](#qué-problema-resuelve-el-control-de-versiones)
- [Por qué Git: instantáneas, no parches](#por-qué-git-instantáneas-no-parches)
- [Áreas de trabajo: directorio, staging y repositorio](#áreas-de-trabajo-directorio-staging-y-repositorio)
- [Terminología mínima para orientarte](#terminología-mínima-para-orientarte)
- [Recursos adicionales](#recursos-adicionales)

## Introducción
Contexto, problemas que resuelve el control de versiones y por qué Git se convirtió en el estándar de facto. Terminología mínima y modelo mental para empezar con buen pie.

## Qué problema resuelve el control de versiones
Si alguna vez has guardado un archivo como `propuesta_final_definitiva_v3(2).docx`, ya has sentido la necesidad de controlar versiones. El control de versiones evita la proliferación de copias, permite comparar estados, volver atrás con seguridad y trabajar en paralelo sin pisarnos. En equipos, añade trazabilidad y responsabilidad: cada cambio tiene autor, momento y propósito.

Git propone un enfoque distribuido: cada persona tiene una copia completa del historial y puede trabajar incluso sin conexión. Esto reduce la dependencia de un servidor central, acelera operaciones locales y favorece flujos flexibles.

## Por qué Git: instantáneas, no parches
Mientras otros sistemas piensan en “deltas”, Git piensa en instantáneas del árbol de archivos. Cada confirmación (commit) guarda un estado coherente del proyecto y un puntero a su padre. Con esto, Git reconstruye la historia con integridad criptográfica (hashes) y operaciones muy rápidas en local.

A nivel práctico, esto se traduce en que revertir, comparar o bifurcar la historia es barato. También facilita estrategias de trabajo como crear ramas para cada tarea y fusionarlas cuando están listas.

## Áreas de trabajo: directorio, staging y repositorio
Git separa el trabajo en tres zonas: el directorio de trabajo, donde editas archivos; el área de preparación (staging), donde seleccionas exactamente qué cambios entrarían en el siguiente commit; y el repositorio (HEAD), que es el historial confirmado.

Incluso sin ejecutar comandos, conviene interiorizar el ciclo: editar → preparar → confirmar. Ese paso intermedio (staging) te da granularidad: puedes partir un cambio grande en varias confirmaciones pequeñas y claras. Este enfoque paso a paso y con ejemplos prácticos será el hilo conductor del curso, inspirado en un estilo didáctico similar al de un README formativo que explica primero el porqué y luego el cómo :contentReference[oaicite:0]{index=0}.

## Terminología mínima para orientarte
Un *commit* es un punto en el tiempo del proyecto, con autor, fecha y mensaje. Una *rama* es un puntero móvil a una secuencia de commits; `main` suele representar el estado estable. *HEAD* es el nombre simbólico del commit en el que estás. *Merge* es fusionar historias; puede ser directo (fast-forward) o con un commit de fusión si hay divergencia.

Primer mapa mental: trabaja en ramas pequeñas, confirma en unidades lógicas y usa mensajes que expliquen el “qué” y, sobre todo, el “por qué”.

## Recursos adicionales
> **Enlaces externos**: Los enlaces se abren en la misma pestaña. Usa Ctrl+Click (Windows/Linux) o Cmd+Click (Mac) para abrirlos en pestaña nueva.

- <a href="https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control" target="_blank">Git Book — Getting Started</a>
- <a href="https://git-scm.com/docs" target="_blank">Git Commands (Overview)</a>
- <a href="https://rogerdudler.github.io/git-guide" target="_blank">Git Guide (rogerdudler)</a>
