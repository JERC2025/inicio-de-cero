# Contexto del proyecto para LLM

## INSTRUCCIONES PRINCIPALES

Este documento contiene el contexto necesario para que un LLM pueda continuar el proyecto "Inicio de cero".

El LLM que utilice este documento debe tratarlo como contexto de trabajo y respetar las siguientes reglas:

1. No asumir que una herramienta está instalada. Comprobarla antes.
2. No asumir que una configuración existe. Comprobarla antes.
3. No saltarse pasos importantes.
4. Explicar qué se está haciendo antes de pedir ejecutar un comando.
5. Indicar claramente dónde debe realizarse cada acción:
   - Terminal.
   - Visual Studio Code.
   - Navegador.
6. Explicar los conceptos importantes asociados a cada paso.
7. Explicar los comandos y, cuando sea útil, explicar cada parte del comando.
8. Después de ejecutar una acción, comprobar el resultado antes de continuar.
9. Si aparece un error, detenerse y entenderlo antes de continuar.
10. No inventar información sobre el estado del proyecto.
11. Diferenciar entre:
    - lo que está comprobado;
    - lo que está pendiente de comprobar;
    - lo que todavía no se ha realizado.
12. Mantener el aprendizaje progresivo.
13. No avanzar simplemente para completar instalaciones.
14. El objetivo es que el estudiante comprenda el entorno y pueda utilizarlo por sí mismo.

---

# 1. Nombre del proyecto

Inicio de cero

---

# 2. Objetivo general

Construir progresivamente un entorno de aprendizaje y desarrollo en un Mac con Apple Silicon.

El proyecto está orientado principalmente a:

- Inteligencia artificial.
- Programación.
- Ingeniería de software.
- Redes y comunicación.
- Modelos de lenguaje (LLM).
- Automatización.
- Herramientas modernas de desarrollo.

El objetivo final incluye trabajar con LLM locales y explorar OpenClaw, pero estos componentes no deben instalarse prematuramente.

Primero deben construirse y comprenderse las bases necesarias.

---

# 3. Filosofía del proyecto

El proyecto no consiste únicamente en instalar programas.

La prioridad es comprender:

- qué es cada herramienta;
- para qué sirve;
- cómo se relaciona con las demás;
- cómo configurarla;
- cómo comprobar que funciona;
- cómo solucionar errores;
- cómo mantener el entorno.

Cada instalación debe convertirse también en aprendizaje.

---

# 4. Entorno actual

## Hardware

Mac con Apple Silicon.

## Sistema operativo

macOS.

## Herramientas confirmadas

### ChatGPT

La aplicación de ChatGPT está instalada y funcionando en el Mac.

### Visual Studio Code

Visual Studio Code está instalado y funcionando.

Se utiliza como editor principal del proyecto.

### Terminal

La Terminal está disponible y se utiliza para ejecutar comandos.

### Git

Git está instalado.

Versión comprobada:

git version 2.50.1 (Apple Git-155)

### GitHub

Existe un repositorio remoto asociado al proyecto.

Repositorio:

JERC2025/inicio-de-cero

---

# 5. Ubicación del proyecto

El proyecto local se encuentra en:

/Users/jhonedisonramosceceres/inicio-de-cero

Para entrar desde Terminal:

cd ~/inicio-de-cero

Para comprobar la ubicación:

pwd

Resultado esperado:

/Users/jhonedisonramosceceres/inicio-de-cero

---

# 6. Estructura actual del proyecto

Dentro de inicio-de-cero existe:

CUADERNO/

Dentro de CUADERNO tenemos:

- 00-ESTADO-DEL-PROYECTO.md
- 00-CONTEXTO-PARA-LLM.md
- 01-Git-y-GitHub.md
- 02-SSH.md
- 03-VS-Code.md
- 04-Preparacion-del-entorno.md

---

# 7. Función de cada documento

## 00-ESTADO-DEL-PROYECTO.md

Contiene el estado actual del proyecto.

Debe responder:

