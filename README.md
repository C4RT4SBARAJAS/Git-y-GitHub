# Git y GitHub
![](https://camo.githubusercontent.com/79d66e25901bc682cf5d00ddd89e9ee24c2a0843e37a9a532c37a607ae7a19b4/687474703a2f2f656c6672656e657469636f696e666f726d617469636f2e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031372f31302f4769744875624c6f676f2e706e67)

![](https://img.shields.io/github/stars/pandao/editor.md.svg) ![](https://img.shields.io/github/forks/pandao/editor.md.svg) ![](https://img.shields.io/github/tag/pandao/editor.md.svg) ![](https://img.shields.io/github/release/pandao/editor.md.svg) ![](https://img.shields.io/github/issues/pandao/editor.md.svg) ![](https://img.shields.io/bower/v/editor.md.svg)

**Table of Contents**

[TOCM]

[TOC]

# ¿Qué es Git y GitHub?
La premisa es simple, en vez de guardar una versión de cada archivo, hay un sistema que gurda solo esos cambios. Ademas maneja el cambio que otras pesonas hagan sobre los mismos archivos, asi multiples pesonas pueden trabajar en un mismo proyecto sin pisarse. Cuando hay errores se puede saber precisamente quien hizo ese cambio. Si hay algo en una versión vieja que quieres recuperar lo puedes hacer de manera precisa.

En tu maquina local usas Git, funciona en la terminal o linea de comandos, y tiene comandos como: `merge`, `pull`, `add`, `commit` y muchos más.

Si quieres colaborar con otros, usar una interfa web o publicar tus proyectos en la web usas GitHub. Es un sistema como facebook o twitter que gurda tu proyecto, sus cambios y cada una de sus versiones.

GitHub es tan popular que es la red social de código. Una hoja de vida que demuestra lo que sabes.

No te limites a solo hacer `add`, `commit`, `pull`, `push` porque estarías desaprovechando el increíble poder de Git. Git tiene ramas, tags, remotos, colaboradores, fusiones y mucho más.

Git no es solo para programadores e ingenieros. Lo que sea que hagas que tenga versiones se puede poner en Git como un proyecto colaborativo.

## Ejemplo de un archivo de texto de toda la vida

| Versión  | Contenido del archivo| Guardado |
|------------|---------------|-----|
| 1  | Mi nombre es Heriberto Cartas. Soy estudiante de Ingeniería Forestal y en mis tiempos libres corro carreras, mecanografio libros y hago cosas raras con python. | biografía.txt |
| 2 | Mi nombre es Heriberto Cartas. Soy egresado de Ingeniería Forestal y en mis tiempos libres derribo árboles, mecanografio libros y hago cosas raras con R. | biografia_v2.txt |

Antes de conocer el sistema de control de versiones esta es nuestra única opción 🙄.

Sin embargo, la realidad es que son muy pocos los cambios que ocurrieron en el archivo y no deberiamos guardar todo el archivo de nuevo solo por esos cambios 👇.

| Versión  | Cambios al archivo| Guardado |
|------------|---------------|-----|
| 1  | Mi nombre es Heriberto Cartas. Soy ~~**estudiante**~~ de Ingeniería Forestal y en mis tiempos libres ~~**corro carreras**~~, mecanografio libros y hago cosas raras con ~~**python**~~. | biografía.txt |
| 2 | Mi nombre es Heriberto Cartas. Soy **egresado** de Ingeniería Forestal y en mis tiempos libres **derribo árboles**, mecanografio libros y hago cosas raras con **R**. | biografia_v2.txt |

Si hubiera una forma en la que solo guardamos esos cambios en lugar de guradar todo el archivo de nuevo, sería ideal. En particular cuando estamos trabajando multiples personas sobre el mismo archivo o cuando estamos cambiando pequeñas cosas en algo tan grande por ejemplo, el código de un proyecto de sofware. Y ahí, es donde entran los sistemas llamados sistemas de **Control de versiones**, que lo que hacen es solamente guardar esos cambios y dejar claro dónde ocurrieron, cuándo, quién los hizo, podemos volver a ellos en el pasado, entre muchas otras cosas. 

El sistem más popular del mundo es **Git**. Fue creado por la fundación Linux, particularmente por Linux Torvalds. Es el sistema que maneja el quernel de Linux. 

Asumiendo que tienes un archio llamado **biografia.txt** como tu archivo base, y que además sabemos de línea de comandos. Entras a esa capeta desde tu línea de comandos e imaginando que ya tienes instalado Git haces `git init`, lo que hace este comando de línea de comandos es empezar en tu carpeta un repositorio, que es esa base de datos donde se van a guardar los cambios de cualquier archivo, en este caso biografia.txt. Pero ahora tu repositorio tiene que saber que este archivo existe entonces ahí dentro lo colocas `git add biografia.txt`. Con esto la base de datos de cambios el sistema de control de versiones Git ahora sabe que existe biografia.txt. No es suficiente solo darle add, tiene que decirle que los cambios ya están listos. Para hacerlo colocas `git commit -m "versión 1"`. De esta manera se envian los últimos cambios del archivo a la base de datos del sistema de control de versiones, para controlar los cambios que se le hayan hecho. Y si quieres colocar un tipo de mensaje para que en el futuro tu sepas lo que hiciste ahí, agregas dentro de las comillas el mensasje que le quieras enviar. Esto es una muy buena practica, mantiene la higiene de tu proyecto entero. Y la higiene es muy importante sobre todo cuando pasa mucho tiempo o cuando empiezas a trabajar con diferentes miembros del equipo en un mismo proyecto.

Ya que tengo agregada a mi base de datos del sistema de control de versiones este archivo voy al editor y ago los cambios. Una vez echos los cambios guardo el archivo y ya esta. Tengo el archivo guardado en mi disco duro. Pero todavía no tengo guardado los cambios en mi repositorio. Entonces para ello, tengo que volver a agregar el archivo si quiero, realmente es opcional. Otra opción para agregar archivos es `git add .`. Cuando agregar el punto lo que haces es que agregas todos los archivos que allan cambiado en la carpeta donde en ese momento estas. Una vez añadido esos cambios de archivo vulves hacer un commit, agregas un mensaje y quedan esos cambios echos y ya quedan obsolutamente grabados.

Puedes ver como esta el status de tu base de datos haciendo `git status`. Otro comando importante es `git show`, te muestra todos los cambios historicos hechos. Incluyendo cuales han sido las líneas de código, las líneas de texto, o las líneas de cualquier archivo que allas añadido que allan cambiado. Cuándo se han hecho esos cambios y quién los hizo. Porque a un repositorio pueden acceder multiples personas. Si quieres ver la historia completa de un archivo puedes hacerlo con `git log biografia.txt`. 

Una vez ya estas listo y has completado todos estos pasos, quizas puedes llevar tu archivo a un servido remoto porque probablemente ese arhivo vive en un servidor en internet o en un servidor donde quieres que lo vea todo el mundo. Para ello utilizamos el comando git push, el cual te pemite enviar hacia otro repositorio remoto lo que estas haciendo y también con git pull lo puedes traer.

# Introducción a la terminal y línea de comandos

## Comandos

|  Nombre del comando | Descripción  |
| ------------ | ------------ |
| `pwd` | Muestra la ruta del directorio actual. |
| `cd` `cd ~` | Moverse al directorio home de Linux. |
| `cd /` | Para ir a mi home en windows |
| `cd <ruta del directorio>` | Permite cambiar y navegar entre directorios. |
| `ls -l` | Lista los archivos de mi carpeta. |
| `ls -al` | Muestra todos los archivos incluso los ocultos y los coloca en una lista. |
| `clear` `Control + L` | Limpia la consola. |
| `cd ..` | Para volver a una capeta anterior. |
| `mkdir <nombre de la carpeta>` | Permite crear un directorio o carpeta. |
| `touch <nombre del archivo.extensión>` | Permite crear un archivo según la extensión especificada. |
| `cat <nombre del archivo>` | Permite visualizar el contenido de un archivo y mostrarlo en la terminal. |
| `history` | Muestra el historial de los comandos que se han hecho. |
| `!<número>` | Permite repetir un comando invocando el número que nos muestra el comando `history` |
| `rm <nombre del archivo>` | Permite borrar un archivo. |
| `rm -r <nombre del directorio>` | Permite borrar un directorio. |
| `rm -rf .git` | Elimina todo el repositorio dejando solo el directorio de trabajo. Util despues de realizar un `git init`. |
| `cp <archivo a copiar> <nombre de la copia>` | Crea una copia de un archivo dentro de la misma carpeta. Primero se coloca el archivo a copiar, enseguida la copia con un nombre diferente. Si queremos copiar el archivo en una ruta diferente debemos especificarla en `<nombre de la copia>`. |
| `cp -r <directorio a copia/> <ruta de destino/nombre de la copia>` | Permite copiar directorios completos (archivos y subcarpetas) a una ruta especificada. |
| `mv <old name> <new name>` | Cambia del nombre de un archivo o carpeta. Primero se coloca el archivo o carpeta que queremos renombrar, enseguida el nombre del nuevo archivo o carpeta. |
| `mv <directorio a mover/> <ruta de destino/directorio a mover>` | Permite mover un directorio a una ruta diferente conservando el mismo nombre. Sin embargo, este nombre puede ser diferente. |
| `mv <archivo a mover> <ruta de destino/archivo a mover>` | Permite mover un archivo a una ruta diferente convervando el mismo nombre. Sin embargo, este nombre puede ser diferente. |
| `<comando> --help` `man <comando>` | Permite acceder a la ayuda y explicación de un comando en específico |
| `<comando> --<agumento de palabra>` | Sintaxis de un comando al utilizar palabras completas de agurmento. |
| `<comando> -<agumento de letra>` | Sintaxis de un comando al utilizar letras de agurmento. |

# Crear un repositorio en Git y hacer mi primer commit

## Crear un repositorio
1. Tienes que decir dónde esta tu carpeta central de tus archivos. Para verificarlo usamos el comando `pwd`.
2. Para inicializar el repositorio escribo el comando `git init`. Se crea una capeta oculta en mi directorio. Lo compruebo con `ls -al`.
3. Para empezar a trabajar puedes crear un archivo con el comando `touch`. 
4. Para abrir este archivo utilizamos un editor de código. Por ejemplo, para abirlo con Visual Studio Code escribimos `code <nombre del archivo>`. Y para abir el directorio completo el comando `code .`.
5. Podemos ver el status del repositorio con `git status`. Cuando creamos un archivo por primera vez nos dirá que hay archivos no rastreados, así que para que sean rastreados usamos el comando `git add <nombre del archivo>` o `git add .`, para agregar todos los cambios que han ocurrido en ese respositorio.
6. Si los cambios están listos podemos realizar un commit, si aún no, entonces podemos quitar o deshacer el add con el comando `git rm --cached `. Muy útil cuando nos equivocamos.
7. Después del add al archivo entra a un estado conocido como stage. Lo único que falta es hacer guardar esos cambios en la base de datos. Para ello utilizamos el comando `git commit -m "<mensaje corto o explicativo del cambio>"` Un commit no es solo una buena práctica sino que además, es muy importante y obligatorio. Para poder enviar mi primer commit necesito haber configurado primero mi Git.

## Configuración de Git

1. Ejecutamos el comando `git config`. Nos muestra todas las configuraciones que tiene Git y como funcionan 
2. Para ver la configuración por defecto de mi git y las cosas que le faltan, ejecutamos `git config --list`. Debiendo verificar que hay un nombre de usuario e email de usuario para saber quien realiza los cambios en mi Git. 
3. Para cambiar la configuración del nombre de usuario en Git usamos el comando `git config --global user.name "<nombre de usuario>"`.
4. Para cambiar la configuración del email en Git usamos el comando `git config --global user.email "<correo electrónico>"`.
5. Hecho ésto ya puedo enviar mi primer commit.

## Mi primer commit

1. Ahora que estoy listo para enviar mi primer commit escribo nuevamente `git commit -m "<mensaje>"`. 
2. Cada vez que un archivo en mi repositorio se modifique y quiera gurdar esos cambios en la historia necesito repetir el ciclo > `git add .` agrega todos los cambios echos para este directorio > `git commit -m "<mesaje"`, para guardar los cambios en mi repositorio. 
3. Cuando se crea un archivo por primera vez obligatoriamente necesito escribir el comando `git add .` y después el commit. Sin embargo, cuando el archivo ya ha sido comiteado puedo acotar estos dos pasos con el comando `git commit -am "<mensaje>"`.
4. Para ver la historia de mi repositorio ejecuto el comando `git log <nombre del archivo>`.

## Interpretación del git log 😲

1. El `commit 63329741cc9eb9ef6f38c09ad071e3acaa9773ba` indica el tag, la indicación de donde estoy en este momento, el nombre de esa modificación o commit. Es un código interno que se usa. 
2. El `(HEAD -> master)` indica que ese tag o commit  es la versión más reciente.
3.  El `Author: Heriberto <heribertocartas@gmail.com>` indica que el autor fue un tal Heriberto de un tal email. Para ello sirvió configurar git anteriormente.
4.  `Date:   Tue Jul 27 23:51:02 2021 -0500` fue hecho en determinada fecha.
5.  `Modifiqué el README.md` muestra un mensaje. El cual es el mismo que agregamos al eviar un commit.
6. Muestra todos los commits anteriores a este si los tuviera.
7. Para salir del `git log` presionamos la tecla `q`.

## Analizar cambios en los archivos de tu proyecto con git show 😨

1. Te muestra el commit el último commit, es decir el más reciente. La misma interpretación del git log.
2. Además,  muestra `diff --git a/README.md b/README.md` indica que toma la versión nueva con la versión vieja y me muestra la diferencia. 
3. `index 0ff131e..b1bbcee 100644` es un indicador en la base de datos de git de dónde se guardan los cambios. 
4. `--- a/README.md`  `+++ b/README.md` indica que hay una versión a y una versiión b. 
5. `@@ -99,5 +99,41 @@` un indicador de cuantos bytes cambiaron. 
6. A continuación te muestra las líenas que cambiaron con los colores rojo `-`y en verde `+`. El color rojo indica lo que se quito o reemplazo, y el color verde lo que se agregó o por lo cual se reemplazó.
7. `\ No newline at end of file` indica que no hay un enter adicional.

## Enviar un commit sin mensaje 😱
1. Si guardamos los cambios con un `git commit` sin mensaje lo que provoca es que nos abre un editor de código de básado en lína de comandos llamado (Vim).


```flow
st=>start: Flujo de trabajo en git
op=>operation: git init
cond=>condition: Successful Yes or No?
e=>end: To admin

st->op->cond
cond(yes)->e
cond(no)->op
```