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
1. Si guardamos los cambios con un `git commit` sin mensaje lo que provoca es que nos abre un editor de código de básado en lína de comandos llamado Vim (del inglés Vi IMproved) es una versión mejorada del editor de texto vi, presente en todos los sistemas UNIX. Otra forma de acceder a Vim es con el comando `vim <nombre dle archivo>`.
2. Lo primero que nos dice el editor es `# Please enter the commit message for your changes.`. Es decir, agrega un mensaje para tus cambios.
3. Lo segundo es `Lines starting # with '#' will be ignored, and an empty message aborts the commit.`. Es decir, toda lína dentro del editor que comienze con el simbolo `#` será tomada como comentario o ignorada y que un mensaje bacio abortará el commit.
4. Estando en el editor de código sin escribir nada más, comenzamos a escribir nuestro mensaje, una vez listo el mensaje necesitamso salir y guradar los cambios. Para ello, escribimos `Control + X`, seguido de `Y` y por último `Enter`.
5. Los cambios se envian correctamentea al repositorio.

## Comparando commits con git diff
1. Para compararar un cambio anterior con el cambio más reciente utilizamos el comando `git diff <cambio anterior> <cambio más reciente>`. Esta es la forma en la que git show y git diff comparan los cambios por default.
2. Para comparar el cambio más reciente con uno anterior, utilizamos el sigueinte orden `git diff <cambio anteior> <cambio más reciente>`.

## Ciclo básico de trabajo en Git
![](https://static.platzi.com/media/public/uploads/capture1_44e940e0-77b2-4f04-b76d-d7637b4ca7a7.PNG)

1. Tienes una carpeta o **directorio** donde están los archivos de tu proyecto. En este directorio que se llama en este caso **proyecto1** , tenemos el archivo **historia.txt**. Y cuando entramos por consola a ese directorio y escibimos el comando `git init`. Pasan dos cosas, se crea un área en memoria ram que se llama **staging**, es donde a principio se van agregando los cambios y se crea el repositorio. Este repositorio es una carpeta que conociemso como `/.git/`, donde estarán todos los cambios al final de tu proyecto. 
2. Una vez haces cambios a tu archivo **historia.txt** lo agregas al **staging** area usando el comando `git add historia.txt`. Cuando haces add este archivo pasa a vivir a **staging**. Y en este momento el archivo esta esperando a que lo envies al repositorio. Mientras tanto puedes agregar otros archivos o puedes removerlo usando el comando `git rm`. Pero suponiendo que los no remueves nada y los cambios ya están listos para enviarse lo que haces **commit** con el comando `git commit`. Al hacer esto el archivo se va al repositorio. Y ese repositorio tiene un nombre por defecto, su nombre es **master** y master es donde van a estar todos los cambios que hagas. 
3. Es necesario entender los estados del archivo. Cuando aún no le has dado `git add` el archivo esta sin rastrear o en ingles **untracked**. Una vez hecho el `git add` el archivo entra al estado **tracked**, es decir lo estamos rastreado y ahí hace parte de **staging**. Cuando le damos `git commit` esos cambios pasan de estar traqueados en staging a traqueados en el **repositorio**.
4. ¿Qué pasa cuando quieres traerte un cambio que esta en el repositorio pero que no esta en tu carpeta? por ejemplo, si un miembro de tu equipo hizo un cambio al archivo que tu no lo tienes en tus archivos locales porque trabajaron sobre el mismo archivo. Lo que haces es ir a la vesión final de repositorio y para traertela a tu carpeta existen un comando llamado `git checkout`. Con este comando tu traes los últimos cambios, una versión justo antes o los que quieres hacia tu carpeta. Con esto puedes traerte todos los cambios, ciertos cambios o los cambios de ciertos archivos dependiendo de como modifiques el comando `git checkout`.
5. Recuerda que cada vez que haces un **commit** de tu archivo hacia el **repostirio**, estas creando una nueva **versión** **v1**, **v2**, **v3** etc. Cada **commit** es una nueva **versión** de cambios de tu archivo hacia el **respotorio**. Y esos números raros que salen ahí en cada uno de los commits es el nombre interno en la base de datos de git de ese cambio.


## Ciclo de vida o estado de los archivos
Cuando trabajamos con Git nuestros archivos pueden vivir y moverse entre** 4 diferentes estados**:
- **Archivos Untracked**: son archivos que NO viven dentro de Git, solo en el disco duro. Nunca han sido afectados por `git add`, así que Git no tiene registros de su existencia. Recuerda que hay un caso muy raro donde los archivos tienen **dos estados al mismo tiempo**: **staged y untracked.** Esto pasa cuando guardas los cambios de un archivo en el área de Staging (con el comando `git add`), pero antes de hacer commit para guardar los cambios en el repositorio haces nuevos cambios que todavía no han sido guardados en el área de Staging (en realidad, todo sigue funcionando igual pero es un poco divertido).
- **Archivos Unstaged**: entiéndelos como archivos “**Tracked pero Unstaged**”. Son archivos que viven dentro de Git pero no han sido afectados por el comando git add ni mucho menos por git commit. Git tiene un registro de estos archivos, pero está desactualizado, sus últimas versiones solo están guardadas en el disco duro.
- **Archivos Staged**: son archivos en Staging. Viven dentro de Git y hay registro de ellos porque han sido afectados por el comando `git add`, aunque no sus últimos cambios. Git ya sabe de la existencia de estos últimos cambios, pero todavía no han sido guardados definitivamente en el repositorio porque falta ejecutar el comando `git commit`.
- **Archivos Tracked**: son los archivos que viven dentro de Git, no tienen cambios pendientes y sus últimas actualizaciones han sido guardadas en el repositorio gracias a los comandos `git add` y `git commit`.

**Recuerda** que hay un caso muy raro donde los archivos tienen **dos estados al mismo tiempo**: **staged y untracked**. Esto pasa cuando guardas los cambios de un archivo en el área de Staging (con el comando `git add`), pero antes de hacer commit para guardar los cambios en el repositorio haces nuevos cambios que todavía no han sido guardados en el área de Staging (en realidad, todo sigue funcionando igual pero es un poco divertido).

## Comandos para mover archivos entre los estados de Git
- `git add`: nos ayuda a mover archivos del Untracked o Unstaged al estado Staged. Podemos usar git nombre-del-archivo-o-carpeta para añadir archivos y carpetas individuales o `git add -A` para mover todos los archivos de nuestro proyecto (tanto Untrackeds como unstageds).
- `git reset HEAD`: nos ayuda a sacar archivos del estado Staged para devolverlos a su estado anterior. Si los archivos venían de Unstaged, vuelven allí. Y lo mismo se venían de Untracked.
- `git commit`: nos ayuda a mover archivos de Unstaged a Tracked. Esta es una ocasión especial, los archivos han sido guardados o actualizados en el repositorio. Git nos pedirá que dejemos un mensaje para recordar los cambios que hicimos y podemos usar el argumento `-m` para escribirlo (`git commit -m "<mensaje>"`).
- `git rm`: este comando necesita alguno de los siguientes argumentos para poder ejecutarse correctamente: `git rm --cached`: mueve los archivos que le indiquemos al estado Untracked. `git rm --force`: elimina los archivos de Git y del disco duro. Git guarda el registro de la existencia de los archivos, por lo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).

## ¿Qué es un Branch (rama) y cómo funciona un Merge en Git??