- ¿Dónde estamos?
- ¿Qué hemos completado?
- ¿Qué estamos haciendo?
- ¿Qué falta?
- ¿Cuál es el siguiente paso?

Debe actualizarse cuando lleguemos a puntos importantes.

---

## 00-CONTEXTO-PARA-LLM.md

Este documento permite transferir el contexto del proyecto a otro LLM.

Debe mantenerse actualizado cuando cambien significativamente:

- los objetivos;
- las herramientas;
- la arquitectura;
- el método de trabajo;
- el estado del proyecto.

---

## 01-Git-y-GitHub.md

Contiene el aprendizaje progresivo de Git y GitHub.

Hasta ahora se han documentado los conceptos iniciales.

El siguiente aprendizaje práctico es continuar con:

- git add
- staging area
- git commit
- git log
- git push
- git pull

---

## 02-SSH.md

Documento reservado para aprender SSH.

Todavía no debemos asumir que SSH está configurado.

---

## 03-VS-Code.md

Documento reservado para aprender y documentar Visual Studio Code.

---

## 04-Preparacion-del-entorno.md

Documenta el proceso inicial de preparación del entorno.

Incluye:

- ChatGPT;
- Visual Studio Code;
- Terminal;
- Git;
- GitHub;
- creación del proyecto;
- creación del cuaderno;
- problemas encontrados;
- método de aprendizaje.

---

# 8. Conceptos de Git ya aprendidos

Hasta este momento se han introducido:

## Git

Sistema de control de versiones.

## GitHub

Plataforma para almacenar y compartir repositorios Git.

## Repositorio

Carpeta de un proyecto administrada por Git.

## Repositorio local

Copia del proyecto almacenada en el computador.

## Repositorio remoto

Copia del proyecto almacenada en un servidor remoto.

## Commit

Registro de cambios dentro del historial de Git.

## Branch

Rama independiente de trabajo.

La rama actual es:

main

## Origin

Nombre utilizado normalmente para identificar el repositorio remoto principal.

## Modified

Indica que un archivo conocido por Git fue modificado.

## Untracked

Indica que un archivo o carpeta existe dentro del proyecto pero Git todavía no lo está siguiendo.

---

# 9. Comandos de Git ya utilizados

## Comprobar versión

git --version

## Consultar configuración

git config --global --list

## Entrar al proyecto

cd ~/inicio-de-cero

## Comprobar ubicación

pwd

## Comprobar estado

git status

## Preparar cambios

git add .

Este último comando ya fue ejecutado y comprobado.

---

# 10. Concepto pendiente: staging area

Todavía debemos profundizar en el concepto de:

staging area

La staging area es el área donde Git coloca los cambios que han sido seleccionados para formar parte del próximo commit.

Debe explicarse antes de continuar con git commit.

---

# 11. Flujo de Git que debemos aprender

Debemos comprender progresivamente este flujo:

Archivo modificado
↓
Git detecta el cambio
↓
git add
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

No se debe asumir que el estudiante ya comprende completamente este flujo.

Debe explicarse paso a paso.

---

# 12. Diferencias importantes

## Guardar archivo

En VS Code:

⌘ + S

Esto guarda físicamente el archivo en el computador.

## git add

Prepara cambios para el próximo commit.

## git commit

Registra los cambios preparados dentro del historial de Git.

## git push

Envía commits desde el repositorio local hacia el repositorio remoto.

Estas cuatro acciones no son equivalentes.

---

# 13. Problemas importantes que ya ocurrieron

## Problema 1: copiar el prompt de Terminal

En algunos momentos se copió accidentalmente información como:

usuario@Mac inicio-de-cero %

junto con los comandos.

Esto produjo errores:

zsh: command not found

### Lección

El prompt no forma parte del comando.

Debemos escribir solamente el comando.

---

## Problema 2: confusión entre Terminal y VS Code

Algunos contenidos estaban destinados a VS Code y otros a Terminal.

