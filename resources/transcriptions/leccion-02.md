# Lección 2: Repaso, dudas y ramas en Git

## 1. Lo más importante explicado por David (teoría)

- **Diferencia entre Git y GitHub:** Git es la herramienta local de control de versiones, GitHub es una plataforma online para alojar repositorios y colaborar. Puedes usar Git sin GitHub.
- **Instalación y configuración:** Es importante usar la herramienta oficial de Git y configurar usuario/correo. Se recomienda practicar con comandos antes que con herramientas gráficas.
- **Flujo básico de trabajo (repaso):**
  1. Inicializar repositorio (`git init`).
  2. Añadir archivos al staging (`git add`).
  3. Confirmar cambios con commit (`git commit`).
  4. Consultar el historial (`git log`).
- **Naming conventions:** Recomendación de usar camelCase, kebab-case o snake_case para nombres de archivos/carpetas, evitando espacios, tildes y eñes.
- **Ramas (branches):**
  - Una rama es un espacio seguro y aislado para trabajar en paralelo sin afectar la rama principal.
  - Permiten probar cosas nuevas sin riesgo.
  - Comandos clave:
    - `git branch nombre`: Crear rama.
    - `git switch nombre`: Cambiar de rama.
    - `git branch -d nombre`: Borrar rama.
    - `git log --oneline --graph`: Ver historial de ramas.
  - Las ramas son como universos paralelos: lo que ocurre en una no afecta a las demás hasta que se integran (merge).
- **Merge (integración):**
  - Integrar cambios de una rama secundaria a la principal.
  - Si no hay cambios en conflicto, el merge es automático (fast-forward).
  - Si hay conflictos, hay que resolverlos manualmente.

## 2. Preguntas de los alumnos y respuestas de David

- **¿Git es gratis? ¿GitHub tiene limitaciones?**
  - Git es totalmente gratis. GitHub tiene planes gratuitos y de pago, pero puedes usar Git sin GitHub.

- **¿Hace falta algún archivo especial para trabajar con los ejercicios?**
  - No, los ejercicios son opcionales. Lo importante es aplicar lo aprendido al trabajo real.

- **¿Qué pasa si hago git init en la carpeta equivocada?**
  - Borra la carpeta `.git` y vuelve a inicializar en la correcta.

- **¿Cómo trabajar con carpetas con espacios?**
  - Mejor evitar espacios. Si los hay, usar comillas o el carácter de escape (`\`).

- **¿Cómo nombrar archivos/carpetas?**
  - Usar camelCase, kebab-case o snake_case. Elegir una convención y mantenerla.

- **¿Para qué sirve git add? ¿Hay que hacerlo para cada archivo?**
  - Añade archivos al staging. Puedes añadir uno, varios o todos a la vez.

- **¿Qué diferencia hay entre commit y push?**
  - Commit guarda cambios localmente. Push los sube al repositorio remoto.

- **¿Cómo ver el historial de commits de forma visual?**
  - Usar `git log --oneline --graph`.

- **¿Qué pasa si hago cambios en varios archivos y solo quiero confirmar algunos?**
  - Añade solo los que quieras al staging antes de hacer commit.

- **¿Qué pasa si hago git init en la carpeta de usuario?**
  - Versionarás todo tu usuario, lo cual no es recomendable. Borra `.git` y hazlo en la carpeta correcta.