![](https://static.platzi.com/media/public/uploads/branches_f9d7e237-6a15-4143-a4e9-cc5af06be833.PNG)

1. Por defecto estás en una **rama** que se llama **master**, y aquí es donde tienes los cambios de tus archivos. Por ejemplo, **v1** y cada vez que hago un commit creo una nueva **versión** **v2**, **v3**, tantas versiones como quiera hasta tener la **versión actual**. Todo esto en el **master**.
2. Pero resulta que en un punto en la versión 3, decidíste que ibas hacer experimentos raros por tu propia cuenta. Pensaste en **cambiar la libreria** actual por otra librería y haber que tal te iría. Para ellos creamos la **rama experimental**, lo que hace es copiar la vesión actual o una anterior de la rama master y le pones un nombre, para este caso le pusé el nombre de **experimentos**. Y ahí sigues con tus commits, entonces aquí estan la **v2** del commit, la versión 3, etc. Y todo esta rama  es completamente diferente en código y en contenido que la rama actual de master, porque estas cambiando cosas. 
3. Digamos que mientras seguias cambiando cosas encontraste un **bug** terrible en la **versión actual** y ese **bug** te obliga a modificar cosas. Si necesitas **arreglar un bug** de la** vesión actual** lo más probable es que tengas que crear una rama especial que digamos que se va a llamar **bugfixing** aunque normalmente en la industria la llaman **hotfix** porque es un arreglo en caliente. Y ahí haces tus cambios y luego los pruebas con la **rama actual**, y esa prueba o conexión hacia la rama actual es lo que se conoce como **un merge**, que es **cuando unes los cambios** de una rama con otra, y termines con una **versión final**, conectada entre el cambio que hiciste y la úlima versión de la rama actual y esta es la última versión llamemosla la versión final, la **versión HEAD**, donde están en este momento todos los cambios.
4. En algún punto tu sigues haciendo tus **experimentos** y cuando ya tienes los **cambios finales** de tus **experimentos** y quieres unirlos a la **rama actual** entonces haces exactamente los mismo. Lo que haces es que le pides a esa rama experimental que se **fusione con la rama HEAD actual** y creen una nueva vesión final final final en el **repositorio master**. Este proceso también es conocido como un **merge**.
5. Podemos crear todas las **ramas** y **commits** que queramos. Podemos aprovechar el registro de cambios de Git para crear ramas, traer versiones viejas del código, arreglarlas y combinarlas de nuevo para mejorar el proyecto. Esa es **la magia de Git** y todo **su base de datos atómica**.
6. Este es **extremadamente común**, esto es como casí siempre funciona **el ciclo de trabajo** en el mundo de Git. Normalmente a la rama experimentos le llaman la rama de **developmet**. Y a hotfixing le llaman **hotfix** porque son los cambios que tienen que salir ya mismo. **Master siempre es master**.
7. Solo ten en cuenta que **fusionar** estas **ramas puede generar conflictos**. Algunos archivos pueden ser diferentes en ambas ramas. Git es muy inteligente y puede intentar unir estos cambios automáticamente, pero no siempre funciona. En algunos casos, somos nosotros los que debemos **resolver** estos **conflictos** a mano.

## Volver en el tiempo en nuestro repositorio utilizando reset y checkout

1. Imaginemos que queremos volver en el tiempo a donde estuvimos por decir un ejemplo al segúndo commit. Para ello, necesitamos entender cuales han sido los commits que han ocurrido hasta ahora llendo a nuestra carpeta principal del repositorio y escribiendo `git log`. Nos muestra todos los commits hechos. Ubicamos el segundo con su respectivo ID es decir: `85c7d9f3c94c718c749647e1db84f085db700b7d`.
3. Existe el comando `git reset`. Este comando nos permite voler a una versión anterior, si le colocamos enfrente la versión anterior a la que queremos volver: `git reset <ID del commit>`. Pero antes hay dos tipos de reset, el duro usando el argumento `--hard` y el suave usando el argumento`--soft`. Si le damos `git reset <ID del commit> --hard` todo vuleve al estado anterior, es el mas peligroso, pero el que más normalmente la gente usa. Si usamos en cambio `git reset <ID del commit> --soft` lo que tengamos en staging sigue en staging, es decir que si has hecho `git add` eso sigue ahí disponible para el próximo commit. Solo que en el directorio de trabajo vulve a la vesión anterior.
4. Para volver realmente en el tiempo usamos el comando `git reset <ID del commit> --hard`. Lo que pasa es que ahora el HEAD apunta a ese commit. Cuando le damos `git log` es como si todo lo que hubieramos trabajado antes ubiera desaparecido por completo. Hay que tener cuidado porque esto realmente borra todo lo que hiceron antes. Entonces puede ser muy peligroso ejecutarlo. En una forma de volver al pasado de una manera agresiva.

## Visualizar cambios especificos en archivos con git log --stat

El comando `git log --stat` te permite ver los cambios específicos que se hicieron en cuales archivos a partir del commit. Los cambios se muestran de la siguiente manera, por ejemplo, `README.md | 8 +++++++-` indica el archivo y el número de bytes que cambió. Y de forma más de tallada nos dice `1 file changed, 7 insertions(+), 1 deletion(-)`.

## Volver a una versión anterior con git checkout
Muy útil cuando solo queremos ver como era un archivo o directorio anteriormente.
Para volver a una versión anterior para un archivo manteniendo el HEAD en el master utilizamos el comando `git checkout <ID commit> <nombre del archivo>`, si queremos guardar esos cambios entonces hacemos un `git commit`. Para volver a una versión para el directorio completo, haciendo este commit el HEAD utilizamos `git checkout <ID commit>`. Si queremos salir sin guardar nada y volver al HEAD master entonces utilizamos el comando `git checkout master <nombre del archivo>` o `git checkout master` para el directorio completo.

# Git reset vs git remove
Git reset y git rm son comandos con utilidades muy diferentes, pero aún así se confunden muy fácilmente.

## Git rm
Este comando nos ayuda a eliminar archivos de git sin eliminar su historial del sistema de versiones. Esto quiere decir que si necesitamos recuperar el archivo solo debemos “viajar en el tiempo” y recuperar el último commit antes de borrar el archivo en cuestión. Para indicarle a git cómo eliminar los archivos que ya no necesitamos en la última versión del proyecto utilizamos:
- `git rm --cached <archivo>`: Elimina los archivos del área de Staging y del próximo commit pero los mantiene en nuestro disco duro.
- `git rm --force <archivo>`: Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).

## Git reset
Este comando nos ayuda a volver en el tiempo. Pero no como `git checkout` que nos deja ir, mirar, pasear y volver. Con `git reset` volvemos al pasado sin la posibilidad de volver al futuro. Borramos la historia y la debemos sobreescribir. No hay vuelta atrás. Este comando es **muy peligroso** y debemos usarlo solo en caso de emergencia. Hay dos formas de usar `git reset`:
- `git reset --soft`: borramos todo el historial y los registros de git pero guardamos los cambios que tengamos en **Staging**, así podemos aplicar las últimas actualizaciones a un nuevo commit.
- `git reset --hard`: borra todo. Todo todito, absolutamente todo. Toda la información de los commits y del área de Staging se borra del historial.
- `git reset HEAD`: este es el comando para sacar archivos del área de **Staging**. No para borrarlos ni nada de eso, solo para que los últimos cambios de estos archivos no se envíen al último commit, a menos que cambiemos de opinión y los incluyamos de nuevo en **Staging** con `git add`, por supuesto.

### ¿Por qué esto es importante?

Imagina el siguiente caso: hacemos cambios en los archivos de un proyecto para una nueva actualización. Todos los archivos con cambios se mueven al área de **Staging** con el comando `git add`. Pero te das cuenta de que uno de esos archivos no está listo todavía. Actualizaste el archivo pero ese cambio no debe ir en el próximo commit por ahora.

### ¿Qué podemos hacer?

Bueno, todos los cambios están en el área de **Staging**, incluido el archivo con los cambios que no están listos. Esto significa que debemos **sacar ese archivo de Staging** para poder hacer commit de todos los demás.

¡Al usar `git rm` lo que haremos será eliminar este archivo completamente de git!. En este caso no buscábamos eliminar un archivo, solo dejarlo como estaba y actualizarlo después, no en este commit.

En cambio, si usamos `git reset HEAD`, lo único que haremos será mover estos cambios de **Staging** a **Unstaged**. Seguiremos teniendo los últimos cambios del archivo, el repositorio mantendrá el archivo (no con sus últimos cambios pero sí con los últimos en los que hicimos commit) y no habremos perdido nada.

# Comandos de git

## Comandos para colaborar

| Nombre del comando | Descripción |
| ------------ | ------------ |
| `git log --oneline` | Muestra el ID del commit y el título del commit. |
| `git log --decorate` | Muestra donde se encuentra el head point en el log. |
| `git log --stat` | Explica el número de líneas que se cambiaron brevemente. |
| `git log -p` | Explica el número de líneas que se cambiaron y te muestra que se cambió en el contenido. |
| `git shortlog` | Indica que commits ha realizado un usuario, mostrando el usuario y el titulo de sus commits.  |
| `git log --graph --decorate --oneline ` | Muestra mensajes personalizados de los commits. |
| `git log --pretty=format:"%cn hizo un commit %h el dia %cd"` | Muestra mensajes personalizados de los commits. |
| `git log -<número>` | Limitamos el número de commits |
| `git log --after=“2021-7-29”` | Commits para localizar por fechas. |
| `git log --after=“yesterday”` | Commits para localizar por fechas. |
| `git log --after=“2021-7-29” --before=“today”` | Commits para localizar por fechas. |
| `git log --author=“nombre de algún autor”` | Commits realizados por autor que cumplan exactamente con el nombre. |
| `git log --grep="Modifiqué el REDME.md"”` | Busca los commits que cumplan tal cual está escrito entre las comillas. |
| `git log --grep="modifiqué el redme.md" -i` | Busca los commits que cumplan sin importar mayúsculas o minúsculas. |
| `git log – README.md` | Busca los commits en un archivo en específico. |
| `git log -S “<contenido a busca>”` | Busca los commits con el contenido dentro del archivo. |
| `git log > log.txt` | guardar los logs en un archivo txt |

## Comandos de un flujo de trabajo

| Nombre del comando | Descripción |
| ------------ | ------------ |
| `git commit -am "<mensaje>"` | Fusiona los comandos `git add` y `git commit` . Solo se puede usar si al archivo ya se le ha hecho un **add** anteriormente. |
| `git commit -a` | Ejecuta el comando `git add` y no permite enviar un commit a traves del editor de código Vim. |
| `git reset` | Te permite eliminar commits |
| `git branch -d` | Te permite eliminar ramas |
| `git log --all` | Nos muestra todos los commits que hemos hecho historicamente. |
| `git log --all --graph` | Te muestra de manera visual como funcionan las ramas o branches. |
| `git log --all --graph --decorate --oneline` | Muestra toda la hitoria de commit desde que arranco el proyecto de manera compremida. |
| `alias <nombre del alias>="<línea de comandos>"` | Te permite crear un alias en Linux. Se guarda de manera temporal durante tu sesión actual en la Terminal. |
| `<nombre del alias>` | Ejecuta un alias en Linux. Debiendo crear el alias primero. |
| `git config alias.<nombre del alias>`  | Guarda un alias en Git para un solo respositorio. |
| `git config --global alias.<nombre del alias>` | Guarda un alias en Git de manera global para todos los repositorios. |
| `git <nombre del alias>` | Ejectua un alias guardado en Git. |
| `alias` | Te permite ver todos los alias creados. |
| `unalias <nombre del alias>` | Elimina un alias. |
| `alias parpadeante="git log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white) - %an%C(reset)%C(blink yellow)%d%C(reset)' --all"` | Alias parpadeante. |
| `git checkout <nombre de la rama>` | Te permite cambiar de ramas. |
| `Git branch` | Te permite ver todas las ramas creadas. |
| `git show-branch` | Nos muestra las ramas que existen y cual ha sido su historia. |
| `git show-branch` | Muy similar al comando `git show-branch` pero con mas datos. |

# Flujo de trabajo básico con un repositorio remoto

Para manterner una historia entera de tu proyecto solo tienes que hacer el flujo de trabajo común, es decir, inicializar el repositorio con `git init`, agregar los cambios con `git add <archivo>` y eviar los cambios al repositorio con  `git commit -m "<comentario>"`. 

Pero ¿qué pasa cuando trabajas con otras personas?, ¿qué pasa cuando trabajas con un equipo de trabajo y el equipo de trabajo tiene un servidor donde esta la versión unificada de multiples desarrolladores? Cuando tu trabajas en este tipo de equipos necesitas un servidor o respositorio remoto. Es un lugar donde tienes el mismo repositorio en el que estás trabajando pero todo el mundo le manda datos para allá, trabajan el local y cuando terminan los volven a mandar para que el resto del equipo los pueda ver. Tipicamente esto es GitHub, GitLab, BitBucket, entre otros.

