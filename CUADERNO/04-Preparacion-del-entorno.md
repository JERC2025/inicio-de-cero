# Preparación del entorno

## 1. Objetivo

El objetivo de esta etapa es preparar nuestro Mac para convertirlo en un entorno de aprendizaje y desarrollo enfocado en:

- Inteligencia artificial.
- Programación.
- Ingeniería de software.
- Redes y comunicación.
- Modelos de lenguaje (LLM).
- Automatización.
- Herramientas de desarrollo.

La preparación del entorno es la base sobre la cual posteriormente construiremos nuestro entorno para trabajar con LLM locales y OpenClaw.

---

# 2. Preparación inicial

Partimos de un Mac con Apple Silicon.

Durante la preparación inicial decidimos trabajar principalmente con:

- macOS.
- Terminal.
- Visual Studio Code.
- Git.
- GitHub.
- ChatGPT.

También establecimos que las herramientas deben instalarse y comprobarse paso a paso, entendiendo para qué sirve cada una.

---

# 3. Instalación de ChatGPT

## Objetivo

Tener ChatGPT instalado como aplicación en el Mac para poder utilizarlo directamente desde el computador.

## Proceso realizado

1. Entramos en la página oficial de ChatGPT.
2. Seleccionamos la descarga correspondiente a Apple Silicon.
3. Se descargó el instalador.
4. Abrimos el instalador.
5. El sistema mostró la opción de instalar la aplicación.
6. Completamos la instalación.
7. Iniciamos sesión.
8. La aplicación quedó funcionando correctamente en el Mac.

## Concepto importante: Apple Silicon

Apple Silicon es la familia de procesadores desarrollados por Apple para sus computadores Mac.

Nuestro Mac utiliza arquitectura Apple Silicon.

Por eso, cuando una aplicación ofrece versiones diferentes para Mac, debemos comprobar si corresponde a:

- Apple Silicon.
- Intel.

No debemos elegir una versión al azar.

## Idea clave

Antes de instalar una aplicación debemos comprobar que estamos descargando la versión compatible con nuestro computador.

---

# 4. Visual Studio Code

## Objetivo

Utilizar Visual Studio Code como nuestro principal editor de código y documentos relacionados con el proyecto.

## Concepto

Visual Studio Code, también conocido como VS Code, es un editor de código fuente.

Un editor de código es un programa que permite escribir y modificar archivos utilizados en proyectos de programación y desarrollo.

## Uso dentro de nuestro proyecto

Estamos utilizando VS Code para trabajar con:

- Archivos Markdown.
- Archivos de configuración.
- Código.
- Documentación.
- Nuestro cuaderno de aprendizaje.

Nuestro proyecto se encuentra en:

inicio-de-cero

Dentro del proyecto creamos:

CUADERNO/

---

# 5. Terminal

## Concepto

La Terminal es una aplicación que permite interactuar con el sistema operativo mediante comandos escritos.

En lugar de utilizar únicamente ventanas y botones, podemos escribir instrucciones para que el sistema realice determinadas acciones.

## Concepto importante: comando

Un comando es una instrucción escrita que le indica a un programa o al sistema qué acción debe realizar.

Por ejemplo:

git --version

es un comando que solicita a Git que muestre su versión.

## Diferencia entre VS Code y Terminal

VS Code:

Nos permite editar archivos y trabajar con el contenido del proyecto.

Terminal:

Nos permite ejecutar comandos y comunicarnos directamente con herramientas del sistema.

Ambas herramientas trabajan juntas, pero cumplen funciones diferentes.

---

# 6. Nuestro proyecto

Creamos y utilizamos el proyecto:

inicio-de-cero

La ubicación local comprobada del proyecto es:

/Users/jhonedisonramosceceres/inicio-de-cero

Para entrar al proyecto desde la Terminal utilizamos:

cd ~/inicio-de-cero

Después comprobamos nuestra ubicación con:

pwd

El resultado obtenido fue:

/Users/jhonedisonramosceceres/inicio-de-cero

## Conceptos importantes

### Directorio

Un directorio es una carpeta dentro del sistema de archivos.

### Directorio actual

Es la carpeta en la que la Terminal está trabajando en ese momento.

### Subdirectorio

Es una carpeta que se encuentra dentro de otra carpeta.

En nuestro proyecto:

inicio-de-cero

es el directorio principal.

CUADERNO

es un subdirectorio de inicio-de-cero.

---

# 7. Git

## Objetivo

Utilizar Git para controlar las versiones de nuestro proyecto.

## Comprobación de instalación

Utilizamos:

git --version

El resultado obtenido fue:

git version 2.50.1 (Apple Git-155)

Esto confirmó que Git está instalado y disponible desde la Terminal.

## Concepto

Git es un sistema de control de versiones.

Un sistema de control de versiones permite registrar los cambios realizados en un proyecto y mantener un historial de esos cambios.

---

# 8. Configuración de Git

Configuramos la identidad que Git utilizará para identificar nuestros cambios.

Configuramos:

- user.name
- user.email

Para comprobar la configuración utilizamos:

git config --global --list

## Concepto importante: configuración global

La opción:

--global

indica que la configuración se aplica de forma general al usuario de Git en este computador.

