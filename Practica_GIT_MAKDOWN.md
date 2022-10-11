# **Git (Software de Control de versiones)**

## **- Índice**
### 1. Concepto 
### 2. Historia
### 3. Caracteristicas
### 4. ¿Qué es un sistema de control de versiones?
### 5. Introducción a los Comandos de GIT
### 6. Comandos: Configuración Inicial
### 7. Comandos: Manejo de Archivos y cambios
### 8. Comandos: Manejo de Repositorios Remotos
<br>
<hr>

## **- Contenidos**

<br>

### **1. Concepto**
<div style="text-align: justify"> 
Git es un sistema de control de versiones distribuido, está pensando en la eficiencia y la confiabilidad del mantenimiento de versiones de aplicaciones cuando estas tienen un gran número de archivos de código fuente.

<br>

-Git está optimizado para guardar cambios de forma incremental.

-Permite contar con un historial, regresar a una versión anterior y agregar funcionalidades.

-Lleva un registro de los cambios que otras personas realicen en los archivos.

Git fue diseñado para operar en un entorno Linux. Actualmente, es multiplataforma, es decir, es compatible con Linux, MacOS y Windows. En la máquina local se encuentra Git, se utiliza bajo la terminal o línea de comandos y tiene comandos como merge, pull, add, commit y rebase, entre otros.
</div>

<br>

### **2. Historia de GIT**
<div style="text-align: justify"> 
Como muchas de las grandes cosas en esta vida, Git comenzó con un poco de destrucción creativa y una gran polémica.

<br>

El kernel de Linux es un proyecto de software de código abierto con un alcance bastante amplio. Durante la mayor parte del mantenimiento del kernel de Linux (1991-2002), los cambios en el software se realizaban a través de parches y archivos. En el 2002, el proyecto del kernel de Linux empezó a usar un DVCS propietario llamado BitKeeper.

En el 2005, la relación entre la comunidad que desarrollaba el kernel de Linux y la compañía que desarrollaba BitKeeper se vino abajo y la herramienta dejó de ser ofrecida de manera gratuita. Esto impulsó a la comunidad de desarrollo de Linux (y en particular a Linus Torvalds, el creador de Linux) a desarrollar su propia herramienta basada en algunas de las lecciones que aprendieron mientras usaban BitKeeper. 

Desde su nacimiento en el 2005, Git ha evolucionado y madurado para ser fácil de usar y conservar sus características iniciales. Es tremendamente rápido, muy eficiente con grandes proyectos y tiene un increíble sistema de ramificación (branching) para desarrollo no lineal
</div>

<br>

### **3. Caracteristicas**
<div style="text-align: justify"> 

**Algunas de las caracteristicas principales de Git son:**
<br>

-Git almacena la información como un conjunto de archivos.

-No existen cambios, corrupción en archivos o cualquier alteración sin que Git lo sepa.

-Casi todo en Git es local. Es difícil que se necesiten recursos o información externos, basta con los recursos locales con los que cuenta.

-Git cuenta con 3 estados en los que es posible localizar archivos: Staged, Modified y Committed.
</div>

<br>

### **4. ¿Qué es un sistema de control de versiones?**
<div style="text-align: justify"> 
Un Sistema de Control de Versiones (SCV) o Version Control System (VCS) en inglés: Es un sistema que registra los cambios realizados sobre un archivo o conjunto de archivos a lo largo del tiempo, de modo que puedas llevar el historial del ciclo de vida de un proyecto, comparar cambios a lo largo del tiempo, ver quién los realizó o revertir el proyecto entero a un estado anterior.
</div>

<br>

### **5. Introducción a los Comandos de GIT**
<div style="text-align: justify"> 
Para empezar con Git lo tienes que tener instalado en tu ordenador. Si todavía no lo tienes, puedes visitar su página y seguir las instrucciones para obtenerlo.

<br>

A continuación sera mostrado los comandos principales de Git, con los que podras empezar a trabajar con esta herramienta y aprovechar sus funcionalidades de forma rápida y sencilla. 
</div>