Para traernos datos de un servidor remoto lo que hacemos es envez de dar `git init` damos `git clone url` es decir clonar. Para ello debemos proporcionar la dirección (url) del repositorio remoto. Lo que hace `git clone url` es que se trae los archivos a dos lugares. Se trae una copia del master a tu directorio o carpeta de trabajo y crea la base de datos de todos los cambios historicos en el repositorio local. ¿Entonces como cambia esto mi flujo de trabajo? Simplemente siguo haciendo haciando `git add` cuando quiero añadir archivos a Staging y `git commit` cuando quiero enviarlos al repositorio local. Pero cuando el último commit en el HEAD esta listo para ser enviado al repositorio remoto hago un `git push`. Con este comando evio todo al servidor remoto. Y si hay confligtos lido con ellos.

Cuando ya estoy conectado al repositorio remoto, ya lo clone, pero quiero traermen una actualización porque alguién más cambio algo. Ahí lo que se hace es un `git fetch`, esto me trae la actualizaciión a mi repositorio local pero no me lo copia a mis achivos. Para que me los copie a mis archivos tengo que hacer un git `git merge`. Pero hay un comando que fusiona ambos conceptos y se llama el comando `git pull`. De esta manera siempre tengo una copia actualizada de lo último que paso en el repositorio.

# Introducción a las ramas o branches de Git

Las ramas son formas en las que nosotros podemos hacer cambios sin afectar la principal rama.

**Master** es nuestra rama principal. En esa rama nosotros tenemos toda nuestra historia de commits. El commit más reciente es el que nosotros llamados el **HEAD**.

**Antes** de crear una rama hay que tener en cuenta que, la rama se va a crear desde el lugar donde estoy. Debiendo crearse siempre desde la **rama master**. Para crearla utilizamos el comando `git branch <nombre de la rama>`. Y eso es todo. Lo que pasa es que se realiza una copia exacta del último commit en master a la `rama creada`. Para visualizar la **rama creada** utilizamos el comando `git branch`, el cual nos muestra todas las ramas creadas. También podemos utilizar los comandos `git log`, `git show` y `git diff` donde aparece junto al **HEAD** del **master**. Se vera de la siguiente manera: `(HEAD -> master, <rama creada>)`. Esto indica que  tengo un HEAD que le apunta al **master** y que también le apunta a la `<rama creada>`, es decir, el útlimo commit esta pegado a dos ramas distintas, pero todavía estoy trabajando en **master**.

Para moverme o cambiar de rama utulizamos el comando `git checkout <rama creada>`. Para asegurarnos de que en realidad estamos en la `rama creada` utilizamos el comando `git status` o `git branch`. Si ahora, estando en esta rama modificamos un archivo, lo agregamos a Staging y lo comiteamos, para este último cambio se verá de la siguiente manera: `(HEAD -> <rama creada>, master)`. Esto indica que el HEAD ahora le apunta a `<rama creada>`, dejando el **master** atras por un commit. Y si ahora volmermos a la rama máster con `git checkout master`, los cambios vuelven a ser los que teníamos en la rama master, y el **HEAD** vuelve a estar en **master**. Esta es la magia de Git, ustedes pueden tener multiples archivos cambiando, solo se guradan los cambios e inmediatamente los puedo ver.

# Fusión de ramas con Git merge

**Antes** de fusionar ramas hay que tener en cuenta a que rama queremos traer esos cambios o dónde quiero que ocurra la fusión, de lo contrario los cambios ocurrirán en la rama donde estoy. Debiendo ejecutarse siempre desde la **rama master**, la rama principal. Por lo que necesitaremos movernos de rama **master** con el comando `git checkout`. Recuerdemos que al ejecutar el comando `git checkout` para cambiar de rama o commit puedes perder el trabajo que no hayas guardado. Guarda tus cambios antes de hacer `git checkout`.

Para fusionar ramas utilizamos el comando `git merge <nombre de la rama que queremos traer>`. Este comando nos permite crear un nuevo commit con la combinación de las dos ramas. Debido a que es un commit siempre te pedirá un mensaje. De lo contrario no es un **merge**. Y eso es todo. Al dar `git log` podemos econtrar el último commit de la `<rama creada>`, el último commi de la rama **master** y el commit más reciente, un **merge**, producto de la fusión de estas dos ramas.

# Resolución de conflictos al hacer un merge

Git es muy inteligente y puede resolver algunos conflictos automáticamente: cambios, nuevas líneas, entre otros. Pero algunas veces no sabe cómo resolver estas diferencias, por ejemplo, cuando dos ramas diferentes hacen cambios distintos a una misma línea.

Esto lo conocemos como **conflicto** y lo podemos resolver manualmente, solo debemos hacer el merge, ir a nuestro editor de código y elegir si queremos quedarnos con alguna de estas dos versiones o algo diferente. Algunos editores de código como VSCode nos ayudan a resolver estos conflictos sin necesidad de borrar o escribir líneas de texto, basta con elegir una de las dos opciones **Aceptar el cambio actual** que es del HEAD (***Accept Current Change***) o **Aceptar el cambio que viene** que es de la `rama creada` (***Accept Incomin Change***). Después debemos guardar y commitear los cambios con `git commit -am "<mensaje>"`

Recuerda que siempre debemos crear un nuevo commit para aplicar los cambios del merge. Si Git puede resolver el conflicto hará commit automáticamente. Pero, en caso de no pueda resolverlo, debemos solucionarlo y hacer el commit.

Los archivos con conflictos por el comando `git merge` entran en un nuevo estado que conocemos como **Unmerged**. Funcionan muy parecido a los archivos en estado Unstaged, algo así como un estado intermedio entre Untracked y Unstaged, solo debemos ejecutar `git add` para pasarlos al área de staging y `git commit` para aplicar los cambios en el repositorio.

# Cambios en GitHub: de master a main

Desde el 1 de octubre de 2020 GitHub cambió el nombre de la rama principal: ya no es ***master*** (como aprenderás en el curso) sino ***main***.

Este derivado de una profunda reflexión ocasionada por el movimiento **#BlackLivesMatter**.

La industria de la tecnología lleva muchos años usando términos como master, slave, blacklist o whitelist y esperamos pronto puedan ir desapareciendo.

# ¿Qué es GitHub?

GitHub es un sitio web que tiene por dentro un super servidor de Git donde culquiera de nosotros puede clonar su repositorio o clonar su repositorio y compartirlo con otros personas, de tal manera que no solo estes tú creando tu propio código. También es una especie de interfaz visual de tus repositorios de tal manera que no tengas que vivir en la consola todo el tiempo para hacer ciertos cambios. Y es una de las herramientas colaborativas más importantes que existe en el mundo del desarrollo. Mucha gente lo llama la red social de los programadores porque tus repositorios son básicamente tu portafolio de proyectos como programador, entonces puedes organizarlos de tal manera que la gente vea qué es lo que tu sabes y puedes hacer.

# Crear un respotorio en GitHub

1. Lo primero que debemos hacer es crear una cuenta en GitHub.
2. Damos click en **New repository**.
3. Agregamos un **Repository name**.
4. De manera ***optional*** podemos agregar una **Description**.
5. Decidimos si queremos que nuestro repositorio sea **Public** o **Private**.
6. Decidimos si queremos **Initialize this repository with a README**. Este es un archivo con extensión .md que se va a ver en el instante que una persona entre al repositorio en GitHub. Esto es una muy buena práctica.
7. Decidimos si queremos **Add .gitignore**.
8. Decidimos si queremos **Add a license**. Estas son licencias a traves de las cuales puedes publicar tu código. Licencias de código abierto o semiabierto, etc.

Una vez creado el respositorio, se creara la URl del respositorio así como todos los archivos creados. Si decidimos inicializar con un `README.md` nos aparecera ese archivo, de lo contrario no nos aparecera ninguno hasta que creemos algúno. Si queremos ver el archivo damos click en él y se nos mostrarán pestañas como **Row**, la cual muestra el código Markdown del archivo, **Blame**, la cual muestra quién ha hecho tales cambios y los cambios. Y **history** muestra la historia del archivo, los commits, es lo mismo que hacer un `git log` dentro de nuestro respositorio.


# Traer cambios del respositorio remoto al respositorio local y agregar un origen remoto

1. Para hacerlo primero debemos ubicarnos en el directorio o respositorio correcto.
2. Para decirlo a Git que queremos agregar un origen remoto de nuestros archivos utilizamos el comando `git remote add origin <dirección del respositorio remoto en GitHub>`. Para agregar la `<dirección del respositorio remoto en GitHub>` utilizamos la pestaña **Code** en GitHub donde nos da la opción de ***Clone*** por **HTTPS** O **SSH**. Copiamos la URL elegida al comando `git remote` y damos **Enter**. Lo que ocurre es que se agrega un **origen remoto** al cual podemos hacer **fetch** y **push**.
3. Para visualizar esta información utilizamos el comando `git remote -v`. Mostrando además la URL elegida para el origen remoto.
4. Lo primero que tienes que hacer es integrar los cambios remotos antes de hacer un **push**. Ya que si creaste un archivo en GitHub, este respositorio remoto pasa a ser el **master** ahora. Para traernos estos cambios utilizamos el comando `git pull origin master`.
5. Para eviar los archivos que tenemos en local, junto con el historial de commits al repositorio en GitHub utilizamos el comando `git push origin master`. Si clonaste por **HTTPS** te pedira tu usuario y contraseña de GitHub para ejecutar este comando. Para comprobar este envio, recargamos GitHub en internet. Y listo. Si usamos `git log` podemos visualizar lo siguiente `(HEAD -> master, origin/master)`, donde el HEAD ahora también le apunta al origen remoto.


# Interpretando el primer git pull origin master

Nos muestra una advertencia o warning. La cual nos dice que no hay commits comunes. Esto por se la primera vez en reslizarse un `git pull` y por ser proyectos totalmente distintos. Nos muestra los cambios que existen en **deltas**. También me indica que la **branch master** es el **FETCH_HEAD**. Y que ahora tengo una **[new branch] master** que es **origin/master**. Ahora ya estoy conectado.

