# Git y GitHub

## 1. ¿Qué es Git?

### Concepto

Git es un sistema de control de versiones.

Un sistema de control de versiones permite registrar los cambios realizados en un proyecto y mantener un historial de su evolución.

Esto nos permite saber qué cambió, cuándo cambió y recuperar versiones anteriores cuando sea necesario.

### Conceptos importantes

- Git: herramienta que utilizamos para controlar las versiones de nuestros proyectos.
- Control de versiones: sistema que permite registrar y organizar los cambios realizados en un proyecto.
- Repositorio: carpeta de un proyecto que está siendo administrada por Git.
- Historial: registro de los cambios realizados en el proyecto.
- Commit: registro de un conjunto de cambios dentro del historial de Git.
- Rama (branch): línea independiente de desarrollo dentro de un repositorio.
- Repositorio local: repositorio almacenado en nuestro computador.
- Repositorio remoto: repositorio almacenado en otro lugar, normalmente un servidor, como GitHub.

### Idea clave

Git nos permite trabajar en un proyecto sin perder el historial de los cambios.


## 2. ¿Qué es GitHub?

### Concepto

GitHub es una plataforma que permite almacenar, compartir y colaborar en repositorios Git.

Git y GitHub no son lo mismo.

- Git: controla las versiones de nuestro proyecto.
- GitHub: permite almacenar y compartir nuestros repositorios Git en Internet.

### Nuestro proyecto

Nuestro repositorio es:

JERC2025/inicio-de-cero

La carpeta inicio-de-cero se encuentra en nuestro computador y contiene nuestro proyecto.

### Conceptos importantes

- GitHub: plataforma donde podemos almacenar y compartir repositorios Git.
- Repositorio remoto: copia del repositorio almacenada en un servidor.
- Repositorio local: copia del repositorio que tenemos en nuestro computador.
- Colaboración: trabajo conjunto entre varias personas sobre un mismo proyecto.

### Idea clave

Podemos pensar en Git y GitHub de esta manera:

Git = controla las versiones

GitHub = almacena y comparte el repositorio


## 3. Configuración inicial de Git

### Concepto

Git necesita conocer la identidad de la persona que realiza los cambios.

Para esto configuramos:

- Nombre de usuario: JERC2025
- Correo electrónico: el correo asociado a nuestra cuenta de GitHub.

Estos datos permiten que Git identifique quién realiza los cambios en un proyecto.

### Comandos

Los comandos utilizados para configurar nuestra identidad son:

git config --global user.name "JERC2025"

git config --global user.email "TU_CORREO"

El valor TU_CORREO representa el correo que configuramos realmente en nuestro computador. No debemos escribir literalmente TU_CORREO.

### ¿Qué significa --global?

La opción --global indica que la configuración se aplicará de forma general al usuario de este computador.

Esto significa que, normalmente, no tendremos que configurar nuestro nombre y correo nuevamente para cada repositorio.

### Conceptos importantes

- Configuración: conjunto de opciones que determinan cómo funciona un programa.
- Identidad: información que permite identificar quién realiza una acción.
- Global: configuración que se aplica de manera general al usuario.


## 4. Comprobar la instalación de Git

### Objetivo

Antes de trabajar con Git debemos comprobar que está instalado correctamente en nuestro computador.

### Comando

Utilizamos:

git --version

### Resultado obtenido

En nuestro computador obtuvimos:

git version 2.50.1 (Apple Git-155)

Esto confirma que Git está instalado y disponible desde la Terminal.

### ¿Qué significa cada parte?

- git: ejecuta Git.
- --version: solicita que Git muestre la versión instalada.
- 2.50.1: versión de Git instalada.
- Apple Git-155: distribución de Git proporcionada por Apple.

### Conceptos importantes

- Versión: edición específica de un programa.
- Distribución: versión de un software preparada o proporcionada por una organización.

### Idea clave

git --version es un comando de comprobación. No modifica nuestro proyecto.


## 5. Comprobar la configuración de Git

### Objetivo

Después de configurar nuestra identidad, debemos comprobar que Git realmente tiene guardados esos datos.

