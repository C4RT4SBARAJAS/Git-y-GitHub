# Git y GitHub

## ¿Qué es Git y GitHub?
La premisa es simple, en vez de guardar una versión de cada archivo, hay un sistema que gurda solo esos cambios. Ademas maneja el cambio que otras pesonas hagan sobre los mismos archivos, asi multiples pesonas pueden trabajar en un mismo proyecto sin pisarse. Cuando hay errores se puede saber precisamente quien hizo ese cambio. Si hay algo en una versión vieja que quieres recuperar lo puedes hacer de manera precisa.

En tu maquina local usas Git, funciona en la terminal o linea de comandos, y tiene comandos como: `$ merge`, `$ pull`, `$ add`, `$ commit` y muchos más.

Si quieres colaborar con otros, usar una interfa web o publicar tus proyectos en la web usas GitHub. Es un sistema como facebook o twitter que gurda tu proyecto, sus cambios y cada una de sus versiones.

GitHub es tan popular que es la red social de código. Una hoja de vida que demuestra lo que sabes.

No te limites a solo hacer `$ add`, `$ commit`, `$ pull`, `$ push` porque estarías desaprovechando el increíble poder de Git. Git tiene ramas, tags, remotos, colaboradores, fusiones y mucho más.

Git no es solo para programadores e ingenieros. Lo que sea que hagas que tenga versiones se puede poner en Git como un proyecto colaborativo.

### Ejemplo de un archivo de texto de toda la vida:

| Versión  | Contenido | Extensión |
|:------------|:---------------|:-----|
| 1  | Mi nombre es Heriberto Cartas. Soy estudiante de Ingeniería Forestal y en mis tiempos libres corro carreras, mecanografio libros y hago cosas raras con python. | biografía.txt |
| 2 | Mi nombre es Heriberto Cartas. Soy egresado de Ingeniería Forestal y en mis tiempos libres derribo árboles, mecanografio libros y hago cosas raras con R. | biografia_v2.txt |

| Versión  | Cambios | Extensión |
|:------------|:---------------|:-----|
| 1  | Mi nombre es Heriberto Cartas. Soy ~~**estudiante**~~ de Ingeniería Forestal y en mis tiempos libres ~~**corro carreras**~~, mecanografio libros y hago cosas raras con ~~**python**~~. | biografía.txt |
| 2 | Mi nombre es Heriberto Cartas. Soy **egresado** de Ingeniería Forestal y en mis tiempos libres **derribo árboles**, mecanografio libros y hago cosas raras con **R**. | biografia_v2.txt |

## Comandos

### Inicializar un repositorio

`$ git init`