A partir de ahora toda instrucción debe indicar claramente dónde debe realizarse.

---

## Problema 3: copiar y pegar desde iPhone

El usuario estaba utilizando ChatGPT principalmente desde el iPhone y utilizaba la duplicación del iPhone en el Mac para copiar información.

Esto produjo problemas de copia y pegado.

Posteriormente se instaló ChatGPT directamente en el Mac para facilitar el trabajo.

---

# 14. Método de enseñanza requerido

Para cada nuevo paso utilizar esta estructura:

## Objetivo

Explicar qué vamos a conseguir.

## Ubicación

Indicar claramente:

Terminal / VS Code / navegador.

## Acción

Indicar exactamente qué debe hacer el estudiante.

## Concepto

Explicar qué significa lo que estamos utilizando.

## Resultado esperado

Explicar qué debería aparecer.

## Comprobación

Verificar que realmente funcionó.

## Errores

Explicar posibles errores y su significado.

## Idea clave

Resumir qué debe recordar el estudiante.

---

# 15. Regla sobre los bloques de contenido

Cuando sea necesario introducir contenido en un archivo:

- entregar un único bloque completo;
- indicar claramente el archivo de destino;
- evitar dividir el contenido en múltiples bloques innecesarios;
- incluir dentro del mismo bloque las explicaciones y conceptos importantes;
- no obligar al estudiante a reconstruir manualmente el contenido.

Cuando sea necesario ejecutar comandos:

- indicar claramente que son comandos;
- indicar que deben ejecutarse en Terminal;
- no incluir accidentalmente el prompt dentro del comando.

---

# 16. Regla sobre documentación

El cuaderno debe funcionar como material de estudio.

No debe ser únicamente una lista de comandos.

Cada concepto importante debe quedar documentado.

Ejemplo:

No escribir solamente:

git add .

También explicar:

El comando git add . prepara los cambios para el próximo commit.

El punto . indica el directorio actual y sus subdirectorios.

---

# 17. Estado actual

## Completado

- ChatGPT instalado.
- Visual Studio Code instalado.
- Terminal disponible.
- Git instalado.
- Git configurado.
- GitHub conectado al proyecto.
- Proyecto inicio-de-cero creado.
- CUADERNO creado.
- Documentación inicial creada.
- git status ejecutado.
- git add . ejecutado.

## Pendiente

- Comprender completamente staging area.
- Realizar el primer commit de esta etapa.
- Comprender git log.
- Comprender git push.
- Comprender git pull.
- Completar Git y GitHub.
- Aprender SSH.
- Completar documentación de VS Code.
- Comprobar Python.
- Preparar el entorno de desarrollo.
- Evaluar e instalar un LLM local adecuado.
- Comprender los requisitos para trabajar con LLM locales.
- Explorar OpenClaw.
- Construir progresivamente el entorno final.

---

# 18. Próximo paso

El próximo paso debe ser:

Volver a 01-Git-y-GitHub.md.

Continuar desde:

git add .

y explicar:

1. Qué es staging area.
2. Qué significa que los archivos estén staged.
3. Cómo comprobarlo con git status.
4. Qué es un commit.
5. Por qué todavía no debemos hacer commit sin entenderlo.

No saltar directamente a instalaciones de LLM u OpenClaw.

Primero completar las bases.

---

# 19. Regla de continuidad para cualquier LLM

Si otro LLM recibe este documento, debe:

1. Leer todo el contexto antes de actuar.
2. Consultar 00-ESTADO-DEL-PROYECTO.md.
3. Determinar el último paso confirmado.
4. No asumir que los pasos pendientes fueron realizados.
5. Comprobar el estado actual cuando sea necesario.
6. Continuar desde el último punto confirmado.
7. Mantener el método de enseñanza descrito en este documento.
8. Actualizar la documentación cuando se complete una etapa importante.

## Regla fundamental

No continuar simplemente porque "parece lógico".

Primero comprobar.

No asumir.

Explicar.

Comprobar.

Documentar.

Continuar.