### Comando

Utilizamos:

git config --global --list

### ¿Qué hace?

Este comando muestra la configuración global de Git.

Comprobamos que aparecen correctamente:

- user.name
- user.email

### ¿Qué significa --list?

--list indica que queremos mostrar una lista de las configuraciones existentes.

### Conceptos importantes

- Configuración global: configuración que se aplica al usuario de Git en este computador.
- user.name: nombre que Git asociará a nuestros cambios.
- user.email: correo que Git asociará a nuestros cambios.

### Idea clave

Comprobar la configuración no modifica nada. Solamente nos permite verificar que los datos están configurados correctamente.


## 6. Comprobar el estado del repositorio

### Objetivo

Después de entrar en nuestro proyecto inicio-de-cero, utilizamos Git para conocer qué está ocurriendo actualmente dentro del repositorio.

### Comando

Utilizamos:

git status

### ¿Qué hace git status?

git status muestra el estado actual del repositorio.

Nos permite saber, entre otras cosas:

- En qué rama estamos.
- Si nuestro repositorio está sincronizado con el repositorio remoto.
- Qué archivos han sido modificados.
- Qué archivos todavía no están siendo rastreados por Git.
- Qué cambios están preparados para el próximo commit.

### Resultado que obtuvimos

Git mostró:

On branch main

Your branch is up to date with 'origin/main'.

Esto significa que:

- Estamos trabajando en la rama main.
- Nuestro repositorio local está actualizado respecto a origin/main.

También apareció:

modified: README.md

Esto significa que README.md ya era conocido por Git, pero su contenido fue modificado desde el último commit.

También apareció:

Untracked files:
CUADERNO/

### ¿Qué significa "untracked"?

Un archivo o carpeta untracked es un elemento que existe dentro del proyecto, pero que Git todavía no está siguiendo.

En nuestro caso:

CUADERNO/

es una carpeta que existe físicamente dentro de inicio-de-cero, pero todavía no había sido añadida al seguimiento de Git.

### ¿Qué significa "modified"?

Modified significa modificado.

Git ya conocía ese archivo, pero detectó que su contenido cambió después del último commit.

### ¿Qué significa "branch"?

Una branch o rama es una línea independiente de trabajo dentro de Git.

Nuestra rama actual es:

main

### ¿Qué significa "origin"?

origin es el nombre que Git utiliza normalmente para identificar el repositorio remoto principal.

En nuestro caso, origin apunta al repositorio remoto de nuestro proyecto en GitHub.

### Conceptos importantes

- Status: estado actual del repositorio.
- Branch: rama de trabajo.
- Main: rama principal que estamos utilizando.
- Origin: nombre utilizado para identificar nuestro repositorio remoto principal.
- Modified: archivo conocido por Git cuyo contenido cambió.
- Untracked: archivo o carpeta que Git todavía no está siguiendo.
- Repositorio local: copia del proyecto que tenemos en nuestro computador.
- Repositorio remoto: copia del proyecto almacenada en GitHub.

### Idea clave

git status es uno de los comandos más importantes de Git porque nos permite saber qué está pasando antes de realizar cualquier otra operación.


# Resumen de lo aprendido hasta ahora

1. Git controla las versiones de nuestros proyectos.
2. GitHub permite almacenar y compartir repositorios Git.
3. Git necesita una identidad configurada.
4. git --version permite comprobar que Git está instalado.
5. git config --global --list permite consultar la configuración global.
6. git status permite conocer el estado actual del repositorio.
7. Untracked significa que Git todavía no está siguiendo un archivo o carpeta.
8. Modified significa que Git detectó cambios en un archivo que ya conocía.
9. Branch significa rama de trabajo.
10. Origin identifica normalmente el repositorio remoto principal.

## Lo que todavía debemos aprender

- git add
- staging area
- git commit
- git log
- git push
- git pull
- La relación completa entre Git local y GitHub.
---

## 7. Staging area y git add

### ¿Qué es la staging area?

La staging area, o área de preparación, es el espacio intermedio de Git donde colocamos los cambios que queremos incluir en el próximo commit.