Si te aparece el siguiente **error**: `fatal: refusing to merge unrelated histories`. No te preocupes es normal, esto pasa cuando usas una **conexión** por **HTTPS**. Para solucionarlo utiliza el siguiente comando: `git pull origin master --allow-unrelated-histories`. Esto me permite **fusionar** lo que tengo en remoto con lo que tengo en local. Debido a que es un **merge** tendrás que escribir un **mensaje**. Ahora ya quedo todo listo. Los archivos creados en GitHub ahora están en local.

Si usaste una **conexión** por **SSH** este **error** no te aparecerá. El comando se abrá ejecutado sin problemas la primera vez.

# ¿Qué son las llaves públicas y privadas?

Piensa en la siguiente situación: estamos tu y yo,  en ese mar azul llamado internet. Y tú me quieres mandar un **mensaje secreto**. Lo que tu quieres es que nadie se entere de este **mensaje secreto**, tu quieres que me llegué a mi. Así que me lo envias por internet. Pero en el proceso lo pueden intervenir. Entonces, ¿qué se hace en estos casos cuando tengo un **mensaje secreto** que no queremos que nadie lo descubra?

Lo que se hace es cifrarlo, le colocas una contraseña, y una vez me llega a mí, yo utilizo la misma contraseña y obtengo el mensaje perfecto. El problema es ¿cómo envias esa contraseña? Porque si alguíen intercepta la contraseña lo va a poder decifrar. Entonces se inventaron un algoritmo que se llama llaves públicas y llaves privadas, que es también conocido como cifrado asimétrico de un solo camino.

# Cómo funcionan las llaves públicas y privadas

Funciona de la siguiente manera, si yo quiero que tu me envies ese **mensaje secreto**, yo voy a crear algo especial que se llama una llave pública y una llave privada. Estas llaves se crean con un proceso algoritmico. Las llaves están vinculadas matemáticamente una con la otra, lo que significa que, lo que yo cifre con la llave pública solo lo abre mi llave privada. La llave privada por su propio nombre es privada y solamente esta conmigo.

Ahora que yo cree estas llaves, las tengo que compartir. Lo que yo hago es que, yo te mando a tí mi llave pública. Te la mando por internet y tu la recibes. Y esa llave pública es como un proceso matemático, ese proceso matemático lo que me permite es convertir el **mensaje secreto** en algo completamente oculto. Y como la made por internet es completamente posible que alguíen la intercepte.

Y esta es la magia: lo que vamos a hacer es que tú copias una versión personal de mi llave pública. Y con esa llave pública tu haces un proceso matemático, el cual es cifrar el mensaje con mi llave pública que te envie, y a traves de ese proceso se genera un nuevo mensaje, el cual es algo completemente imposible de decifrar. Un mensaje cifrado. Dejando a los Hackers sin ninguna opción de poder optener el mensaje. ¿Pero como lo obtengo yo?

Para que yo pueda obtener el mensaje, yo copio ese mensaje cifrado y uso mi llave privada para convertirlo de regreso en las palabras que me enviaste tal cual. Y eso esa es la magia de una llave pública y privada.

Lo importante es que tú que me vas a enviar un **mensaje secreto**, mantengas ese mensaje secreto. Que viva en tu entorno local y que no le digas a nadie qu esta ahí. Y cuando me lo quieres eviar lo cifres con mi llave para que yo lo decifre con mi llave privada y obtenga el mensaje tal cual.

Ahora si lo quiero hacer al reves, entonces tú creas una llave pública y privada. Y esta llave pública me la mandas a mi. Y yo cifro el mensaje con tu llave pública, te lo envio y con tu llave privada decifras el mensaje.

Entonces cuando se hace ese compatir de dos llaves públicas entre dos personas, mientras mantengan sus llaves privadas. Es lo que les permite a esas dos personas tener comunicacines completamente seguras, y que nadie los intercepte.

# Resumen de las llaves públicas y privadas

Las llaves públicas y privadas nos ayudan a cifrar y descifrar nuestros archivos de forma que los podamos compartir sin correr el riesgo de que sean interceptados por personas con malas intenciones.

La forma de hacerlo es la siguiente:

1. Ambas personas deben crear su llave pública y privada.
2. Ambas personas pueden compartir su llave pública a las otras partes (recuerda que esta llave es pública, no hay problema si la “interceptan”).
3. La persona que quiere compartir un mensaje puede usar la llave pública de la otra persona para cifrar los archivos y asegurarse que solo puedan ser descifrados con la llave privada de la persona con la que queremos compartir el mensaje.
4. El mensaje está cifrado y puede ser enviado a la otra persona sin problemas en caso de que los archivos sean interceptados.
5. La persona a la que enviamos el mensaje cifrado puede usar su llave privada para descifrar el mensaje y ver los archivos.

***Puedes compartir tu llave pública pero nunca tu llave privada.***

# Llaves públicas y privadas en Git & GitHub

Recuerda que cuando te conectaste a GitHub pusiste tu nombre de usuario y contraseña. Al hacerlo esto tiene dos problemas:
1. Siempre tienes que estar haciendolo.
2. En principio esto es una conexión segura. Es **HTTPS**, es igual a cuando te conectas a un sitio web y tiene el candadito. Sin embargo el nombre de usuario y contraseña se están guardando en tu entorno local, eso significa que si en algún momento te roban tu laptop, eres vulnerable a PassWord cracking. A que crakeen la contraseña de tu repositorio. Y esto es muy problemático. Pueden agregar huecos de seguridad, esta es la forma en la que los sitios web son hackeados.

Para evitar eso tenemos que agregar **una capa de seguridad mucho más fuerte**. Es decir, crear un entorno de **llaves públicas y privadas en Git y GitHub**.

Ventajas de usar llaves públicas y privadas en Git y GitHub:

1. La seguridad es mas fuerte.
2. No tienes que volver a agregar nombre de usuario y contraseña.

# Cómo funcionan las llaves públicas y privadas en Git Y GitHub

Funciona de la siguiente manera:

1. En tu entorno local vas a crear una llave privada y una llave pública.
2. Una ves las creas le vas a enviar esa llave pública a GitHub a tu repositorio. Le vas a decir a GitHub, para este repositorio quiero que uses esta llave pública de mi llave privada que va a seguri siendo privada en mi computadora.
3. Y eso lo conectas por un protocolo nuevo. En lugar de conectarnos a nuestro respositorio por HTTPS, vamos a conectarnos por un protocolo llamado SSH, también conocido como (Secure Shell).
5. GitHub es muy inteligente, así que en la primera conexión se va a dar cuenta que le enviaste una llave pública que esta relacionada con tu llave privada, y te va a enviar cifrado con tu llave pública su propia llave pública de GitHub. Porque GitHub también tiene su propia llave privada. Esto ocurre de manera automática no hay que hacer nada. Automáticamente GitHub te va a enviar esa llave y tu la vas a conectar.
6. Como tú tienes la llave pública de GitHub cifrada y GitHub tiene tu llave pública, a partir de ahora puede haber una conexión de doble camino 100% cifrada por SSH y ya nunca más tienes que agregar contraseña.

Algo a agregar es que:

1. La llave privada que tu crees se le pued agregar una contraseña encima para hacerla aún mas fuerte y ún más poderosa.
3. Adicionalmente a eso tu deberías estar cifrando tu disco. Los discos se cifran en Windows con Bidloquer.

# Configura tus llaves SSH en local

**NOTA: las llaves SSH no son por repositorio o por proyecto. Sino por persona.**

Antes de hacer esto asegurate de tener el mismo correo electrónico de GitHub en tu configuración en local. Para verificarlo usamos el comando `git config -l`. Sino para hacerlo puedes repetir los pasos del apartado ***Configuración de Git***.

Vamos a crear una serie de llaves exclusivamente para ti. Para ello:

1. Nos dirigimos al HOME usando el comando `cd`.
2. Para crear la llave SSH utilizamos el comando `ssh-keyen -t rsa- -b 4096 -C "<tu email en GitHub>"`. El número **4096** indica la complejidad del algoritmo. Y damos Enter.
3. Ésto nos dira **generando llave publica y privada**. Y también **nos dira dónde debemos guardar la llave**. Aquí puedes colocar otra carpeta. Pero honestamente no se los recomiendo porque por defecto te la guarda en el HOME. Por eso es importante dirigirnos al HOME antes de crear la llave. La ruta se vería algo así: `(/home/<nombre de usuario>/.ssh/id_rsa>)`. Como podemos observar también me crea una carpeta `.ssh`, la cual es una carpeta oculta. Y un archivo `id_rsa` sin extención. No hagas nada simplemente da un **Enter**.
4. Ahora nos pedirá un **Passphrase**. Es decir, la contraseña adicional de texto que le vas a poner a tu llave pública y privada. Tu decides si colocarle un passphrase o no. Yo en general creo que sí. Pero sino, simple mente da dos **Enter** más.
5. Y listo. Te indica que tu tu identificación ha sido guardada en: `/home/<nombre de usuario>/.ssh/id_rsa>`. Te indica que tu llave pública ha sido guardada en `/home/<nombre de usuario>/.ssh/id_rsa.pub>`. Y te genera un **fingerprint** y un **randomart image**. Estas son maneras de cofirmar que tu llave es de verdad.

No es suficiente con lo que hicimos. El procedimiento es el mismo en Windows y Linux, pero en Mac no. Porque una vez tienes tu llave la tienes que agregar al entorno. Es decir, que el sistema operativo donde tu trabajas sepa que la llave existe. En Windows o Linux:

