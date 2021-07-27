# Git y GitHub

## ¿Qué es Git y GitHub?
<p p style="text-align: justify">La premisa es simple, en vez de guardar una versión de cada archivo, hay un sistema que gurda solo esos cambios. Ademas maneja el cambio que otras pesonas hagan sobre los mismos archivos, asi multiples pesonas pueden trabajar en un mismo proyecto sin pisarse. Cuando hay errores se puede saber precisamente quien hizo ese cambio. Si hay algo en una versión vieja que quieres recuperar lo puedes hacer de manera precisa.</p>

<p p style="text-align: justify">En tu maquina local usas Git, funciona en la terminal o linea de comandos, y tiene comandos como: `$ merge`, `$ pull`, `$ add`, `$ commit` y muchos más.</p>

<p p style="text-align: justify">Si quieres colaborar con otros, usar una interfa web o publicar tus proyectos en la web usas GitHub. Es un sistema como facebook o twitter que gurda tu proyecto, sus cambios y cada una de sus versiones.</p>

<p p style="text-align: justify">GitHub es tan popular que es la red social de código. Una hoja de vida que demuestra lo que sabes.</p>

<p p style="text-align: justify">No te limites a solo hacer `$ add`, `$ commit`, `$ pull`, `$ push` porque estarías desaprovechando el increíble poder de Git. Git tiene ramas, tags, remotos, colaboradores, fusiones y mucho más.</p>

<p p style="text-align: justify">Git no es solo para programadores e ingenieros. Lo que sea que hagas que tenga versiones se puede poner en Git como un proyecto colaborativo.</p>

### Ejemplo de un archivo de texto de toda la vida:

| Versión  | Contenido | Extensión |
|:------------:|:---------------:|:-----:|
| 1  | <p style="text-align: justify">Mi nombre es Heriberto Cartas. Soy estudiante de Ingeniería Forestal y en mis tiempos libres corro carreras, mecanografio libros y hago cosas raras con python.</p> | biografía.txt |
| 2 | <p style="text-align: justify">Mi nombre es Heriberto Cartas. Soy egresado de Ingeniería Forestal y en mis tiempos libres derribo árboles, mecanografio libros y hago cosas raras con R.</p> | biografia_v2.txt |

| Versión  | Cambios | Extensión |
|:------------:|:---------------:|:-----:|
| 1  | <p style="text-align: justify">Mi nombre es Heriberto Cartas. Soy ~~**estudiante**~~ de Ingeniería Forestal y en mis tiempos libres ~~**corro carreras**~~, mecanografio libros y hago cosas raras con ~~**python**~~.</p> | biografía.txt |
| 2 | <p style="text-align: justify">Mi nombre es Heriberto Cartas. Soy **egresado** de Ingeniería Forestal y en mis tiempos libres **derribo árboles**, mecanografio libros y hago cosas raras con **R**.</p> | biografia_v2.txt |

## Comandos

### Inicializar un repositorio

`$ git init`