No todos los cambios que existen en nuestro proyecto tienen que formar parte necesariamente del próximo commit.

Git nos permite seleccionar qué cambios queremos registrar.

### El comando git add .

Utilizamos:

git add .

Este comando prepara los cambios para el próximo commit.

### ¿Qué significa el punto `.`?

El punto `.` indica el directorio actual.

Cuando utilizamos:

git add .

le estamos indicando a Git que incluya los cambios del directorio actual y sus subdirectorios.

En nuestro proyecto, al ejecutarlo desde:

inicio-de-cero

Git busca cambios dentro de `inicio-de-cero` y sus carpetas internas.

### Flujo

Archivo modificado
↓
Git detecta el cambio
↓
git add .
↓
Staging area
↓
git commit
↓
Historial de Git

### Conceptos importantes

- Staging area: área intermedia donde se preparan los cambios antes del commit.
- Staged: significa que un cambio está preparado para formar parte del próximo commit.
- Unstaged: significa que un cambio existe, pero todavía no está preparado para el próximo commit.
- Directorio actual: carpeta en la que estamos trabajando actualmente.
- Subdirectorio: carpeta que se encuentra dentro de otra carpeta.

---

## 8. ¿Qué es un commit?

### Concepto

Un commit es un registro de un conjunto de cambios dentro del historial de Git.

Podemos imaginarlo como una fotografía del estado del proyecto en un momento determinado.

### Importante

Un commit NO es lo mismo que guardar un archivo.

Guardar con:

⌘ + S

guarda el archivo físicamente en nuestro computador.

Utilizar:

git add .

prepara los cambios para el próximo commit.

Utilizar:

git commit

registra esos cambios en el historial de Git.

Utilizar:

git push

envía posteriormente esos commits al repositorio remoto en GitHub.

### Diferencia entre las acciones

Guardar archivo:
⌘ + S
↓
Guarda el archivo en el computador.

Preparar cambios:
git add .
↓
Coloca los cambios en la staging area.

Registrar cambios:
git commit
↓
Crea un registro en el historial local de Git.

Enviar cambios:
git push
↓
Envía los commits al repositorio remoto.

### Idea clave

Guardar, preparar, registrar y enviar son acciones diferentes.

El flujo completo que estamos aprendiendo es:

Archivo
↓
Guardar
↓
git add .
↓
Staging area
↓
git commit
↓
Historial local
↓
git push
↓
GitHub
---

## 9. git commit y el historial local

### ¿Qué es un commit?

Un commit es un registro de un conjunto de cambios dentro del historial de Git.

Podemos imaginarlo como una fotografía del estado del proyecto en un momento determinado.

### Comando utilizado

git commit -m "Documenta la preparacion del entorno y conceptos iniciales de Git"

### ¿Qué significa cada parte?

- git: ejecuta Git.
- commit: crea un registro en el historial.
- -m: indica que vamos a proporcionar un mensaje.
- "Documenta...": mensaje que describe los cambios registrados.

### Resultado obtenido

Nuestro commit fue creado correctamente:

[main e7f602b] Documenta la preparacion del entorno y conceptos iniciales de Git

El identificador corto del commit es:

e7f602b

### Concepto importante: identificador del commit

Cada commit recibe un identificador único.

Git utiliza este identificador para distinguir un commit de los demás registros del historial.

En nuestro caso, el identificador corto es:

e7f602b

---

## 10. Repositorio local y repositorio remoto

Después de crear el commit comprobamos el estado con:

git status

Obtuvimos:

Your branch is ahead of 'origin/main' by 1 commit.

### ¿Qué significa "ahead"?

Ahead significa que nuestro repositorio local está adelantado respecto al repositorio remoto.

En nuestro caso significa:

El repositorio local tiene 1 commit que todavía no ha sido enviado a GitHub.

### Situación actual

Mac:
1 commit nuevo
↓
GitHub:
todavía no tiene ese commit

Por lo tanto:

Repositorio local ≠ repositorio remoto

en este momento.

---

