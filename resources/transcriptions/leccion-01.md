# Lección 1: Introducción a Git y control de versiones

## 1. Lo más importante explicado por David (teoría)

- **Definición de Git:** Git es un sistema de control de versiones distribuido basado en cambios. Permite llevar un registro de la historia de un proyecto, como un diario o cuaderno de bitácora, guardando los diferentes estados por los que pasa un conjunto de ficheros.
- **Diferencia entre centralizado y distribuido:** En sistemas centralizados (como SVN), todo pasa por un servidor central. En sistemas distribuidos (como Git), cada usuario tiene una copia completa del repositorio y puede trabajar de forma independiente.
- **Repositorio:** Un repositorio es un proyecto (conjunto de ficheros y carpetas) con control de versiones. Si no tiene control de versiones, es solo una carpeta.
- **Basado en cambios:** Git guarda solo los cambios (diferencias) entre versiones, no copias completas de los ficheros.
- **Origen de Git:** Creado por Linus Torvalds para el desarrollo del kernel de Linux, permitiendo a miles de personas colaborar en diferentes zonas horarias.
- **Herramientas y documentación:** Se recomienda usar la herramienta oficial de Git y consultar el libro Pro Git solo como referencia, no para aprender desde cero.
- **Instalación y configuración:** Es importante instalar Git desde la fuente oficial y configurar el usuario y correo global. El editor de texto por defecto puede cambiarse durante la instalación.
- **Flujo básico de trabajo:**
  1. Trabajar en los ficheros (working directory).
  2. Añadir cambios al área de preparación (staging area) con `git add`.
  3. Confirmar los cambios con un commit (`git commit`).
  4. Consultar el estado con `git status` y el historial con `git log`.
- **Comandos clave:**
  - `git init`: Inicializa un repositorio.
  - `git status`: Muestra el estado de los archivos.
  - `git add`: Añade archivos al área de preparación.
  - `git commit -m "mensaje"`: Confirma los cambios.
  - `git log`: Muestra el historial de commits.
- **Recomendaciones:**
  - Hacer commits solo de trabajo terminado o funcional.
  - Es mejor tener muchos repositorios pequeños que uno grande.
  - No usar caracteres raros ni espacios en nombres de archivos/carpetas.
  - Los commits pueden fusionarse o eliminarse si es necesario.

## 2. Preguntas de los alumnos y respuestas de David

- **¿Qué pasa si hago git init en la carpeta equivocada?**
  - Puedes borrar la carpeta `.git` y volver a inicializar en la correcta. No pasa nada grave.

- **¿Qué editor elegir si no programo?**
  - Cualquier editor de texto plano, incluso el Bloc de notas. Evitar VI/VIM si no se conoce.

- **¿Se puede tener varios repositorios?**
  - Sí, lo recomendable es tener un repositorio por proyecto.

- **¿Qué pasa si modifico un archivo después de añadirlo al staging area?**
  - Los cambios posteriores no están en el staging hasta que vuelvas a hacer `git add`.

- **¿Se puede hacer commit de solo algunos archivos?**
  - Sí, solo los que añadas al staging con `git add`.

- **¿Qué pasa si hago commit de más?**
  - Se pueden fusionar o eliminar commits después.

- **¿Cómo moverse entre carpetas en Git Bash?**
  - Usar `cd` para cambiar de directorio, `ls` para listar archivos y `pwd` para ver la ruta actual.

- **¿Qué es el hash de un commit?**
  - Es un identificador único para cada commit, útil para comparar, volver atrás o consultar cambios.

- **¿Cuándo hacer push?**
  - Cuando quieras subir tus commits locales al repositorio remoto. Hasta entonces, todo es local.

- **¿Se puede volver atrás en los commits?**
  - Sí, Git permite retroceder a estados anteriores.
