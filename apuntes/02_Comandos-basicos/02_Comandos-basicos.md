# **Comandos Básicos de Git**

### Indice 
[Inicializar un repositorio local](#inicializar-un-repositorio-local)  
[Directorio ***.git***](#directorio-git)  
[Los tres estados (staged, modified, comitted)](#los-tres-estados-staged-modified-comitted)  

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