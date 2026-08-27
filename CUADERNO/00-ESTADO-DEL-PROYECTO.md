# Estado del Proyecto — Inicio de cero

## Objetivo general

Crear progresivamente un entorno de desarrollo para aprender:

- Programación.
- Python.
- Inteligencia artificial.
- Ingeniería de software.
- Redes y comunicación.
- Modelos de lenguaje (LLM).
- Automatización.
- Herramientas modernas de desarrollo.

El objetivo no es solamente instalar herramientas, sino comprender qué hacen, cómo funcionan y cómo utilizarlas para construir proyectos reales.

---

# Entorno actual

## Computador

- Mac con Apple Silicon.
- macOS.

## Herramientas confirmadas

- Git instalado y funcionando.
- Visual Studio Code instalado.
- Terminal funcionando.
- Repositorio Git local funcionando.
- Repositorio remoto conectado con GitHub.
- Conexión entre el repositorio local y GitHub funcionando.
- SSH configurado para el repositorio.
- Carpeta `CUADERNO` utilizada para documentar el aprendizaje.

---

# Estado actual del proyecto

## Git y GitHub

Se completó la etapa de fundamentos y se practicó un flujo básico de trabajo con Git.

Conceptos aprendidos:

- Repositorio.
- Repositorio local.
- Repositorio remoto.
- GitHub.
- `main`.
- `origin`.
- `origin/main`.
- `HEAD`.
- Commit.
- Hash o identificador del commit.
- Working tree.
- Working tree clean.
- Modified.
- Untracked.
- Staged.
- Unstaged.
- Staging area.
- Branch.
- `git switch`.
- `git merge`.
- Conflictos de merge.
- `git fetch`.
- `git pull`.
- `git push`.
- Estado `ahead`.
- Estado `behind`.
- Estado `up to date`.
- Fast-forward.

---

# Flujo básico aprendido

Cuando modificamos un archivo:

Modificar archivo

↓

`git status`

↓

`git add`

↓

Staging area

↓

`git commit -m "mensaje"`

↓

Historial local

↓

`git push`

↓

GitHub

↓

`git status`

↓

Comprobar sincronización

---

# Branches

Se creó una rama de prueba llamada:

`prueba-branches`

Se practicó:

`git branch prueba-branches`

para crear una rama.

Se practicó:

`git switch prueba-branches`

para cambiar de rama.

Se comprendió que una branch no es una carpeta nueva, sino una línea independiente dentro del historial de Git.

---

# Merge

Se practicó la integración de una rama mediante:

`git merge prueba-branches`

La operación se realizó estando en `main`, por lo que los cambios de `prueba-branches` fueron integrados en `main`.

Durante esta práctica apareció un conflicto en:

`CUADERNO/01-Git-y-GitHub.md`

El conflicto fue revisado y resuelto manualmente.

Después se utilizó:

`git add CUADERNO/01-Git-y-GitHub.md`

y posteriormente un commit para concluir el merge.

La rama de prueba fue eliminada después de completar la integración:

`git branch -d prueba-branches`

---

# Conflictos

Se aprendió que un conflicto no significa necesariamente que Git esté dañado.

Un conflicto aparece cuando Git encuentra cambios que no puede combinar automáticamente.

El proceso aprendido fue:

Detectar conflicto

↓

Revisar el archivo

↓

Decidir qué contenido debe conservarse

↓

Eliminar las marcas de conflicto

↓

`git add`

↓

`git commit`

---

# Fetch y Pull

También se practicó el trabajo entre el repositorio local y el remoto.

## git fetch

`git fetch`

actualiza la información que el repositorio local tiene sobre el repositorio remoto.

No mueve automáticamente nuestra rama `main`.

Durante la práctica se comprobó que `origin/main` podía avanzar mientras `main` local permanecía en un commit anterior.

## git pull

`git pull`

trae los cambios del repositorio remoto y actualiza la rama local.

Durante la práctica:

`main`

estaba un commit detrás de:

`origin/main`.

Después de ejecutar `git pull`, la rama local avanzó mediante un `fast-forward`.

---

# Diferencia entre main y origin/main

## main

Es nuestra rama `main` local.

## origin/main

Es la referencia local que Git mantiene sobre la rama `main` del repositorio remoto.

`origin` representa el repositorio remoto configurado para nuestro proyecto.

Por lo tanto:

`main` = rama local.

`origin/main` = referencia de la rama `main` remota.

---

# Estado confirmado

Último estado comprobado:

`git status`

Resultado:

`On branch main`

`Your branch is up to date with 'origin/main'.`

`nothing to commit, working tree clean`

Esto confirma que, en el momento de la última comprobación:

- Estamos en `main`.
- `main` está sincronizada con `origin/main`.
- No existen cambios pendientes en el working tree.

Último commit confirmado:

`a012735`

Mensaje:

`Update 01-Git-y-GitHub.md`

---

# Documentación de Git

El documento:

`CUADERNO/01-Git-y-GitHub.md`

contiene el aprendizaje realizado sobre Git y GitHub.

Durante el aprendizaje se documentaron conceptos, comandos, pruebas con branches, merge, conflictos, `fetch` y `pull`.

---

# Método de trabajo aprendido

A partir de ahora no debemos ejecutar comandos de Git automáticamente sin comprobar primero el estado.

Regla:

**NO ASUMIR → COMPROBAR → ACTUAR → VERIFICAR**

En Git, el comando principal para conocer el estado actual es:

`git status`

---

# Próximo paso

La etapa de fundamentos de Git y GitHub ya está suficientemente desarrollada para continuar.

El siguiente objetivo será comenzar con **SSH**, pero antes de avanzar se debe comprobar el estado real del repositorio y verificar que la documentación esté sincronizada con GitHub.

Después comenzaremos la etapa:

**SSH → VS Code → entorno de desarrollo → Python → herramientas de IA → LLM locales → automatización**

---

# Regla de continuidad

Cuando retomemos el proyecto:

1. Leer `CUADERNO/00-ESTADO-DEL-PROYECTO.md`.
2. Leer `CUADERNO/00-CONTEXTO-PARA-LLM.md` cuando sea necesario.
3. Ejecutar `git status`.
4. Comparar el estado real con este documento.
5. No asumir que el estado documentado sigue siendo actual.
6. Continuar únicamente desde el último punto confirmado.

---

# Principio del proyecto

El objetivo no es únicamente terminar instalaciones.

Cada etapa debe seguir el ciclo:

**CONSTRUIR → COMPROBAR → INVESTIGAR → COMPARAR → COMPRENDER → DOCUMENTAR → MEJORAR → CONTINUAR**