No significa que la configuración pertenezca exclusivamente a un proyecto.

---

# 9. GitHub

## Concepto

GitHub es una plataforma que permite almacenar, compartir y colaborar utilizando repositorios Git.

Nuestro proyecto está relacionado con el repositorio:

JERC2025/inicio-de-cero

## Conceptos importantes

### Repositorio local

Es la copia del proyecto que tenemos almacenada en nuestro computador.

### Repositorio remoto

Es la copia del proyecto almacenada en un servidor remoto, en nuestro caso GitHub.

### Origin

origin es el nombre que Git utiliza normalmente para identificar el repositorio remoto principal.

---

# 10. Creación del CUADERNO

Dentro del proyecto creamos:

CUADERNO/

La finalidad del cuaderno es documentar nuestro proceso de aprendizaje.

No queremos guardar únicamente comandos.

Queremos registrar:

- Qué es cada herramienta.
- Para qué sirve.
- Qué significa cada comando.
- Qué conceptos debemos aprender.
- Qué errores encontramos.
- Cómo solucionamos los errores.
- Qué comprobamos.
- Qué debemos aprender después.

## Documentos creados

Actualmente tenemos:

- 00-ESTADO-DEL-PROYECTO.md
- 01-Git-y-GitHub.md
- 02-SSH.md
- 03-VS-Code.md
- 04-Preparacion-del-entorno.md

---

# 11. Problemas encontrados durante la preparación

## Problema de copiar y pegar

Durante el proceso encontramos problemas al copiar contenido desde el iPhone hacia VS Code.

En algunos momentos se copiaba también información que pertenecía a la Terminal, incluyendo elementos como:

usuario@Mac carpeta %

Esto provocaba errores como:

zsh: command not found

## ¿Qué significa "command not found"?

Significa:

"comando no encontrado".

La Terminal intentó interpretar como un comando algo que realmente no era un comando válido.

## ¿Por qué ocurrió?

La información que aparecía en la Terminal se estaba copiando junto con el comando.

Por ejemplo, esto:

usuario@Mac inicio-de-cero % pwd

no debe copiarse completo.

Lo que debemos escribir es solamente:

pwd

## Concepto importante: prompt

El prompt es la parte que aparece en la Terminal indicando que el sistema está listo para recibir un comando.

Por ejemplo:

usuario@Mac inicio-de-cero %

No debemos copiar el prompt como si fuera parte del comando.

---

# 12. Problemas con el guardado

También comprobamos que:

⌘ + S

guarda los cambios realizados en VS Code.

Aprendimos que guardar un archivo en VS Code y registrar un cambio mediante Git son operaciones diferentes.

## Diferencia importante

Guardar con:

⌘ + S

guarda el archivo en nuestro computador.

Git posteriormente puede detectar que ese archivo fue modificado.

Por lo tanto:

Guardar archivo ≠ hacer commit.

---

# 13. Estado comprobado al finalizar esta etapa

Hasta este punto hemos comprobado:

✅ ChatGPT está instalado y funcionando en el Mac.

✅ Visual Studio Code está instalado y funcionando.

✅ Terminal está disponible.

✅ Git está instalado.

✅ Git devuelve la versión:

git version 2.50.1 (Apple Git-155)

✅ Git tiene configurada nuestra identidad.

✅ Existe el proyecto:

inicio-de-cero

✅ Podemos entrar al proyecto desde Terminal.

✅ Existe la carpeta:

CUADERNO/

✅ Existe el repositorio remoto asociado a GitHub.

---

# 14. Información pendiente de comprobar

No debemos asumir que una herramienta está correctamente instalada solamente porque estaba prevista para instalarla.

Por eso todavía debemos comprobar explícitamente:

- Python.
- Versión de Python.
- Herramientas relacionadas con Python.
- Otros componentes necesarios para nuestro futuro entorno de LLM local.

## Regla del proyecto

No documentaremos como "instalado y funcionando" algo que todavía no hayamos comprobado.

---

# 15. Método de aprendizaje establecido

A partir de este momento, cada etapa debe explicar:

1. Qué vamos a hacer.
2. Dónde debemos hacerlo.
3. Qué comando o acción debemos realizar.
4. Qué significa el comando o concepto.
5. Qué resultado esperamos.
6. Qué resultado obtuvimos.
7. Qué errores pueden ocurrir.
8. Cómo solucionarlos.
9. Qué debemos recordar.
10. Qué queda pendiente.

El objetivo no es solamente completar la instalación.

El objetivo es comprender el entorno que estamos construyendo.

---

# 16. Punto de continuación

Después de documentar la preparación inicial del entorno, debemos continuar con:

01-Git-y-GitHub.md

El último concepto práctico alcanzado fue:

git status

Después aprendimos que:

git add .

prepara los cambios para el próximo commit.

El siguiente concepto que debemos estudiar es:

staging area

y posteriormente:

git commit

No debemos saltarnos estos conceptos.

---

# Regla fundamental

Antes de ejecutar un comando debemos saber:

¿Qué hace?

¿Por qué lo estamos ejecutando?

¿Qué resultado esperamos?

Y después debemos comprobar qué ocurrió.

Esto forma parte de nuestro método de aprendizaje.