1. Tienes que revisar que el servido de llaves SSH este prendido. Para ello utilizamos el comando `eval $(ssh-agend -s)`. Al ejecutarlo te tiene que salir algo así: `Agent pid <numero>`. El `<numero>` indica que el proceso está corriendo. Entonces todo está bien.
2. El siguiente paso es agregar la llave a nuestro sistema, decirle que existe. Para ello tenemos que recordar donde la creamos: `(/home/<nombre de usuario>/.ssh/id_rsa>)` es decir en el HOME. Para dirigirnos ahí usamos el comando `cd`.
3. Una vez en el HOME utilizamos el comando `ssh-add ~/.ssh/id_rsa`. Nos muestara las dos llaves: `id-rsa` y `id-rsa.pub`. Debo agregar la llave privada la que no tiene extensión. Así que volvemos a ejecutar el comando `ssh-add ~/.ssh/id_rsa`. Y listo.

# Conexión a GitHub con SSH

Las llaves están creadas. Tenemos una **carpeta .ssh** en el **HOME** de tu entorno **local**. Y recuerda **siempre crea una llave pública y privada por cada computadora que uses**. Para hacer la conexión a GitHub:

1. Abres la llave pública ya sea con un editor de código o usando el comando `cat id_rsa.pub` para ver el contendio. Y copias.
2. Vas a tu perfil en GitHub. A **Settings**, a **SSH and GPG keys**, New SSH key. Agregas un **Title**, es decir, el nombre que le quieras dar a la llave, de preferencia el nombre de tu computadora y en **Key** pegas la llave. Click en **Add SSH key**.
3. A continuación me pide mi **contraseña** para continuar. Y listo.

# Cambiar la conexión del origen remoto de mi repositorio por SSH

Luego de crear nuestras llaves SSH podemos entregarle la llave pública a GitHub para comunicarnos de forma segura y sin necesidad de escribir nuestro usuario y contraseña todo el tiempo.

1. Para hacerlo primero debemos ubicarnos en el directorio o respositorio correcto.
2. Para decirlo a Git que queremos agregar un origen remoto de nuestros archivos utilizamos el comando `git remote set-url origin <dirección del respositorio remoto en GitHub>`. Para agregar la `<dirección del respositorio remoto en GitHub>` utilizamos la pestaña **Code** en GitHub donde nos da la opción de ***Clone*** por **HTTPS** O **SSH**. Copiamos la URL por **SSH** al comando `git remote` y damos **Enter**. Lo que ocurre es que se cambia la URL del **origen remoto** . Así que nos crea una nueva URL a la cual podemos hacer **fetch** y **push**.
3. Para visualizar estos cambios utilizamos el comando `git remote -v`. Mostrando la nueva URL por SSH para el origen remoto.
4. Para probar este cambio a SSH tenemos que hacer cambios al repositorio, entonces agregamos y comiteamos con`git commit -am "<mensaje>"`, traemos cambios del remoto `git pull origin master` y `git push origin master` enviamos los cambios al remoto. Y listo.
5. Para comprobar este envio recargamos GitHub en internet. Como pudiste observar no te pidio nombre de usuario y contraseña.

Ahora ya tengo conectado Git con GitHub, ya tengo funcionando SSH, mi vida es perfecta.

# Tags y versiones en Git y GitHub

Los tags nos permiten crear versiones para nuestro proyecto o categorizar que está listo, es decir, "Hasta aquí llego mi proyecto, esto es lo que voy a enviar". Son utiles en GitHub, en el sitio web, porque es la forma en que usuarios de código abierto u otras personas pueden ver qué versión ocurrió. Son rara vez útiles dentro del proyecto excepto si quieres dejar un registro "Aquí fue donde quede". En mas como referencia interna. Para crear un tag debemos:

1. Visualizar la historia de nuestros commits con el comando`git log --all --graph --decorate --oneline`, el cual nos permite visualizar la versión corta de nuestros commits y debemos decidir qué commit queremos etiquetar o versionar,  por ejemplo, este commit `69a09ec`.
2. Para crear el tag utilizamos el comando `git tag -a <nombre de la versión> -m "<mensaje>" <commit>`. Pudiendo verse de la siguente forma: **git tag -a v0.1 -m "Esta es la versión 0.1 del proyecto" 69a09ec**.
3. Para visualizar todos los tags creados utilizamos comando `git tag`. Para visualizar qué commit está asignado a tal tag utilizamos el comando `git show-ref --tags`.
4. Antes hacemos `git pull origin master` para traernos los camibos. Y por buenas practicas.
5. Para enviar el tag a GitHub utilizamos el comando `git push origin --tags`. Y listo.
6. Para visualizar estos cambios nos rigimos en GitHub a **Branches** y después a **Tags**. Y veremos el `<nombre de la versiión>`.

Si queremos **elimar un tag** de Git y GitHub **por X razón**, utilizamos dos comandos. Primero `git tag -d <nombre del tag>`, elimina el tag de respositorio local. Y segundo `git push origin :refs/tags/<nombre del tag>`, elimina el tag de GitHub. **Enter** y listo.

# Manejo de ramas en GitHub

En GitHub siempre vas a ver la rama **main**, anteriormente ***master***, la rama principal donde está la última versión, pero ¿qué pasa con las ramas de desarrollo? Normalmente hay una versión estable de tu software y luego empiezas a generar cambios que no estas seguro si agregar a la rama principal, o también puede que haya múltiples programadores trabajando en ramas distintas. Por ejemplo, para la creación de una página web, vamos a dividir el desarrollo de la cabecera o **header** en una rama y el desarrollo del pie de página o **footer** en otra rama.

Tu puedes tener ramas que nunca envies a tu respositorio en internet o a GitHub. Tu puedes tener ramas que siempre estes enviando. 

Para crear nuestras ramas de trabajo header y footer tenemos que movernos a nuestra rama principal **master**, porque es importante hacerlo desde la versión mas reciente. Estando aquí utilizamos el comando `git branch <nombre de la rama>`, es decir, **git branch header** y **git branch footer**. Con eso ya tengo los branches creados. Para comprobar que las ramas están creadas utilizamos el comando `git branch`. Para enviar las ramas a nuestro respositorio remoto utilizamos el comando `git push origin <nombre de la rama>`, es decir, **git push origin header** y **git push origin footer**.

# Configurar múltiples colaboradores en un repositorio de GitHub

Imagina que acabas de ser contratado para trabajar en un proyecto remoto. Así que estas muy emocionado por tu primer día de trabajo y empiezas a crear una **Nueva carpeta** en tu **HOME** llamada **collaborativeProjects** y dentro de este **Directorio** creas una **Nueva carpeta** llamada **Proyecto-Company-Name**. Entras a **Company-Name** y aquí vas a arrancar tu repositorio.

Pero hay una diferencia entre el resto y tú. Porque tú **NO** vas a hacer **git init**. Porque tu te quieres traer el repotorio. Entonces lo que deberás hacer es visitar el respotirio en GitHub. Estando en GitHub nos dirigimos a la pestaña  ***clone*** donde nos da la opción de ***Clone*** por **HTTPS** O **SSH**. Y copiamos la URL elegida.

Rcuerda una cosas es que tú puedas **clonar** y otra cosa es que tú puedas **enviar**.

¿Qué pasa cuándo queremos traernos un proyecto de otro lado? ¿Qué pasa cuándo no estamos arrancando desde cero, sino que alguien más ya creo el proyecto y tu te estas uniendo como un nuevo miembro de ese equipo?

Lo que pasa es que vas a tu directorio en local donde arrancarás o **clonarás** tu respositorio. Estando aquí utilizamos el comando `git clone <dirección del respositorio remoto en GitHub>`. Lo que pasa es que empezará a clonarlo. Y listo. Notaras que no te pide usuario ni contraseña, es porque el repositorio es un repositorio público. Al ser público simplemente lo puedo descargar como personas que navegan por el repositorio.

Para comprobar que el repositorio remoto fue clonado en mi entorno local damos `ls -al`. Y visualizamos el repositorio creado en su propio directorio. Con el mismo nombre que el del repositorio remoto. El es el nombre por defecto. Pero sin problemas también le puedo cambiar el nombre.

Ahora imaginemos que modificamos el proyecto. Y para guardar esos cambios hacemos un commit `git commit -am "<mensaje>"`. Porque el archivo ya fue creado y enviado anteriormente. Ahora para enviar esos cambios al respositorio remoto hacemos `git pull origin master`. De esta manera siempre nos traemos cambios si los hubo. Por buenas prácticas. Cabe mencionar que en nuestro repositorio local nos tragimos toda la **historia** del proyecto de solo la rama **master**. Y podemos visualizar todas las ramas que faltan agreagar con el comando `git log`, ya que ahora mi commit es el mas reciente. Por último hacemos `git push origin master`, porque es lo que hay que hacer.

Pero algo paso. **Unable to access**, **Permission denied**.

¿Y por qué paso ésto? porque en el proceso el el jefe no te dió acceso.

Para que tu jefe que es el dueño del respositorio te agregué. Debe ir a los **Settings** del respositorio. Después a **Manage access**. Hacer clic en **Invite a collaborator** y escribir tu username, full name, or email. Y por último clic en **Select a collaborator above**.

Lo que pasará es que te llegará un email de la empresa el cual te informará que te estan invitando a colaborar. Así que solo deberas **aceptar la invitación** si estas de acuerdo.

Ahora ya tienes permiso de hacer un `git push origin master`. Y listo tus cambios se han enviado exitosamente el respositorio remoto.

Tu jefe notará tus cambios en el repositorio remoto. Para qué el pueda tener esos cambios en su repositorio remoto tiene que hacer `git pull origin master`. Y listo.

Sin embargo, tu jefe tiene una charla contigo y te hace saber que los **cambios** se hacen en ramas. Así que te asigna una **rama de trabajo**. Y cuando todos los cambios esten listos tu jefe se encargará de hacer el **merge** para fusionar todos los cambios.

# Flujo de trabajo profesional

## Traerme una rama del repositorio remoto a mi repositorio local

Siguiendo con el ejemplo de que acabas de ser contratado para trabajar en un proyecto remoto

Recordemos que en nuestro repositorio local nos tragimos toda la **historia** del proyecto de solo la rama **master**. Para traernos la historia de otra rama así como posibles nuevos cambios o actualizaciones utilizamos el comando `git pull origin <nombre de la rama>`. Debiendo ejecutarse desde la rama **master** en nuestro **repositiro local**. Para comprobar que nos tragimos la rama utilizamos el comando `git branch`. Y listo.

