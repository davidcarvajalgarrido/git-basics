# Lección 4: Repositorios remotos, clones y colaboración en Git

## 1. Lo más importante explicado por David (teoría)

- **Repaso del flujo básico de Git:** Se recuerda el flujo de trabajo local: crear ramas, trabajar en ellas y fusionar (merge) a la rama principal solo cuando el trabajo está listo. Lo que ocurre en una rama no afecta a las demás hasta que se integran.
- **Resolución de conflictos:** Git detecta conflictos solo cuando hay cambios distintos en la misma línea del mismo archivo. Si dos personas editan la misma línea de forma diferente, hay conflicto; si editan líneas distintas o hacen el mismo cambio, no hay conflicto. Los conflictos se resuelven manualmente, eligiendo qué cambios mantener.
- **Herramientas visuales para conflictos:** Se recomienda usar herramientas visuales para facilitar la resolución de conflictos, aunque es importante entender el proceso manual.
- **Trabajo en equipo y repositorios remotos:** Se introduce el trabajo colaborativo usando un servidor remoto (como GitHub). Se explica la diferencia entre trabajar solo en local y trabajar en común con otros.
- **Diferencia entre crear y clonar un repositorio:**
  - Opción A: "Yo soy el que crea el repo" (git init). Se inicializa un repositorio desde cero en una carpeta local.
  - Opción B: "Clonar un repo existente" (git clone). Se descarga una copia completa de un repositorio ya existente en un servidor remoto. Solo una persona debe hacer `git init`; el resto debe clonar.
- **Repositorios públicos y privados:** Si el repositorio es público, cualquiera puede clonarlo. Si es privado, se requieren credenciales y ser añadido como colaborador.
- **Ventajas de los repositorios remotos:** Permiten tener un backup y compartir el trabajo. Si algo sale mal en local, se puede borrar y volver a clonar el repositorio.
- **Práctica recomendada:** Trabajar en ramas, subir solo el trabajo terminado y no tener miedo a borrar y volver a clonar si es necesario.

## 2. Preguntas de los alumnos y respuestas de David

- **¿Qué pasa si el repositorio remoto (Nextcloud) está caído?**
  - No se puede acceder ni clonar hasta que vuelva a estar disponible. Es importante tener alternativas y backups.

- **¿Qué ocurre si hago git init y luego borro la carpeta?**
  - Puedes volver a clonar el repositorio desde el remoto y tendrás exactamente lo mismo que antes.

- **¿Qué pasa si el repositorio es privado?**
  - Se pedirá usuario y contraseña de la plataforma (GitHub). Hay que estar registrado y ser añadido como colaborador.

- **¿Puedo borrar mi copia local y volver a empezar?**
  - Sí, mientras el repositorio esté en el remoto, puedes borrar tu copia local y clonar de nuevo sin problema.

- **¿Qué diferencia hay entre crear y clonar un repositorio?**
  - Solo una persona debe inicializar (`git init`) y subir el repositorio. El resto debe clonar (`git clone`).

- **¿Qué pasa si hago git init en una carpeta que ya es un repositorio clonado?**
  - No es necesario ni recomendable. Solo se hace una vez al crear el repositorio.