## 11. ¿Qué significa "working tree clean"?

También obtuvimos:

nothing to commit, working tree clean

Esto significa que actualmente no existen cambios pendientes en nuestros archivos de trabajo.

### Conceptos importantes

- Working tree: conjunto de archivos del proyecto sobre los que estamos trabajando actualmente.
- Clean: limpio, sin cambios pendientes.
- Ahead: adelantado respecto al repositorio remoto.

### Idea clave

Tener el working tree limpio NO significa necesariamente que GitHub esté actualizado.

En nuestro caso:

Working tree:
limpio.

Repositorio local:
contiene 1 commit nuevo.

GitHub:
todavía no contiene ese commit.

---

## 12. git push

### Concepto

git push es el comando utilizado para enviar nuestros commits desde el repositorio local hacia el repositorio remoto.

En nuestro proyecto, el repositorio remoto está en GitHub.

### Flujo

Archivo modificado
↓
Guardar con ⌘ + S
↓
git add .
↓
Staging area
↓
git commit
↓
Historial local
↓
git push
↓
Repositorio remoto en GitHub

### Importante

git commit y git push son operaciones diferentes.

git commit:

Registra los cambios en nuestro repositorio local.

git push:

Envía esos commits al repositorio remoto.

### Situación actual

Nuestro commit:

e7f602b

ya existe en el repositorio local.

Todavía debemos utilizar:

git push

para enviarlo a GitHub.

### Regla

Antes de ejecutar git push debemos entender que estamos enviando nuestros commits locales al repositorio remoto.

---
---

## 13. git push y sincronización con GitHub

### ¿Qué es git push?

`git push` es el comando que utilizamos para enviar los commits que existen en nuestro repositorio local hacia el repositorio remoto.

En nuestro proyecto, el repositorio remoto está alojado en GitHub.

Comando utilizado:

git push

### Resultado obtenido

El comando terminó correctamente y mostró:

main -> main

Esto significa que nuestra rama local `main` fue enviada correctamente hacia la rama `main` del repositorio remoto.

---

## 14. ¿Qué significa origin/main?

Anteriormente Git mostró:

Your branch is ahead of 'origin/main' by 1 commit.

Y después de utilizar `git push` mostró:

Your branch is up to date with 'origin/main'.

### origin

`origin` es el nombre que Git utiliza para identificar nuestro repositorio remoto principal.

### main

`main` es la rama principal que estamos utilizando.

Por lo tanto:

`origin/main`

significa:

La rama `main` del repositorio remoto identificado como `origin`.

---

## 15. ¿Qué significa "up to date"?

`up to date` significa que está actualizado.

Cuando Git muestra:

Your branch is up to date with 'origin/main'.

significa que nuestra rama local `main` y la rama remota `origin/main` están sincronizadas.

### Antes del push

Nuestro estado era:

Repositorio local:
2 commits nuevos

GitHub:
todavía no tenía esos commits

Por eso Git indicaba que nuestra rama estaba:

ahead

### Después del push

Nuestro estado pasó a ser:

Repositorio local:
2 commits

GitHub:
2 commits

Por lo tanto:

Local = Remoto

Y Git mostró:

up to date

---

## 16. ¿Qué significa "working tree clean"?

Después del `git push` ejecutamos:

git status

Y obtuvimos:

nothing to commit, working tree clean

### Significado

`working tree clean` significa que no existen cambios pendientes en los archivos que Git deba registrar.

No hay:

- archivos modificados sin preparar;
- archivos preparados sin commit;
- archivos nuevos sin seguimiento.

Nuestro proyecto está limpio.

### Importante

`working tree clean` y `up to date` son conceptos diferentes.

`working tree clean`:

Nuestro proyecto local no tiene cambios pendientes.

`up to date`:

Nuestro repositorio local está sincronizado con el repositorio remoto.

Podemos tener uno sin el otro.

---

## 17. Flujo completo que hemos aprendido

Hasta este momento hemos completado el ciclo básico de Git y GitHub:

Modificar archivo
↓
Guardar con ⌘ + S
↓
Git detecta el cambio
↓
git add .
↓
Staging area
↓
git commit
↓
Historial local
↓
git push
↓
Repositorio remoto en GitHub
↓
git status
↓
Comprobar sincronización

---

## 18. Diferencia entre las operaciones

### ⌘ + S

Guarda el archivo en nuestro computador.

### git status

Nos informa sobre el estado actual del repositorio.

### git add .

Prepara los cambios para el próximo commit.

El punto `.` representa el directorio actual y sus subdirectorios.

### git commit

Registra los cambios preparados en el historial local.

### git push

Envía los commits locales al repositorio remoto.

---

## 19. Conceptos importantes aprendidos

### Local

Algo que se encuentra en nuestro propio computador.

Português: `local`

### Remoto

Algo que se encuentra fuera de nuestro computador y al que accedemos mediante una red.

Português: `remoto`

### Sincronizado

Cuando dos versiones de información están actualizadas y coinciden respecto a los cambios registrados.

Português: `sincronizado`

### Ahead

Indica que nuestro repositorio local tiene commits que todavía no existen en el repositorio remoto.

Português: `à frente` / `adiantado`

### Up to date

Significa que está actualizado.

Português: `atualizado`

### Working tree

Representa los archivos actuales sobre los que estamos trabajando.

Português: `árvore de trabalho`

### Clean

Significa que no existen cambios pendientes.

Português: `limpo`

---

## 20. Punto de control

Hemos completado correctamente nuestro primer ciclo completo de Git y GitHub:

git add .
↓
git commit
↓
git push

Y comprobamos posteriormente:

git status

Resultado:

Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

Esto confirma que el repositorio local y el repositorio remoto están sincronizados.

---

## Idea clave

Git no es simplemente una herramienta para "guardar archivos".

Git permite controlar la evolución de un proyecto mediante un flujo:

cambios
↓
preparación
↓
registro
↓
sincronización

Cada etapa cumple una función diferente.

---

---

## 21. git log: consultar el historial

### ¿Qué es git log?

`git log` es el comando que utilizamos para consultar el historial de commits de un repositorio.

Comando utilizado:

git log

Git muestra los commits comenzando por el más reciente y avanzando hacia los más antiguos.

### Información que muestra git log

Cada commit puede mostrar:

- Identificador del commit.
- Autor.
- Fecha.
- Mensaje del commit.
- Referencias como `HEAD`, `main` y `origin/main`.

---

## 22. Identificador del commit

Cada commit tiene un identificador.

Ejemplo:

c021ff4d590e2263c289f2ac2096663d87d7537a

Git también permite utilizar una versión corta:

c021ff4

### Hash

El identificador completo de un commit es un hash generado por Git.

El hash permite identificar un commit específico dentro del historial.

En nuestro proyecto:

Hash corto:

c021ff4

Hash completo:

c021ff4d590e2263c289f2ac2096663d87d7537a

---

## 23. HEAD

`HEAD` es una referencia que indica la posición actual dentro del historial de Git.

En nuestro caso:

HEAD -> main

Esto significa que nuestra posición actual está en la rama `main`.

Podemos imaginarlo así:

HEAD
↓
main
↓
c021ff4
↓
5c4ce14
↓
e7f602b
↓
dfd0fb4

### Idea clave

HEAD indica dónde estamos actualmente dentro del historial.

---

## 24. Branch

Una `branch` es una rama del historial de un proyecto.

En nuestro proyecto utilizamos:

main

La rama permite desarrollar una línea de trabajo independiente dentro del historial.

Más adelante aprenderemos a crear y utilizar otras ramas.

Português:

branch = ramo / ramificação

---

## 25. origin

`origin` es el nombre que Git asigna normalmente al repositorio remoto principal.

En nuestro proyecto:

origin

representa el repositorio remoto de GitHub.

---

## 26. origin/main

`origin/main` representa la rama `main` del repositorio remoto identificado como `origin`.

Actualmente nuestro historial muestra:

(HEAD -> main, origin/main)

Esto significa que:

HEAD apunta a `main`.

