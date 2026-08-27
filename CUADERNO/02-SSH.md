# SSH — Secure Shell

## Objetivo

Comprender qué es SSH, para qué lo utilizamos en nuestro proyecto y cómo permite que Git se autentique de forma segura frente a GitHub.

El objetivo no es solamente configurar SSH, sino comprender qué función cumple cada elemento.

---

# ¿Qué es SSH?

SSH es un protocolo de seguridad que permite autenticar nuestra computadora frente a un servidor mediante una comunicación segura.

En nuestro proyecto utilizamos SSH para que Git pueda comunicarse con GitHub de forma autenticada.

Es importante distinguir las funciones:

- Git administra los cambios y el historial del proyecto.
- SSH proporciona la autenticación segura durante la comunicación.
- GitHub almacena el repositorio remoto.

Flujo:

Mac
↓
Git
↓
SSH
↓
GitHub

---

# Claves SSH

SSH utiliza un par de claves relacionadas:

- clave privada;
- clave pública.

Estas claves trabajan juntas para permitir la autenticación.

---

## Clave privada

Archivo:

id_ed25519

Ubicación:

~/.ssh/id_ed25519

La clave privada permanece en nuestra computadora.

Regla de seguridad:

NO compartir la clave privada.

No debemos enviarla a otras personas ni subirla a GitHub.

La clave privada permite que nuestra computadora demuestre que posee la identidad SSH correspondiente.

---

## Clave pública

Archivo:

id_ed25519.pub

Ubicación:

~/.ssh/id_ed25519.pub

La clave pública puede registrarse en GitHub.

GitHub utiliza la clave pública para verificar la identidad asociada con nuestra clave privada.

Por eso:

id_ed25519
→ clave privada
→ permanece en nuestra Mac

id_ed25519.pub
→ clave pública
→ puede registrarse en GitHub

---

# known_hosts

Archivo:

~/.ssh/known_hosts

Este archivo no es una clave privada ni una clave pública.

Contiene información sobre servidores SSH conocidos.

En nuestro caso está relacionado con el reconocimiento del servidor de GitHub por parte de nuestra computadora.

Podemos entenderlo como un registro de servidores conocidos.

---

# Relación entre Git, SSH y GitHub

Git y SSH cumplen funciones diferentes.

Git:

- administra el repositorio;
- registra cambios;
- crea commits;
- envía y recibe información del repositorio remoto.

SSH:

- proporciona autenticación segura;
- permite que Git se comunique con GitHub utilizando nuestra configuración SSH.

GitHub:

- almacena nuestro repositorio remoto;
- conserva los commits enviados;
- puede reconocer nuestra identidad SSH mediante la clave pública registrada.

---

# git push y SSH

Cuando ejecutamos:

git push

Git intenta enviar los commits locales hacia GitHub.

Como nuestro repositorio utiliza una dirección SSH, Git utiliza SSH durante esta comunicación.

Flujo:

git push
↓
Git
↓
SSH
↓
Autenticación
↓
GitHub
↓
Los commits son enviados al repositorio remoto

---

# Configuración SSH del repositorio

Comprobamos la configuración del repositorio con:

git remote -v

Resultado confirmado:

origin git@github.com:JERC2025/inicio-de-cero.git (fetch)

origin git@github.com:JERC2025/inicio-de-cero.git (push)

Esto confirma que el repositorio utiliza una dirección SSH para las operaciones de fetch y push.

---

# Comprobación de autenticación

Comprobamos la autenticación SSH con:

ssh -T git@github.com

GitHub respondió:

Hi JERC2025! You've successfully authenticated, but GitHub does not provide shell access.

Esto confirma que GitHub reconoce correctamente nuestra autenticación mediante SSH.

La frase:

You've successfully authenticated

significa que la autenticación fue exitosa.

---

# Seguridad

Reglas fundamentales:

- No compartir la clave privada.
- No subir la clave privada a GitHub.
- No enviar la clave privada por mensajes.
- La clave pública sí puede registrarse en GitHub.
- Una computadora nueva puede utilizar una nueva pareja de claves SSH.
- No es necesario copiar la clave privada de una computadora antigua a una nueva.

---

# GitHub y diferentes dispositivos

SSH no identifica nuestra cuenta de GitHub como si fuera exclusivamente una computadora.

SSH autentica una computadora mediante una clave SSH.

Por eso podemos utilizar GitHub desde diferentes dispositivos.

Por ejemplo:

Mac
↓
Git + SSH
↓
GitHub

Celular
↓
GitHub
↓
Misma cuenta y repositorios

El repositorio remoto permanece en GitHub aunque nuestra computadora se pierda o deje de funcionar.

---

# Recuperación en una computadora nueva

Si perdemos nuestra Mac y también perdemos la clave privada que estaba almacenada en ella:

- el repositorio de GitHub no desaparece;
- los commits enviados a GitHub permanecen;
- podemos utilizar otra computadora;
- podemos generar una nueva pareja de claves SSH;
- podemos registrar la nueva clave pública en GitHub;
- posteriormente podemos volver a trabajar con el repositorio.

No necesitamos conocer ni memorizar la clave privada anterior.

---

# Conceptos aprendidos

Hasta este punto comprendemos:

- SSH.
- Protocolo.
- Autenticación.
- Clave privada.
- Clave pública.
- id_ed25519.
- id_ed25519.pub.
- known_hosts.
- Git.
- GitHub.
- Repositorio local.
- Repositorio remoto.
- git push.
- git fetch.
- git pull.
- git remote -v.

---

# Comandos utilizados

Comprobar autenticación SSH:

ssh -T git@github.com

Consultar el repositorio remoto:

git remote -v

Consultar información de Git:

git status

Enviar commits:

git push

Consultar información del repositorio remoto:

git fetch

Actualizar el repositorio local:

git pull

---

# Idea clave

Git administra los cambios y los repositorios.

SSH proporciona autenticación segura durante la comunicación.

GitHub almacena el repositorio remoto.

Las claves SSH permiten autenticar nuestra computadora:

id_ed25519
→ clave privada
→ NO compartir

id_ed25519.pub
→ clave pública
→ puede registrarse en GitHub

known_hosts
→ registro de servidores SSH conocidos

---

# Estado de SSH en nuestro proyecto

Estado confirmado:

- SSH funciona correctamente.
- GitHub reconoce nuestra autenticación.
- Existe una clave privada Ed25519.
- Existe una clave pública Ed25519.
- Existe el archivo known_hosts.
- El repositorio utiliza una URL SSH.
- git push funciona mediante esta configuración.

No es necesario modificar la configuración SSH actual.

---

# Próximo paso

Después de documentar SSH, continuaremos con la siguiente etapa del proyecto según el estado general documentado en:

CUADERNO/00-ESTADO-DEL-PROYECTO.md

Antes de avanzar comprobaremos nuevamente el estado real del repositorio.