<br>

### **6. Comandos: Configuración Inicial**
<div style="text-align: justify"> 
Para configurar GIT y crear repositorios existen los siguientes comandos:

<br>

#### **-Git config**
El comando git config sirve para definir valores de configuración de Git a nivel de un proyecto global o local. Estos niveles de configuración se corresponden con archivos de texto con extensión .gitconfig.

**Sintaxis:** 
<br>
*git config --global user.name <Nombre_de_Usuario>*

*git config --global user.name <Direccion email>*

<br>

#### **-Git init**
El comando git init se ejecuta una única vez por cada proyecto. Sirve para que Git se prepare para controlar las diferentes versiones de los archivos de código fuente.

**Sintaxis:** *git init <Nombre_Repositorio>*

<br>

#### **-Git clone**
Este comando inicializa un nuevo repositorio en el repositorio local clonando íntegramente el contenido de un repositorio remoto que le indiquemos mediante una URL.

**Sintaxis:** *git clone <URL_Repositorio>*
</div>

<br>

### **7. Comandos: Manejo de Archivos y cambios**
<div style="text-align: justify"> 
Es necesario saber cómo guardar los cambios (en GitHub) de los archivos que creemos, modifiquemos y borremos en nuestro repositorio local.

<br>

#### **-Git add**
Una vez que hemos realizado los cambios necesarios en nuestra área de trabajo (working area), para comenzar la confirmación de dichos cambios, es necesario pasar todos los archivos que queramos confirmar al área de preparación (staging area).

**Sintaxis:** *git add [opciones] [<Archivo_1>] [<Archivo_2>]... [<Archivo_n>]*

<br>

#### **-Git commit**
Una vez que tenemos archivos preparados en el área de preparación, para confirmar dichos archivos y crear una confirmación de cambios la sentencia utilizada es git commit.

**Sintaxis:** 
<br>
*git commit [opciones] [<Archivo_1>] [<Archivo_2>]... [<Archivo_n>] [-m <"Mensaje de confirmación">]*

<br>

#### **-Git log**
Cada vez que confirmamos cambios (Hacemos un git commit), se crea una confirmación con un número hash identificativo. Dicho número hash determina cada confirmación realizada y será importante para futuras operaciones.

**Sintaxis:** *git log*

<br>

#### **-Git diff**
Este comando permite ver las diferencias que existen entre las confirmaciones que determinemos. Se hace referenciando las confirmaciones mediante su número hash.

**Sintaxis:** *git diff <hash de confirmación 1> <hash de confirmación 2>*

<br>

#### **-Git revert**
Puede utilizar dicho comando para deshacer de forma segura una confirmación que ya se haya enviado.

**Sintaxis:** *git revert hash_commit*
</div>

<br>

### **8. Comandos: Manejo de Repositorios Remotos**
<div style="text-align: justify"> 
La parte más interesante de GIT es la posibilidad de trabajar con repositorios remotos (como GitHub) para poder llevar a cabo proyectos grandes gracias a un equipo de desarrollo.

<br>

#### **-Git remote**
Para conectar al repositorio remoto con el cual nos comunicaremos entre nuestro repositorio local y dicho repositorio remoto el comando utilizado es git remote.

<br>

#### **-Git Branch**
Las ramas es uno de los conceptos más interesantes dentro de GIT. Permite el trabajo en paralelo sobre distintas partes del código base para añadir funcionalidades, corregir errores o realizar versiones de nuestros proyectos.

<br>

#### **-Git checkout**
Para moverse entre las ramas creadas y realizar los cambios necesarios sobre dichas ramas, el comando utilizado es git checkout.

<br>

#### **-Git status**
Podemos comprobar en cualquier momento el estado de la rama en la que nos encontramos para comprobar si existen archivos (o directorios) que tienen cambios que deben de ser confirmados o rechazados.
</div> 
<br> 
<hr>
