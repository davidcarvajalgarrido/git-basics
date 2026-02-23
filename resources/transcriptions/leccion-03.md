# Lección 3: Resolución de conflictos y buenas prácticas en Git

## 1. Lo más importante explicado por David (teoría)

- **Trabajo local vs remoto:** Todo lo que se hace en Git es local hasta que se hace un push a un repositorio remoto (como GitHub). Se recomienda trabajar en local y subir solo cuando el trabajo esté listo para compartir.
- **Ramas y flujo de trabajo:**
  - La rama principal (`main` o `master`) debe usarse solo para trabajo terminado y compartido.
  - Cada persona debe trabajar en ramas propias y fusionar (merge) a la principal solo cuando el trabajo esté listo.
  - Se recomienda crear ramas con `git branch -b nombre` y cambiarse a ellas para trabajar de forma aislada.
- **Merge y resolución de conflictos:**
  - Un merge integra los cambios de una rama secundaria a la principal.
  - Si hay cambios en el mismo archivo/línea en ambas ramas, se produce un conflicto que debe resolverse manualmente.
  - Git marca los conflictos en el archivo con delimitadores (`<<<<<<<`, `=======`, `>>>>>>>`). Hay que elegir con qué versión quedarse o combinar ambas.
  - Tras resolver el conflicto, se debe hacer un nuevo commit para confirmar la resolución.
  - Las herramientas gráficas pueden ayudar a resolver conflictos, pero es importante entender el proceso manual.
- **Historial y limpieza:**
  - Tras un merge exitoso, se recomienda borrar la rama secundaria.
  - El historial (`git log --oneline --graph`) muestra la evolución y fusiones de las ramas.
- **Buenas prácticas:**
  - No trabajar nunca directamente en la rama principal.
  - Hacer commits frecuentes y descriptivos.
  - Resolver los conflictos de forma consciente, eligiendo la mejor solución para el proyecto.
  - Entender que los conflictos son normales y parte del trabajo colaborativo.

## 2. Preguntas de los alumnos y respuestas de David

- **¿Se puede revertir un commit si rompe el proyecto?**
  - Sí, se puede volver a un commit anterior o deshacer cambios.

- **¿Qué pasa si hago commits en la rama principal?**
  - No es recomendable. Lo ideal es trabajar en ramas y fusionar solo el trabajo terminado.

- **¿Por qué la rama principal se llama main o master?**
  - Por convención. El nombre puede cambiarse, pero es importante que coincida local y remotamente.

- **¿Cómo limpiar la consola?**
  - Usar el comando `clear`.

- **¿Qué pasa si hay conflictos en varias líneas o archivos?**
  - Hay que resolver cada conflicto manualmente, eligiendo qué cambios mantener.

- **¿Qué ocurre si dos personas modifican la misma línea?**
  - Se genera un conflicto y hay que decidir cuál de los dos cambios se mantiene.

- **¿Qué ocurre si los cambios son en líneas distintas?**
  - Git puede fusionar automáticamente los cambios.

- **¿Qué hacer tras resolver un conflicto?**
  - Hacer `git add` al archivo resuelto y luego un commit para confirmar la resolución.

- **¿Por qué aparecen mensajes de advertencia en pull requests?**
  - Porque puede haber conflictos que tendrá que resolver el responsable del repositorio remoto.

- **¿Se pueden borrar ramas tras el merge?**
  - Sí, es recomendable borrar ramas que ya han sido fusionadas.
