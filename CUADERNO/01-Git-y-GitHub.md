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