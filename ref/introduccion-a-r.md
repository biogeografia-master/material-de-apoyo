
<!-- Este .md fue generado a partir del .Rmd homónimo. Edítese el .Rmd -->
Introducción a R. Guión de referencia
=====================================

Introducción
------------

Te paso a continuación algunas fuentes (mayoritariamente en español) sobre las aplicaciones que manejarás y otros recursos.

-   Sobre [R](https://www.r-project.org/)
    -   [Vídeo corto sobre la historia de R](https://es.coursera.org/lecture/intro-data-science-programacion-estadistica-r/historia-e-introduccion-a-r-alNk0), donde podrás aprender algunas las características de R y el software libre en general, ventajas y desventajas de R, así como algunas aplicaciones.
    -   [Libro R4DS, R for Data Science](https://r4ds.had.co.nz/), una fuente muy completa realizada principalmente por Wickham & Grolemund (2017), con apoyo de la comunidad R. [Fue traducido recientemente a español](https://es.r4ds.hadley.nz/) por la comunidad R hispanohablante. Es un buen punto de partida. La organización del libro, que priorice el aparato gráfico sobre la parte programática, ayudan a mantener la motivación en el aprendizaje de R. Seguiré este esquema, pero usando datos ecológicos, tanto para las asignaciones, como para este guión de referencia.
    -   [Esta web](https://oscarperpinan.github.io/R/) es bastante completa, y es a la vez un buen lugar de referencia.
    -   [Este libro](https://cran.r-project.org/doc/contrib/rdebuts_es.pdf) está organizado con enfoque de programación, todo un clásico.
    -   La existencia de una diversa y activa comunidad R, motiva a muchos/as usuarios/as a usar este entorno de programación. [Abajo](#twitter) coloqué algunas cuentas de Twitter donde podrás observar en vivo una mínima parte de la actividad de la comunidad R. Hay muchas otras cuentas, foros, sitios web e incluso reuniones periódicas donde podrás interactuar con la comunidad. Te animo a descubrirlas.
    -   [RStudio](https://www.rstudio.com/). Tanto la página de Wikipedia como [este vídeo](https://www.youtube.com/watch?v=5XeFFoTf2IY) explican muy bien en qué consiste este entorno de desarrollo integrado, además de que hace una breve introducción a qué es R.
-   [Git](https://git-scm.com/). Bueno, esta es una larga historia, que parece estar bien resumida en [Wikipedia](https://es.wikipedia.org/wiki/Git). Busca en YouTube, y verás otros aportes.
-   [GitHub](https://github.com/). Se erige como un servicio público para desarrolladores y desarrolladoras. Luce bien explicado [aquí](https://www.deustoformacion.com/blog/programacion-diseno-web/que-es-para-que-sirve-github).
-   [GitHub Classroom](https://github.com/education/classroom%5D). En [esta web](https://www.genbeta.com/desarrollo/classroom-for-github-ayudando-a-los-profesores-a-gestionar-los-ejercicios-de-sus-clases) te explican para qué sirve. Con este servicio estoy asignándote trabajo. También te recomiendo que leas [ésta afirmación](https://github.com/education/classroom#who-is-classroom-for).
-   Foros de ayuda y listas de distribución, entre los que destacan [R-help](https://stat.ethz.ch/mailman/listinfo/r-help), [R-devel](https://stat.ethz.ch/mailman/listinfo/r-devel), [Stackoverflow](https://stackoverflow.com/). Las preguntas deben plantearse con un ejemplo reproducible. Si vas a plantear una, lee antes las guías de publicación. Existe una [lista de distribución de R-help en español](https://stat.ethz.ch/mailman/listinfo/r-help-es), así como de [Stackoverflow en español](https://es.stackoverflow.com/).
-   <a name="twitter"></a>Twitter:
    -   [The R Foundation](https://twitter.com/_r_foundation)
    -   [RStudio](https://twitter.com/rstudio)
    -   [RLadies](https://twitter.com/RLadiesGlobal)
    -   [We Are R-Ladies](https://twitter.com/WeAreRLadies)
    -   [Comunidad R Hispano](https://twitter.com/r_hisp?lang=es)
    -   [Hadley Wickham](https://twitter.com/hadleywickham)
    -   [Gabriela de Queiroz](https://twitter.com/gdequeiroz)
    -   [R Consortium](https://twitter.com/rconsortium)
    -   [UseR! 2020](https://twitter.com/useR2020stl)
    -   [UseR! 2019](https://twitter.com/UseR2019_Conf)
    -   [Rstats](https://twitter.com/rstatstweet)

Instalación y ejecución de R y RStudio
--------------------------------------

-   Puedes usar el servidor RStudio habilitado por el profesor. Habrás recibido un correo electrónico con los detalles de acceso.

-   Si prefieres trabajar en tu propia PC, instala R y RStudio. La guía de instalación varía mucho según el sistema operativo:
    -   [R](https://cloud.r-project.org/)
    -   [RStudio](https://www.rstudio.com/products/rstudio/download/#download)
-   Igualmente, la forma de ejecutar estas aplicaciones dependerá del sistema operativo.
    -   En GNU/Linux es posible ejecutar tanto aplicaciones tanto desde el gestor de ventanas como desde el intérprete de línea de órdenes (CLI) o "terminal" (por ejemplo, para ejecutar R, presiona `CRTL+ALT+T`, escribe `R` y presiona `<enter>`).
    -   En Windows y MacOS la ejecución se realiza desde el GUI.

CRAN (Comprehensive R Archive Network)
--------------------------------------

-   [¿Qué es CRAN?](https://cran.r-project.org/doc/FAQ/R-FAQ.html#What-is-CRAN_003f)
-   Instalar paquetes: Ejemplo: `install.packages('vegan', dependencies = T)`. Si realizas tus asignaciones en el servidor RStudio habilitado por el profesor, no necesitarás instalar paquetes.

Ayuda de R
----------

``` r
help(package = 'base') #Ayuda sobre un paquete
library(help = 'base') #Documentación sobre un paquete
help(lm) #Ayuda sobre una función
?lm #Ídem
example(lm) #Ejemplo(s) sobre una función
help.search("matrix") #Busca la palabra clave en las ayudas de los paquetes
??matrix #Ídem
```

¡Usa los foros! Si introduces un mensaje de error de R en un buscador (el mensaje en inglés devuelve más resultados), encontrarás varias entradas de foros con posibles soluciones.

Visualización de datos
----------------------

Wickham & Grolemund (2017) afirman que, durante la producción de resultados comunicables, subyace la necesidad de realizar el análisis exploratorio de datos (AED o EDA) lo más rápidamente posible. El esquema a continuación, de la misma fuente, resume este proceso:

<img src="https://es.r4ds.hadley.nz/diagrams_w_text_as_path/es/data-science-explore.svg" width="65%" />

Las múltiples herramientas ofrecidas por los paquetes de la colección `tidyverse` te servirán para agilizar sustancialmente el EDA. Los paquetes `dplyr`, `tidyr` y otros, te ayudarán a importar, ordenar y transformar datos, mientras `ggplot2` te ayudará a crear gráficos estilizados eficientemente. Wickham & Grolemund (2017) aseguran que estas herramientas mantienen la motivación en el aprendizaje por sus flujos de trabajo lineales.

Usemos el conjunto de datos `doubs`, del paquete `ade4`, que son además los utilizados en el libro de Borcard, Gillet, & Legendre (2018).

<!-- ## Directorio de trabajo -->
<!-- * Para consultar tu directorio de trabajo en R: `getwd()`. -->
<!-- * Si usas el servidor RStudio habilitado por el profesor, la ruta por defecto será algo parecido a ésto: `'/home/<tunombredeusuario>'`. Esta ruta se denomina "carpeta personal". -->
<!-- * Puedes cambiar tu directorio de trabajo mediante `setwd('<rutademipreferencia>')`. -->
<!-- ## Objetos -->
<!-- ### Crear objetos -->
<!-- El operador de asignación ` <- ` te da la bienvenida, aunque también se puede escribir ` -> `. Transfórmalo en una flecha: hacia donde apunta es el valor que asume el nombre de objeto que se encuentra en el lado contrario. Lee `a <- 'Hola R'` como al objeto `a` es un vector cuyo valor es la cadena de caracteres `'Hola R'`. Creado el objeto, pedimos por ejemplo que se nos muestre su valor. En la consola se vería así: -->
<!-- ```{r} -->
<!-- a <- 'Hola R' -->
<!-- a -->
<!-- ``` -->
<!-- Al escribir `a` estamos llamando el objeto, y pedimos que se imprima su valor. Es equivalente a: -->
<!-- ```{r} -->
<!-- print(a) -->
<!-- ``` -->
<!-- Encontrarás largas discusiones y acalorados debates sobre si usar ` <- ` como asignador o `=`. Por limpieza de código, y para evitar confusión entre argumentos de funciones y declaraciones de objetos, recomiendo usar ` <- ` como asignador. -->
<!-- ### Tipos -->
<!-- ### Guardar -->
<!-- ## Scripts -->
<!-- * Crear. -->
<!-- * Guardar. -->
<!-- ## Tablas (`data.frame`, `tibble`) -->
<!-- * Crear. -->
<!-- * Importar. -->
<!-- * Operaciones básicas. -->
Situaciones comunes
-------------------

-   R es sensible a las mayúsculas. No es lo mismo `Mi_objeto` que `mi_objeto`.
-   *"En RStudio, ¿Qué atajo de teclas es que usan para poner el operador de asignación `<-`?"* Debería funcionarte `ALT+-`, pero recuerda, sólo lo podrás usar en RStudio.
-   *"¿Y el *pipe\* `%>%`?"\* `CTRL+SHIFT+M`.
-   Más atajos de teclado de RStudio: `ALT+SHIFT+K`.
-   *"Me quedé trancá' en la consola de R con un signo de `+`. ¿Qué hago pa' salir de eso?"*. Suele resolverse presionando la tecla `Escape` (`Esc`). Lee [este texto](https://support.rstudio.com/hc/en-us/community/posts/200792676-stuck-on-).

Referencias
===========

Borcard, D., Gillet, F., & Legendre, P. (2018). *Numerical ecology with r*. Springer.

Wickham, H., & Grolemund, G. (2017). *R for data science: Import, tidy, transform, visualize, and model data* (1st ed.). Retrieved from <http://r4ds.had.co.nz/>