Si agregamos cambios y queremos enviarlos de vuelta al respositorio remoto utilizamos el comando `git push origin <nombre de la rama>`. Recuerda que por buenas practicas siempre antes de hacer un **push** hay que hacer un **pull**.

## Hacer un merge en las ramas del proyecto

Tú jefe tiene el trabajo de fusionar las ramas. ¿Por qué? Porque es el jefe. Ya que verificó que los cambios están bien puede ir a continuación a la rama principal desde donde quiere hacer el merge. Es decir a la rama *master*. Desde la rama master tu jefe utiliza el comando `git merge <nombre de la rama que quiere fusionar>`. Y si todo salio bien, tu jefe agregará un mensaje para el merge. Y listo. 

## Pull requests

Es una funcionalidad de **github** (en **gitlab** llamada merge request y en **bitbucket** push request), en la que el dueño del respositorio o un colaborador te pide que revises sus cambios antes de hacer **merge** a la rama principal, normalmente **master**. Siguiendo con el ejemplo de que acabas de ser contratado para trabajar en un proyecto remoto.

En caso de que no trabajes para un proyecto remoto. Y solo seas un extraño que envia sus cambios al proyecto también se le conoce como Pull request.

Un Pull request también puedes crearlo tú mismo, siempre que seas **el dueño del repositorio**, una **rama experimental** aparte de la rama máster y tengas **colaboradores** en tu proyecto. Para ello de igual manera puedes pedirle a alguien que revise tus cambios y los apruebe, para que tú puedas hacer el merge. Y también puedes aceptar o rechazar Pull request personas extrañas al proyecto.

**En terminos simples** crear **un Pull request** es asignarle a alguien el trabajo de revisar los cambios y los apruebe. Y una vez revisados, **el owner** puede fusiona los cambios al **master**.

Flujo de trabajo de un Pull request:

1. Modificas la rama development o experimental, comiteas esos cambios y los envias al respositorio remoto.
2. Te diriges a GitHub. **GitHub** te crea **automaticamente** un Pull request entre la **rama development** y la **rama master**. Visualizandose en la **pestaña Pull requests**. Lo que hace GitHub es compara esos cambios y te dice que es posible fusionar esas ramas.
3. Sino queremos el Pull request automático podemos crearlo nosotros mismos. Para hacerlo nos dirigimos a nuestro repositorio y damos clic a **New pull resquest**. En este lugar elegimos para la rama ***base*** **master** y para la rama ***compare*** **development**. Es decir, tenemos una **rama principal** llamada master y una rama que queremos comparar, la **rama development**. GitHub te hará saber si las ramas se pueden fusionar automáticamente. Y damos clic a **Create pull request**.
4. Una vez creado me permite agregarle detalles, tales como el **nombre** del pull request el cual por defecto es el mensaje del commit, **Leave a coment** y **Reviewers** o personas que revisen los cambios entre estas ramas. Siendo estas tres las principales para GitHub como herramienta. También tenemos **Assigness**, para asignarle el Pull requets a alguien, **Labels** o etiquetas, **Projects** o agrupación de repositorios en GitHub y **Milestone** o un objetivo logrado y representado con este pull request. Estas otras opciones se vuelven útiles en el proceso de **DevOps** o **Developer Operations**. Es decir, una conexión eficiente entre los operadores con developers, de esta manera los equipos de trabajo alinean sus metas, mejoran su comunicación y aumentan la velocidad y los resultados. DevOps es una cambio en la cultura de la empresa que te permite automatizar y medir procesos. Damos clic nuevamente a **Create pull request**. Y listo.

Si es nuestro trabajo revisar los cambios para este pull request, entonces:

1. Nos dirigimos a la **pestaña Pull requests**. y elegimos el pull request que queremos revisar.
2. **Para la pestaña Conversation**. GitHub automáticamente te dice **quien** requiere tú revisión para este pull request. Te dice que **el dueño del respositorio quiere fusionar** 1 commit hacia el master de su rama development. Te permite ver su comentario para tí. Te avisa si la rama development tiene o no conflictos con la rama master. Podemos realizar una fusión creando un **Merge pull request** (Existiendo también, las opciones ***Squash and merge*** y ***Rebase and merge***, pero son malas practicas).
3. **Para la pestaña Commits**. Visualizamos todos los commits que pertenecen a los cambios. Pudiendo ser uno o una rama entera.
4. **Para la pestaña Files changed**. Visualizamos que archivos fueron cambiados o modificados.
5. **Para** decirle a la persona que no aceptas sus cabios nos dirigimos a **la pestaña Checks**. Damos clic en **Review changes**. Aquí puedo puedo agregar un comentario hacerca de por qué no acepto sus cambios y lo que debería de arreglar. Después, doy clic en **Request changes** para pedirle los cambios. Pero también lo puedo **Comment** o **Approve**. Si apruebo los cambios, como Reviewer que soy tendre una palomita de que he aprovado los cambios.
6. El merge o la fusión a master lo puede hacer culaquier colaborador del equipo. Sin embargo, siempre debe haber alguien que haga los merges y que se respete quíen los hace. Porque de lo contrario no existe este proceso de **Code Review**. Los cuales son una excelente práctica. Hacemos clic en **Mege pull request**, agregamos el mensaje y por último damos clic en **Confirm merge**. Se nos mostrará el mensaje **Pull request successfully merged and closed**. De manera opcional puedo borrar la rama haciendo clic en **Delete branch**. Esto es útil cuando no quiero llenarme de branches y cuando son ramas que no necesito porque son arreglos que tocaba hacer de última hora.


Los Pull request del lado de Git no existen, solamente existen los merges. Un Pull request es como una pausa justo antes de poder fusionarlo que te permite agregar cambios. Y ese Code Review siempre es la mejor de las ideas para hacer un trabajo completo.

## Pull requests cuándo no eres parte del proyecto

¿Qué pasa cuando no eres un colaborador del proyecto, cuando quieres aportar a Opensure, cuando eres un extraño que envia sus cambios al proyecto? Ahí es cuando los pull requests son aún mas importantes, porque tu no tienes poder de merge.

Aquí **lo que se hace es** clonar con algo llamado un **Fork** y luego hacer **Pull request** de una manera ligeramente distinta.

Vamos a intender cómo funciona un **proyecto OpenSource**. Es decir, cuando simplemente eres **una persona que le gusta el proyecto y quieres aportar para el**.
Cuando no eres un colaborador, significa que **no puedes hacer merges**, pudes clonar el proyecto, pero no puedes hacerle** push de ningún tipo** a un proyecto OpenSource. Porque no tienes permiso de push, ya no pudes **crear ramas y tags** en GitHub. **Lo máximo que puedes hacer es clonar o copia el proyecto**, porque es un proyecto público y abierto. Y decirles a los dueños y colaboradores del proyecto, ***quiero hacerle este cambio por favor fusionenlos***.

Los pasos para poder colaborar en el proyecto OpenSource:

1. Ubicarme en el repositorio al cual quiero aportar.
2. Si me gusta puedo darle **Watch**. De esta manera me llegarán notificaciones en el momento en el que cambien cosas.
3. También puedo darle una **Start**. De esta forma indico que el proyecto me gusta. Entonces me llegarán avisos de cuando las cosas cambien el en proyecto.
4. También puedo hacerle un **Fork**. Hacer un Fork es tomar una copia del estado actual del proyecto y clonarlo. Y de esta forma lo clono como un proyecto mío. Esto solo se puede hacer con proyectos públicos. Y es una característica única de GitHub. Así que le doy clic a **Fork**.
5. Para poder hacer cambios, necesito traermelo a mi entorno local. Para hacerlo me ubico en un directorio o carpeta culaquiera en mi entorno local. Y ejectuo el comando `git clone <dirección del respositorio remoto en GitHub>`. Como es un repositorio público no me pide nombre de usuario y contraseña. Para agregar la `<dirección del respositorio remoto en GitHub>` utilizamos la pestaña Code en GitHub donde nos da la opción de Clone por HTTPS O SSH. Copiamos la URL por SSH al comando git clone y damos Enter. Lo que ocurre es que se agrega un origen remoto al cual podemos hacer fetch y push. Además de nos crear un directorio con el nombrel del proyecto y dentro del directorio podemos visualizar todos los archivos que son parte del proyeto.
6. Ahora puedo hacer algún cambio, agregarlo y comitearlo. Si mi historia es más fuerte, me dira **Your branch is ahead of 'origin/master' by 1 commit**.
7. Para enviar esos cambios al remoto utilizo el comando `git push origin master`. Y puedo comprobar esos cambios al recargar el repositorio en GitHub.
7. Para poder **crear** el Pull request, hacemos clin en **New pull ruequest**. A continuación GitHub nos da a elegir dos ramas para comparar sus cambios. Pero también nos da la opción de comparar los diferentes forks **compare across forks**. De esta manera GitHub me mostrará los cambios entre master del repositorio que forkie y el master del repositorio original. Aquí puedo **Unified** o **Split** los cambios.
8. Ahora que tenemos claro cuales fueron los cambios. Damos clic en **Create pull request**. Siempre y cuando **This branch has no conflicts with the base branch** o rama original. Hay que recordar que el pull request es como un commit intermedio, por lo que tenemos que agregar un mensaje. GitHub utiliza por defecto el **mensaje** del commit como **Title** en el pull request y de manera opcional podemos **Leave a comment**. Y por útlimo vuelvo a dar clic en **Create pull request**. Y listo.
8. Ahora podras segir la **Conversation** en la pestaña Pull request del repositorio remoto original. Si quiero cancelar mi pull request puedo dar clic en **Close pull request** o puedo seguir comentando y esperar. Porque ya no puedo hacer nada más.

Si en el proyecto o repositorio original se hacen cambios yo como tengo un fork de ese repositoro voy a tener que traerme esos cambios en mi propio fork. A medida que el original va cambiando el fork se va quedando atras, y si quiero mantenerme trabajando a la par voy a tener que traerme los cambios.

Para mantener actualizado mi fork del proyecto, tengo que:

