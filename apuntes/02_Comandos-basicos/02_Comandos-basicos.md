# **Comandos Básicos de Git**

[Ir a Subtema anterior](../01_Introduccion/01_Introduccion.md)

### Indice 

[Configuración de ***Git***](#configuración-de-git)  
[Inicializar un repositorio local](#inicializar-un-repositorio-local)  
[Directorio ***.git***](#directorio-git)  
[Los tres estados (***staged, modified, comitted***)](#los-tres-estados-staged-modified-comitted)  
[git **add**](#git-add)  
[git **status**](#git-status)  
[git **commit**](#git-commit)  

## Configuración de GIT

Antes de usar ***Git*** debemos indicarle quienes somos. Esto lo podemos hacer gracias al comando `git config`.

El comando ***git config*** anterior te permite establecer variables de configuración que controlan el aspecto y funcionamiento de Git en tu computadora.

***Nota:*** Esta configuración solo se hace la primera vez que configuras **Git** en tu computadora. Solo es necesario volver a establecer los valores cuando quieras hacer un cambio específico (***correo, alias, etc***).

### Configuración de identidad

A continuación vamos a configurar nuestro nombre y nuestro email.

***Ejemplo:***  
- **Nombre:**
```bash
git config --global user.name "Aldo Santiago"
```
- **Email:**
```bash
git config --global user.email "correo@dominio.com"
```

Puedes comprobar la configuración usando `git config user.name` o la variable de configuración que desees.

## Inicializar un repositorio local

Para crear un repositorio se escribe el comando `git init` en el directorio en el que te encuentras.

Una vez hecho eso, verás que se crea un directorio oculto llamado ***.git***. 

![Directorio ***.git***](img/directorio-git.PNG)

## Directorio ***.git***

Esta carpeta es la más importante de todo ***git*** puesto que almacena todos los metadatos y la base de datos de objetos para tu proyecto. 

![Contenido de la carpeta ***.git***](img/contenido-directorio.png)

Toda esta carpeta es la que se copia cuando clonas un repositorio desde otra computadora al hacer `git clone`.

## Los Tres Estados (***staged, modified, comitted***)

En ***Git***, existen tres estados principales en los que se pueden encontrar tus archivos:
- Confirmado (***comitted***): Los archivos están almacenados correctamente en tu base de datos local. 
- Modificado (***Modified***): El archivo ha sido modificado pero aún no está almacenado en la base de datos.
- Preparado (**staged**): El archivo está listo para ser confirmado.

---
**El flujo de trabajo básico en Git es algo así:** 
1. Modificas una serie de archivos en tu directorio.
2. Preparas los archivos, añadiendolos a tu área de preparación.
3. Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación y almacena esa copia instantánea de manera permanente en tu directorio de Git.
> Según Pro Git (p. 22)
---

## Comando ***add***, **status** y **commit**.
### **Ejercicio incluido**

Supongamos que inicializamos el repositorio de ***Git*** en algún directorio. Ahora, dentro de este directorio creamos archivos nuevos (***texto, python, c, cpp, etc***). 

### **git add**

Para que los archivos creados puedan guardarse en tu base de datos de forma segura, es necesario hacer un ***commit***, pero para hacer un commit primero debemos agregar estos archivos al **stage** de la siguiente forma:

- ***Para un solo archivo***

```bash
git add "Nombre del archivo"
```

- ***Para varios archivos***
```bash
git add "Archivo1" "Archivo2" "Archivo3"
```

- **Para añadir todos los archivos modificados del directorio**
```bash
git add .
```
***Nota:*** Tambien puedes agregar carpetas, no solamente archivos. 


### ***git status***

El comando `git status` en ***Git*** te proporciona información sobre el estado actual de tu repositorio. Al ejecutar ***git status***, obtendrás detalles sobre los archivos que han sido modificados, los archivos que han sido agregados al área de preparación (***staging area***), y cualquier archivo que aún no haya sido rastreado por **Git**.

Así que, una vez agregados los archivos al ***stage*** podemos ver el estado de nuestro repositorio usando el comando `git status`.

***Ejemplo antes de hacer `git add .`***

![Ejemplo git status](img/status1.png)  
Imagen. Ejemplo en **git bash**

***Ejemplo despues de hacer `git add .`***

![Ejemplo git status](img/status2.png)  
Imagen. Ejemplo en **git bash**


Si bien es cierto que la salida de ***git status*** es bastante explícita, también es verdad que es muy extensa. Por esta razón, **Git** ofrece una opción para obtener un estado abreviado, de manera que puedas ver tus cambios de una forma más compacta. Si ejecutas `git status -s` o `git status --short`, obtendrás una salida mucho más simplificada.

![ejemplo status abreviado](img/status-abreviado.png)  
Imagen. Ejemplo en **git bash**

### **git commit**

Cuando has agregado los archivos/carpetas al **stage** y te has asegurado que tus cambios están listos para guardarlos de forma segura a tu base de datos, entonces puedes ejecutar el comando `git commit`.

Cuando realizas un ***commit*** en ***Git***, se espera que proporciones un mensaje que describa los cambios que estás confirmando, esto se hace de la siguiente forma:

```bash
git commit -m "Mensaje descriptivo"
```

**Nota:** El argumento adicional `-m` viene de '***message***'.