`main` y `origin/main` apuntan actualmente al mismo commit.

Por lo tanto, nuestro repositorio local y el repositorio remoto están sincronizados.

---

## 27. Historial actual del proyecto

Nuestro historial contiene actualmente cuatro commits:

dfd0fb4
Primer commit

↓

e7f602b
Documenta la preparacion del entorno y conceptos iniciales de Git

↓

5c4ce14
Documenta commit y git push

↓

c021ff4
Actualiza estado del proyecto despues del primer ciclo Git

El commit más reciente es:

c021ff4

---

## 28. Control de versiones

Git es un sistema de control de versiones.

Esto significa que Git permite registrar la evolución de un proyecto a través del tiempo.

No solamente conserva el estado actual de los archivos.

También conserva los diferentes puntos registrados mediante commits.

### Idea clave

Proyecto
↓
Cambio
↓
Commit
↓
Nuevo estado
↓
Cambio
↓
Commit
↓
Nuevo estado

De esta manera podemos consultar cómo evolucionó el proyecto.

---

## 29. Conceptos aprendidos con git log

- `git log`: consulta el historial de commits.
- `commit`: registro de cambios.
- `hash`: identificador de un commit.
- `HEAD`: posición actual dentro del historial.
- `branch`: rama del historial.
- `main`: rama principal que estamos utilizando.
- `origin`: nombre del repositorio remoto.
- `origin/main`: rama `main` del repositorio remoto.
- `control de versiones`: sistema para registrar y consultar la evolución de un proyecto.

---

---

## 30. git log --oneline

### ¿Qué es git log --oneline?

`git log --oneline` es una versión resumida de `git log`.

Muestra cada commit en una sola línea, haciendo que el historial sea más fácil de leer.

Comando:

git log --oneline

Resultado obtenido en nuestro proyecto:

ddf8f32 (HEAD -> main, origin/main) Documenta historial y conceptos de Git
c021ff4 Actualiza estado del proyecto despues del primer ciclo Git
5c4ce14 Documenta commit y git push
e7f602b Documenta la preparacion del entorno y conceptos iniciales de Git
dfd0fb4 Primer commit

---

## 31. ¿Cómo leer una línea de git log --oneline?

Una línea normalmente tiene esta estructura:

HASH + MENSAJE DEL COMMIT

Por ejemplo:

ddf8f32 Documenta historial y conceptos de Git

### Hash

`ddf8f32` es el identificador corto del commit.

### Mensaje

`Documenta historial y conceptos de Git` es el mensaje que describe lo que registramos en ese commit.

Por lo tanto:

ddf8f32
↓
identificador del commit

Documenta historial y conceptos de Git
↓
mensaje del commit

---

## 32. Diferencia entre git log y git log --oneline

### git log

Muestra información detallada de cada commit.

Puede mostrar:

- hash completo;
- autor;
- fecha;
- mensaje;
- referencias.

### git log --oneline

Muestra una versión resumida:

- hash corto;
- mensaje del commit;
- referencias cuando corresponda.

### Idea clave

`git log`

= historial detallado

`git log --oneline`

= historial resumido

---

## 33. ¿Qué significa --oneline?

`--oneline` es una opción que modifica la forma en que Git muestra el historial.

Una opción es un parámetro adicional que cambia el comportamiento o la presentación de un comando.

En este caso:

`--oneline`

le indica a Git que muestre cada commit resumido en una sola línea.

Português:

opción = opção

---

## 34. Leer las referencias de un commit

En nuestro resultado aparece:

ddf8f32 (HEAD -> main, origin/main)

Esto contiene varias referencias.

### HEAD

Indica nuestra posición actual dentro del historial.

### main

Es la rama local en la que estamos trabajando.

### origin/main

Es la rama `main` del repositorio remoto identificado como `origin`.

Por lo tanto:

ddf8f32 (HEAD -> main, origin/main)

significa que:

- `HEAD` está en `main`.
- `main` está apuntando al commit `ddf8f32`.
- `origin/main` también está apuntando al commit `ddf8f32`.

Esto indica que nuestro repositorio local y el remoto están sincronizados en ese commit.