1. Me dirigo a mi fork del proyecto en GitHub, donde podre observar por cuantos commits estoy atras del original.
2. Ahora puedo **Compare** para ver esos cambios. Al comparar me dice que no hay nada que comparar porque compara de mi rama fork a la rama base. Puedo cambiar el orden o hacer clic en Try **switching the base** for your comparison. Ahora si puedo ver lo que cambios.
3. Los cambios se pueden traer de dos maneras desde **GitHub** o desde la **Console**. Para traer los cambios desde consola necesitamos crear otro origin remoto para hacer pull y trernos los cambios. Para hacerlo me situo en el directorio del respositorio o proyecto en local. Y aquí puedo comprobar cuantos origenes remotos tengo con el comando `git remote -v`. Ahora para crear el nuevo origin remoto utilizo el comando `git remote add upstream <dirección del respositorio remoto en GitHub>`. Para agregar la `<dirección del respositorio remoto en GitHub>`, nos dirigimos al repositorio original y utilizamos la pestaña Code en GitHub donde nos da la opción de Clone por HTTPS O SSH. Copiamos la URL por SSH al comando git clone y damos Enter. Lo que ocurre es que se agrega el origen remoto llamado **upstream**, al cual podemos hacer fetch y push. Para coprobar que el nuevo origen remoto fue agregado utilizamo nuevamente el comando `git remote -v`. Por último para traernos las actualizaciones del respositorio original utilizamos el comando `git pull uptream master`. Y Enter. Al hacer esto nos traemos todos los cambios de master y nuestro respositorio local esta actualizado,  comprobamos estos cambios con el comando `git status`. Para actualizar el respositorio remoto hacemos un `git push origin master`. Y listo ahora nuestro fork en GitHub esta actualizado a la par con el respositorio original.
5. La otra forma es al reves, es hacerlo directamente desde GitHub.

Ambas opciones son 100% validas, ambas opciones se pueden hacer depende de ti.

# Ignorar archivos en el repositorio con .gitignore

No todos los archivos que tu agregas a un proyecto deberían ir en un repositorio. Por ejemplo, cuando tienes un archivo donde están tus contraseñas, cuando te conectas a una base de datos, eso tiene que ir en un archivo aparte que no puede ser parte de ti repositorio. ¿Por qué? Porque alguíen más lo puede ver. Sobre todos en proyectos OpenSources. Teniendo en mente eso, Git tiene algo que se llama **Gitignore**.

Una buena práctica es evitar que los archivos binarios o imágenes sean parte del repostirio. Entonces hay que ignorarlos.

Para ignorar archivos creamos un archivo en el diretorio de nuestro proyecto, junto con los archivos del respositorio y el repositorio. Debiendo llamarse **.gitignore**. Lo creamos con el siguiente comando `touch .gitignore` o creandolo desde algún editor de código y guardando como ***.gitignore***. Gitignore es una lista de los archivos que vamos a ignorar. La sintaxis para **ignorar el 100% de archivos .jpg** es la siguiente:

```
*.jpg
```

