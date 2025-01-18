## Preguntas:

1. **¿Qué es Git y para qué sirve?**

   Git sirve para organizar y gestionar el desarrollo de proyectos, especialmente si es para trabajar en equipo.
   Sirve para guardar el historial de cambios, trabajar en conjunto y sincronizar el trabajo entre dispositivos.

2. **¿Cuáles son las ventajas de usar Git?**

   Organización, eficiencia y seguridad.

3. **¿Qué diferencia hay entre Git y GitHub/GitLab/Bitbucket?**

   Git se enfoca en gestionar y registrar cambios en el código, mientras que GitHub/GitLab/Bitbucket son plataformas online que permiten almacenar y compartir ese código, esto hace que fluya la colaboración con otros en un proyecto pero igualmente estarían basándose en Git para el control de versiones.

4. **¿Qué hacen los siguientes comandos Git?**:  
   `clone`, `add`, `commit`, `push`, `pull`, `branch`, `merge`, `checkout`)

`git clone` Crea una copia local de un repo remoto.
`git add` Añade cambios en los archivos a la staging area para que puedan ser incluidos en el siguiente commit.
`git commit` Registra los cambios añadidos a la staging area con un mensaje descriptivo. 
`git push` Envía los commits locales a un repositorio remoto (tipo GitHub) para que los otros que estén trabajando en el proyecto lo integren en el código.
`git pull` Descarga los cambios del repo remoto y los fusiona/une/integra con la copia local, así el repo está actualizado.
`git branch` Muestra las ramas existentes en el proyecto o permite crear una nueva rama. Esto con el fin de no afectar la rama principal.
`git merge` Integra los cambios realizados en una rama de desarrollo a la rama principal o en otra rama. 
`git checkout` Cambia a otra branch o restaura archivos a un estado anterior. También se utiliza para crear una nueva branch.
 
5. **¿Qué es un repositorio y cuáles son los tipos de repositorios que existen?**

   Un repo es lo que se usa para almacenar y gestionar el código fuente y otros archivos de un proyecto.
   Repositorio local: se almacena en nuestra compu.
   Repositorio remoto: se almacena online (como GitHub o GitLab).
   Repositorio público: cualquier persona puede acceder.
   Repositorio privado: su contenido solo es visible para las personas que estén autorizadas.

6. **¿Qué son los "branch" en Git y para qué se utilizan?**

   Las ramas/branch en Git permiten trabajar de manera aislada en diferentes tareas. Estas se usan para desarrollar nuevas características del proyecto, corregir bugs, probar una librería, etc.

7. **Describe un flujo de trabajo típico con Git.  (Ejemplo: Gitflow)**
   # Inicializar el repo en caso de no haberlo hecho antes
   git init
   # Agregar el archivo
   git add nhera.txt
   # Hacer el primer commit
   git commit -m "Cambio footer"
   # Si es la primera vez, configuro el repo remoto y subo los cambios
   git remote add origin https://github.com/nhera/landing.git
   git push -u origin main
   # Antes de comenzar una nueva implementación, traigo los últimos cambios
   git pull origin main
   # Creo una nueva branch para la nueva implementación
   git checkout -b feature/nueva-implementacion
   # Agrego los cambios
   git add .
   # Hago commit
   git commit -m "Nueva implementación agregada"
   # Cambiar a la branch principal
   git checkout main
   # Usar los cambios de la branch feature/nueva-implementacion
   git merge feature/nueva-implementacion
   # Subo estos cambios al repo remoto
   git push origin main

   
8. **¿Qué es un "merge conflict" y cómo se resuelve?**

   Un "merge conflict" ocurre cuando Git no puede fusionar/unir automáticamente dos ramas porque los cambios afectan la misma parte de un archivo de manera diferente, por ejemplo, una persona elimina una línea de código que otro editó.
   Se resuelve identificando el conflicto en los archivos, editándolo, se agrega el archivo resuelto y se hace commit.