---

## 35. Historial resumido actual

Nuestro historial actual es:

ddf8f32
Documenta historial y conceptos de Git

↓

c021ff4
Actualiza estado del proyecto despues del primer ciclo Git

↓

5c4ce14
Documenta commit y git push

↓

e7f602b
Documenta la preparacion del entorno y conceptos iniciales de Git

↓

dfd0fb4
Primer commit

El commit que está arriba es el más reciente.

---

## 36. ¿Por qué es útil git log --oneline?

Cuando un proyecto tiene muchos commits, `git log` puede producir una gran cantidad de información.

`git log --oneline` permite obtener rápidamente una visión general del historial.

Por ejemplo:

git log --oneline

permite responder rápidamente:

- ¿Cuántos commits tengo?
- ¿Cuál es el último commit?
- ¿Cuál es su identificador?
- ¿Qué cambios registré anteriormente?
- ¿Cuál es el orden de los commits?

---

## 37. Conceptos aprendidos

### Historial

Conjunto de commits que representan la evolución de un proyecto.

Português:

historial = histórico

### Opción

Parámetro que modifica el comportamiento o la presentación de un comando.

Português:

opción = opção

### Resumen

Representación más corta de una información.

Português:

resumen = resumo

### Identificador

Valor que permite reconocer o distinguir algo.

Português:

identificador = identificador

### Referencia

Elemento que señala o apunta hacia otro elemento.

Português:

referencia = referência

---

## 38. Comandos aprendidos hasta este punto

### Consultar el estado

git status

### Preparar cambios

git add .

### Crear un commit

git commit -m "mensaje"

### Enviar commits a GitHub

git push

### Consultar historial detallado

git log

### Consultar historial resumido

git log --oneline

---

## Idea clave

Hasta este momento podemos pensar en Git como una secuencia:

Modificar
↓
Guardar
↓
Consultar estado
↓
Preparar
↓
Registrar
↓
Consultar historial
↓
Enviar a GitHub

Los comandos no hacen lo mismo.

Cada uno representa una etapa diferente del control de versiones.

---

---

## 39. Repositorio local y repositorio remoto

Para entender Git correctamente debemos diferenciar dos lugares donde existe nuestro proyecto.

## Repositorio local

El repositorio local es la copia del proyecto que existe en nuestra computadora.

En nuestro caso:

Mac
↓
Carpeta inicio-de-cero
↓
Git local

Aquí ocurren acciones como:

- modificar archivos;
- usar `git add`;
- crear commits con `git commit`;
- consultar el historial con `git log`.

Los commits creados con `git commit` existen inicialmente solamente en nuestro repositorio local.

---

## Repositorio remoto

El repositorio remoto es una copia del proyecto almacenada en un servidor externo.

En nuestro caso:

GitHub

El repositorio remoto permite:

- tener una copia de seguridad;
- trabajar desde diferentes dispositivos;
- compartir el proyecto;
- colaborar con otras personas.

---

## Diferencia entre commit y push

### git commit

`git commit` guarda los cambios en el historial del repositorio local.

Ejemplo:

Mac:

e5acded
↓
Commit creado localmente

Todavía no está en GitHub.

---

### git push

`git push` envía los commits del repositorio local hacia el repositorio remoto.

Ejemplo:

Mac
↓
git push
↓
GitHub

Después del push:

Repositorio local = repositorio remoto

---

## Flujo completo aprendido

Modificar archivo

↓

git add .

Prepara los cambios en la staging area.

↓

git commit

Crea un punto de guardado en el historial local.

↓

git push

Envía ese historial hacia GitHub.

---

## Conceptos importantes

### Repositorio local

Lugar donde Git guarda el historial del proyecto en nuestra computadora.

Português:

repositório local

### Repositorio remoto

Lugar externo donde se almacena una copia del repositorio, por ejemplo GitHub.

Português:

repositório remoto

### Sincronizar

Hacer que dos versiones tengan el mismo estado.

En nuestro caso:

Mac = GitHub

Português:

sincronizar = sincronizar

---