**Guardamos** estos cambios, **hacemos** `git add`, `git commit -m "<mensaje>"`, `git pull origin master` y `git push origin master`. Y listo, tenemos **.gitignore** en nuestro **respositorio remoto**. Lo que pasa es que en nuestro respositorio remoto la imágen .jpg no está, no se subio porque fue ignorada, a pesar de que si está en mi entorno local. Para subir la imágen debemos hacer uso de algún lugar externo, por ejemplo, en: [https://imgur.com/](https://imgur.com/), puedes subir gratis imágenes y georrefernciarlas desde ahí. porque los binarios no deberían ir en los repositorios remotos.

```
# Ignorar directorios, archivos y anidados

directorio
archivo.extesión
directorio/archivo.extensión
directorio1/directorio2
directorio1/directorio2/*.extensión


# No ignorar o aplicar excepciones

!/archivo.extensión
!/directorio1/directorio2/archivo.extensión
```

Impirarte en proyecto OpenSources no es solo lo correcto, es la forma en la que todo el mundo aprende en la industria del Software.

# README.md es una excelente práctica

README.md es una excelente práctica en tus proyectos. ***md*** significa Markdown. Es una espeice de código que te permite cambiar ligeramente la forma en la que se ve un archivo de texto.

La forma de aprende README.md es inspirarnos de proyectos OpenSources. README.md existe porque nosotros queremos contarle al mundo de qué es un repositorio.

Para editar nuestro README.md podemos abrir el archivo en algún editor de código o podemos usar algún editor online como: [https://pandao.github.io/editor.md/en.html](https://pandao.github.io/editor.md/en.html).

# Tu sitio web público con GitHub Pages

GitHub tiene un servicio de hosting gratis llamado GitHub Pages, tu puedes tener un repositorio donde el contenido del repositorio se vaya a GitHub y se vea online.

Para crear sitios web para ti y tus proyectos, alojado directamente desde su repositorio de GitHub, puede visitar la página oficial: [https://pages.github.com/](https://pages.github.com/) o seguir los pasos a continuación.

NOTA: Obtienes un sitio por cada cuenta y organización de GitHub, y sitios de proyectos ilimitados. Empecemos.

1. Si ya estas listo para empezar, dirígete a **GitHub** y crea un **nuevo repositorio público llamado username.github.io**, donde username es tu nombre de usuario (o el nombre de la organización) en GitHub. ***Si la primera parte del repositorio no coincide exactamente con su nombre de usuario, no funcionará, así que asegúrese de hacerlo bien.***
![](https://pages.github.com/images/user-repo@2x.png)

2. ¿Qué cliente de git estás usando? Una terminal.

3. Clonar el repositorio. Vaya a la carpeta donde desea almacenar su proyecto y clone el nuevo repositorio por HTTPS:
`git clone https://github.com/username/username.github.io` o por SSH: `git@github.com:username/username.github.io`
![](https://pages.github.com/images/setup-in-desktop@2x.png)

4. Hello World. Ingrese a la carpeta del proyecto y agregue un archivo index.html:
`cd username.github.io`
`echo "Hello World" > index.html`
5. Push it. Agregue, comitea, traiga y envíe sus cambios:
`git add --all`
`git commit -m "Initial commit"`
`git pull -u origin master`
`git push -u origin master`
6. …¡y tu estas listo!. Inicie un navegador y vaya a https://username.github.io.
7. Si la url no funciona deberas ir primero a los Setting del repositorio: 
![](https://pages.github.com/images/repo-settings@2x.png) 
y después al opción **GitHub Pages**, donde en **Source** seleccionaremos la rama **master** para GitHub Pages. Y listo: ![](https://pages.github.com/images/source-setting@2x.png)

Para crear **sitios web para tus proyectos** solo deberas **repetir los pasos 4** al **7**. Debiendo tener un **index.html** como tu archivo principal.

# Git Rebase: reorganizando el trabajo realizado

En un flujo normal de trabajo, tenemos nuestro master de toda la vida, y supongamos que en un punto, me di cuenta que cometí un error. Entonces hago una neuva rama que se llama **bugfix** y en esa nueva rama empiezo a arreglar el bug. Y eventualmente caundo ya estoy listo realizo un merge. Ese merge fusiono lo que había he bugfinx lo que había en master, continuo con mi vida y esa rama sigue existiendo. ¿Pero que pasa cuando quiero que la rama se agregué a la historia del master?¿Qué pasa si lo que yo quiero no es hacer un merge, sino hacer como si no paso nada? Lo que quiero es borrar la rama bugfix y pegar todos los cambios que hice a la historia del master. Y una vez pegados esos cambios no le digo a nadie y es como si no hubiera pasado nada. Para poder hacer eso necesito hacer un **rebase**.

***Rebase es solo para respositorios locales***, porque rebase reescribe la historia del repositorio.

***Rebase es una muy mala práctica enviandola a repositorios remotos***, porque en general la historia en los repositorios remotos debería mantenrse intacta.

Funciona en ciertos casos, usa tu criterio, pregunta a tus compañeros de trabajo, pero ***ten mucho cuidado la hacer resbase***. Pero los errores pasan y hay que aprende a solucionarlos.

Para hacer un rebase:

1. Creamos una rama experimental, por ejemplo, la rama bugfix. Arreglamos y  agregando los cambios necesarios a esta rama. Y la rama master puede cambiar o manterse sin cambios. 
2. Una vez que estamos listos. Nos aseguramos de estar en la rama experimental y desde aquí utilizamos el comando `git rebase master`. De esta manera pegamos la historia de la rama experimental a la historia del master. Si la rama master no fue modificada se nos mostrará el siguiente mensaje: `current branch <rama experimantal> is up to date`. Si la rama master fue modificada y hacemos un `git rebase master`se nos mostrarán los siguientes mensajes: 
`First, rewinding head to replay your work on top of it...`
`Applyin: <mensaje>`
`Using index info to reconstruct a base tree...`
`M  archivo.extensión`
`Falling back to patching base and <número>-way merge`
`Auto-merging archivo.extensión`. De esta manera me pega y autofusiona todos los cambios de master con la rama experimental. Cual se el caso, lo que pasa es que la historia ya no es que la rama experimental arranco un commit atras, sino que la rama experimantel arranco un commit adealnte. Cambia la historia de donde arranco el branch.
3. Ahora para traerme la historia al master, desde la rama master utilizo el comando `git rebase <rama experimental>`. Este siempre es el orden, primero se la hace el rebase a la rama voy a desaparecer de la historia y después se la hace rebase a la rama principal. De lo contrario podríamos entrar un un conflicto que solo podría arreglarse con `git reset`. Al ejecutarlo nos muestra lo siguiente: 
`First, rewinding head to replay your work on top of it...`
`Fast-forwarded master to <rama experiental>`.
Ahora ya tengo todo en la rama master. Y el HEAD le apunta a la rama master y experimental.
4. Ahora podemos enviar estos cambios al repositorio remoto, haciendo pull y push. Y cuando visualizamos la historia, podemos observar que todo paso en master, la rama experimental no existe.
5. Por último puedo eliminar la rama experimental utilizando el comando `git branch -D <rama experimantal>`. Y listo. Si visualizamos con git log, la rama desaparecio de la historia en local.

# Git Stash: Guardar cambios en memoria y recuperarlos.

Hay un escenario que no hemos plateado, y es el escenario donde yo estoy en la **branch master** y quiero hacer unas modificaciones, pero tengo que irme a una **rama anterior**, pero no quiero todavía hacerle **commit a esas modificaciones**, pero las quiero **guardar en un lugar**. Esto se hace con el comando ``git stash``.

Supongamos que por error borramos o modificamos algo en nuestro proyecto que no queriamos o que al final no nos gusto y damos ``Control + S``. Entonces, para saber que tenía antes puedo cambiar a la rama donde todo estaba bien, pero si doy `git checkout` me saldrá un **error** porque tengo este cambio, pero este cambio aún no estoy listo para comitearlo. Entonces aquí es donde es útil el comando ``git stash``. Lo que ocurre es que me vuelve al estado anterior, porque ahora tengo guardado los cambios que hice en un lugar temporal, este lugar temporal lo puedo visualizar con el comando ``git stash list``. Me muestra que tengo un ``stash(0): WIP (Work In Progress) on master: last commit``. Ahora puedo hacer ``git checkout`` e ir a la rama donde todo estaba bien. Ahora debo quitar el Stash, pero no estando en la rama donde todo esta bien, sino que debo ir de vuelta a la rama master donde todo paso, y utilizar el comando ``git stash pop``.  De esta manera abro el Stash que tenía y si esos cambios no me gustan utilizo ``Control + Z`` y vuelvo a mi estado normal porque como no mofique nada, no pasó nada.

Otra cosa que puedo hace interesante es **guardar mis cambios** y ponerlos **en una rama**. Supongamos que modifico algo en mi proyecto, guardo con ``Control + S`` y utilizo el comando ``git stash``. Mostrandonos el mensaje: ``Saved working directory and index state WIP on master: last commit``. Para visualizar mi Stash utilizo el comando ``git stash list``. Ahora para poner este Stash en una rama nueva utilizo el siguiente comando: ``git stash branch <nombre de la rama>``. Esto me crea la rama. Puedo comprobarlo con el comando ``git branch`` para visualizar la rama. Ahora estando en la rama creada guardo con un commit. Y puedo volver de nuevo a la rama master sin ningún problema, desaparenciendo además el Stash hecho anteriomente.

Por último que pasa cuando tengo un  Stash pero relamente no lo quiero guardar. Supongamos que arruinamos todo en más de un archivo, entonces guardo esto con ``git stash``, esto me devolvera a mi último commit. De esta manera todo se arreglo solito, todo es maravilloso. Si visualizo el Stash con ``git stash list`` ahí esta. Ahora lo que quiero es borrarlo entonces utilizo el comando ``git stash drop`` y listo, ya no existe y todo vuelve como antes.

Git Stash es tipico cuando estas haciendo pequeños experimentos que no merecen una rama o que no merecen un Rebase, sino que simplemente estas probando algo y luego quieres volver rapidamente a tu versión anterior la que es la correcta, la del último commit. Otro ejemplo tipico de Stash es cuando llevas mucho trabajo adelantado y se te olvido hacer commit y necesitas datos de otra rama, entonces puedes hacer ``git stash`` y luego un checkout hacia la otra rama.

Este es un comando extremadamente popular en equipos de trabajo con proyectos complejos. A medida que tus proyecto se haga más y más grande, y más y más complejos vas a necesiar el comando ``git stash``.

# Git Clean: limpiar tu proyecto de archivos no deseados.

A veces creas archivos mientras estas desarroyando tu proyectos que realmente no son parte de tu directorio de trabajo, que no deberías agregar, y que tú lo sabes, archivos como: .logs, archivos como el resultado de una compilación o por ejemplo, imágenes que te quedarón por ahí sueltas.

Imagina que por error creas un montón de copias de tus archivos de tu directorio de trabajo, entonces tienes muchos archivos que por error terminaste creando. Si ahora ejecuto ``git status`` veo todos los archivos creados que son un error. Git sabe cual es la estructura de tu directorio de trabajo. Si tu tienes archivos que no has agregado, y en vez de agregarlos los quieres quitar o borrar, entonces usas el comando **git clean**. Para saber cuales archivos se van a borrar usas el comando ``git clean --dry-run``, y después de comprobar que son los archivos que quieres borrar, utilizas el comando ``git clean -f``. Lo que pasa es que se borran todos los archivos que te mostro el comando ``git clean --dry-run``. Si volvemos a dar ``git status`` podemos ver que hay archivos que no borró, como los directorios, proque a Git no le importan las carpetas, a Git le importan los archivos. Desde la perspectiva de Git este archivo todavía esta siendo trackeado, por ende esta es una carpeta que tengo que borrar a mano. Otros archivos que no borró son los archivos especificados en tú **.gitignore**, por ejemplo todos los ``.jpg``, estos son ignorados para todo lo que tenga que ver con Git, incluyendo borrarlos de Git.

De esta manera tu puedes estar con la seguridad que sin ningún problema las imágenes que tu agregues aunque no esten siendo traqueadas no van a ser borradas por Git Clean. Git Clean solamente borra las cosas que puede indexar.

# Git cherry-pick: traer commits viejos al head de un branch.

Existe un mundo alternativo, donde tu vas avanzando en una rama, pero necesitas en master uno de esos avances de la rama. Para ellos se usa un comando llamado **cherry-pick**.

Supongamos que trabajamos en la rama development, dejando atras al master por varios commits, pero aún no listo para unir a la rama master. De repente puede que alguien del equipo o tú jefe, llengo a la **rama master** te diga que necesita en esta rama, cieto código que vió en la rama development. Te das cuenta que ese código esta en una rama que no has terminado todavía, y que tú jefe solo te esta pidíendo una línea de código, porque lo demas no le importa.

Lo que hacemos es dirigirnos a la **rama master** y utilizo el comando **git cherry-pick**, y ahí me traigo solo el commit que tiene ese código. Para encontrar ese commit me dirijo a la rama development, utilizo el comando ``git log`` y *copy* ese commit. Entonces volviendo de nuevo al master utilizo el comando ``git cherry-pick <commit>``. Lo que pasa es que me traigo al master un commit que quería de otra rama. Al comprobar con ``git status`` veo que no se modificó nada, porque es un commit que ya existía el que se pego.

Si después de un tiempo tengo lista la rama development y quiero unir mis cambios con la rama master, entonces utilizo el comando **git merge** desde la rama master. Pero como habrá un línea que es igual en ambos ya que me traje esa línea anteriomente ocurrirá un conflicto, resolviendolo al elegir cual línea de código se queda o se va, apoyandonos de Visual Studio Code. Entonces guardo, agrego y comiteo esos cambios.

**Cherry-pick es una mala practica**. Porque significa que estas reconstruyendo la historia. Es mucho mejor que hagas el trabajo duro y lo hagas con un **merge**, hagas un checkout para tratar de ver como quedo y luego vulevas a hacer checkout al HEAD. Sin embargo, cherry-pick funciona para lo que quieras, lo puedes hacer para cambiar el HEAD del master, el HEAD de otra rama, cherry-pick funciona donde tu quieras.

USA CHERRY-PICK CON SABIDURIA, SINO SABES LO QUE ESTAS HACIENDO TEN MUCHO, MUCHO, MUCHO CUIDADO. Aunque recuerda que en Git cualquier error se puede recuperar, porque nunca nada se borra en Git. Esas es la magía de Git.

# Reconstruir commits en Git con amend.

A veces, haces un commit y resulta que realmente no querías mandar ese commit porque te faltaba algo más.

Supongamos que modificas un archivo, guardar y comiteas, pero te das cuenta de que te falto modificar otra cosa. Entonces modificas lo que te falto, agreas con ``git add .``, y ahora utilizo el comando ``git commit --amend``. AMEND en inglés significa ENMENDAR, lo que hace este comando, es que, lo cambios que hice me los va a pegar al commit anterior, al que acabo de hacer, no va a hacer un commit nuevo. Damos ENTER, y a continuación me abre VIM, donde puedo cambiar el mensaje del commit anterior. Guardo y salgo. Al hacer **git log**, podemos ver que estos cambios se pegaron al commit anterior, pudiendo haber modificado el mensaje de ese commit.

Como si nada paso, nadie sabe nada, así se enmendan los commits.

# Git Reset y Reflog: úsese en caso de emergencia.

Qué pasa cuando todo, todo se va al carajo, que pasa cuando todo se rompe y uno no sabe lo que esta pasando y quiere llorar.

Simulemos que por accidente en la rama master rompes o arruinas tu código porque estabas muy cansado y no sabías lo que hacías, y te das cuenta de todo al día siguiente. Entonces si yo voy en estos momentos a **git log** puedo ver todos mis errores y todas las cosas locas que hice. Así que yo quiero volver al lugar correcto, donde todo estaba bien, entonces ejecutamos el comando ``git reflog``. En **git reflog** se ve todo, aquí encontraremos tando el *commit acortado o hash*, como algo que se llama ``HEAD@{0}``. Estos son los HEADS que se han ido muriendo a traves del tiempo. Entonces lo que tu haces es buscar el último commit donde todo era correcto y **COPY**. Te relajas, compruebas que estas en la rama master, y utilizamos ya sea el comando ``git reset --SOFT`` o ``git reset --HARD``. La diferencia es que, SOFT te mantiene lo que sea que tengas en STAGING en STAGING, lo que le hayas dado **git add**, y HARD te resetea todo, en un entorno de programación profesional cuando llegan opción en general se utiliza HARD. Una vez que encontramos el commit o hash al que queremos volver utilizamos el comando HARD de la siguiente manera: ``git reset ---HARD <commit o hash>``. Al ejecutarlo todo volvio a la normalidad. Los commits indeseados desaparecieron, al igual que los errores en mi código, todo esta perfecto, como si no hubiera pasado nada.

En general **es una mala practica**, porque resetea toda la historia de tus commits. No deberías usar este comando sino hasta cuando algo realmente se rompio.

Puede que te este limpiando la historia, pero no la historia completa, **git reflog** tiene la verdad.