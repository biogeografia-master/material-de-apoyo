
<!-- Este .md fue generado a partir del .Rmd homónimo. Edítese el .Rmd -->
Introducción a R y Visualización rápida de datos
================================================

Introducción a R
----------------

### Recursos

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

### Instalación y ejecución de R y RStudio

-   Puedes usar el servidor RStudio habilitado por el profesor. Habrás recibido un correo electrónico con los detalles de acceso.

-   Si prefieres trabajar en tu propia PC, instala R y RStudio. La guía de instalación varía mucho según el sistema operativo:
    -   [R](https://cloud.r-project.org/)
    -   [RStudio](https://www.rstudio.com/products/rstudio/download/#download)
-   Igualmente, la forma de ejecutar estas aplicaciones dependerá del sistema operativo.
    -   En GNU/Linux es posible ejecutar tanto aplicaciones tanto desde el gestor de ventanas como desde el intérprete de línea de órdenes (CLI) o "terminal" (por ejemplo, para ejecutar R, presiona `CRTL+ALT+T`, escribe `R` y presiona `<enter>`).
    -   En Windows y MacOS la ejecución se realiza desde el GUI.

### CRAN (Comprehensive R Archive Network)

-   [¿Qué es CRAN?](https://cran.r-project.org/doc/FAQ/R-FAQ.html#What-is-CRAN_003f)
-   Instalar paquetes: Ejemplo: `install.packages('vegan', dependencies = T)`. Si realizas tus asignaciones en el servidor RStudio habilitado por el profesor, no necesitarás instalar paquetes.

### Ayuda de R

``` r
help(package = 'base') #Ayuda sobre un paquete
library(help = 'base') #Documentación sobre un paquete
help(lm) #Ayuda sobre una función
?lm #Ídem
example(lm) #Ejemplo(s) sobre una función
help.search("matrix") #Busca la palabra clave en las ayudas de los paquetes
??matrix #Ídem
```

¡Usa los foros! Si introduces un mensaje de error de R en el buscador de tu preferencia (en inglés obtienes más resultados), encontrarás varios punteros a foros con posibles soluciones.

Visualización de datos
----------------------

Wickham & Grolemund (2017) afirman que, durante la producción de resultados comunicables, subyace la necesidad de realizar el análisis exploratorio de datos (AED o EDA) lo más rápidamente posible. El esquema a continuación, de la misma fuente, resume este proceso:

<img src="https://es.r4ds.hadley.nz/diagrams_w_text_as_path/es/data-science-explore.svg" width="65%" />

Las múltiples herramientas ofrecidas por los paquetes de la colección `tidyverse` te servirán para agilizar sustancialmente el EDA. Los paquetes `dplyr`, `tidyr` y otros, te ayudarán a importar, ordenar y transformar datos, mientras `ggplot2` te ayudará a crear gráficos estilizados eficientemente. Wickham & Grolemund (2017) aseguran que estas herramientas mantienen la motivación en el aprendizaje por sus flujos de trabajo lineales.

### El conjunto de datos `doubs`

En esta guía de referencia, utilizo el conjunto de datos `doubs` de Verneaux (1973), cargándolo mediante el paquete `ade4`. Estos datos se utilizan también en Borcard, Gillet, & Legendre (2018).

``` r
library(ade4)
data(doubs)
```

> **Nota**. Si no usas el servidor RStudio habilitado por el profesor, instala `ade4` con `install.packages('ade4', dependencies = T)`

La sentencia anterior carga el objeto `doubs` a memoria, pero no lo imprime en pantalla. `doubs` es una lista de 4 tablas o *data.frame*, etiquetadas como `env`-matriz ambiental, `fish`-matriz de comunidad usando abundancia semi-cuantitativa (más explicación abajo), `xy`-matriz de coordenadas de las muestras y `species`-nombres de las 27 especies encontradas. Las filas de los tres primeros *data.frame* corresponden a 30 sitios muestreados a lo largo del río franco-suizo Doubs.

<a name="doubs"></a>Como ves, el objeto `doubs` se compone de varios elementos, por lo que es preferible imprimirlo en pantalla por separado. Para imprimir sólo un objeto de una lista, se usa el operador `$`. Así, `doubs$env`, imprime sólo la matriz ambiental.

``` r
doubs$env
##     dfs alt   slo  flo pH har pho nit amm oxy bdo
## 1     3 934 6.176   84 79  45   1  20   0 122  27
## 2    22 932 3.434  100 80  40   2  20  10 103  19
## 3   102 914 3.638  180 83  52   5  22   5 105  35
## 4   185 854 3.497  253 80  72  10  21   0 110  13
## 5   215 849 3.178  264 81  84  38  52  20  80  62
## 6   324 846 3.497  286 79  60  20  15   0 102  53
## 7   268 841 4.205  400 81  88   7  15   0 111  22
## 8   491 792 3.258  130 81  94  20  41  12  70  81
## 9   705 752 2.565  480 80  90  30  82  12  72  52
## 10  990 617 4.605 1000 77  82   6  75   1 100  43
## 11 1234 483 3.738 1990 81  96  30 160   0 115  27
## 12 1324 477 2.833 2000 79  86   4  50   0 122  30
## 13 1436 450 3.091 2110 81  98   6  52   0 124  24
## 14 1522 434 2.565 2120 83  98  27 123   0 123  38
## 15 1645 415 1.792 2300 86  86  40 100   0 117  21
## 16 1859 375 3.045 1610 80  88  20 200   5 103  27
## 17 1985 348 1.792 2430 80  92  20 250  20 102  46
## 18 2110 332 2.197 2500 80  90  50 220  20 103  28
## 19 2246 310 1.792 2590 81  84  60 220  15 106  33
## 20 2477 286 2.197 2680 80  86  30 300  30 103  28
## 21 2812 262 2.398 2720 79  85  20 220  10  90  41
## 22 2940 254 2.708 2790 81  88  20 162   7  91  48
## 23 3043 246 2.565 2880 81  97 260 350 115  63 164
## 24 3147 241 1.386 2976 80  99 140 250  60  52 123
## 25 3278 231 1.792 3870 79 100 422 620 180  41 167
## 26 3579 214 1.792 3910 79  94 143 300  30  62  89
## 27 3732 206 2.565 3960 81  90  58 300  26  72  63
## 28 3947 195 1.386 4320 83 100  74 400  30  81  45
## 29 4220 183 1.946 6770 78 110  45 162  10  90  42
## 30 4530 172 1.099 6900 82 109  65 160  10  82  44
```

`doubs$env` contiene información ambiental con las siguientes variables: `dfs`-distancia desde cabecera (en km x 10), `alt`-altitud (en m), `slo`-pendiente (log(x+1), donde x es la pendiente en tantos por 1000), `flo`-caudal promedio mínimo (m<sup>3</sup>/s 100), `pH` ( x 10), `har`-dureza del agua (mg/l de calcio), `pho`-fostados (mg/l x 100), `nit`-nitratos, `amm`-amoníaco, `nit`-nitrógeno (mg/l x 100), `oxy`-oxígeno disuelto (mg/l x 100), `bdo`-demanda biológica de oxígeno (mg/l x 10)

La tabla `doubs$fish` contiene la abundancia de especies. Los valores de las celdas no son individuos; la abundancia está representada en una escala semi-cuantitativa específica por especie, que va de 0 a 5. Por lo tanto, los valores no pueden entenderse como estimadores insesgados de la abundancia real o de la biomasa por sitio (Borcard et al., 2018). La abreviatura usada como nombre de columna se explica en la tabla `doubs$species`.

``` r
doubs$fish
##    Cogo Satr Phph Neba Thth Teso Chna Chto Lele Lece Baba Spbi Gogo Eslu
## 1     0    3    0    0    0    0    0    0    0    0    0    0    0    0
## 2     0    5    4    3    0    0    0    0    0    0    0    0    0    0
## 3     0    5    5    5    0    0    0    0    0    0    0    0    0    1
## 4     0    4    5    5    0    0    0    0    0    1    0    0    1    2
## 5     0    2    3    2    0    0    0    0    5    2    0    0    2    4
## 6     0    3    4    5    0    0    0    0    1    2    0    0    1    1
## 7     0    5    4    5    0    0    0    0    1    1    0    0    0    0
## 8     0    0    0    0    0    0    0    0    0    0    0    0    0    0
## 9     0    0    1    3    0    0    0    0    0    5    0    0    0    0
## 10    0    1    4    4    0    0    0    0    2    2    0    0    1    0
## 11    1    3    4    1    1    0    0    0    0    1    0    0    0    0
## 12    2    5    4    4    2    0    0    0    0    1    0    0    0    0
## 13    2    5    5    2    3    2    0    0    0    0    0    0    0    0
## 14    3    5    5    4    4    3    0    0    0    1    1    0    1    1
## 15    3    4    4    5    2    4    0    0    3    3    2    0    2    0
## 16    2    3    3    5    0    5    0    4    5    2    2    1    2    1
## 17    1    2    4    4    1    2    1    4    3    2    3    4    1    1
## 18    1    1    3    3    1    1    1    3    2    3    3    3    2    1
## 19    0    0    3    5    0    1    2    3    2    1    2    2    4    1
## 20    0    0    1    2    0    0    2    2    2    3    4    3    4    2
## 21    0    0    1    1    0    0    2    2    2    2    4    2    5    3
## 22    0    0    0    1    0    0    3    2    3    4    5    1    5    3
## 23    0    0    0    0    0    0    0    0    0    1    0    0    0    0
## 24    0    0    0    0    0    0    1    0    0    2    0    0    1    0
## 25    0    0    0    0    0    0    0    0    1    1    0    0    2    1
## 26    0    0    0    1    0    0    1    0    1    2    2    1    3    2
## 27    0    0    0    1    0    0    1    1    2    3    4    1    4    4
## 28    0    0    0    1    0    0    1    1    2    4    3    1    4    3
## 29    0    1    1    1    1    1    2    2    3    4    5    3    5    5
## 30    0    0    0    0    0    0    1    2    3    3    3    5    5    4
##    Pefl Rham Legi Scer Cyca Titi Abbr Icme Acce Ruru Blbj Alal Anan
## 1     0    0    0    0    0    0    0    0    0    0    0    0    0
## 2     0    0    0    0    0    0    0    0    0    0    0    0    0
## 3     0    0    0    0    0    0    0    0    0    0    0    0    0
## 4     2    0    0    0    0    1    0    0    0    0    0    0    0
## 5     4    0    0    2    0    3    0    0    0    5    0    0    0
## 6     1    0    0    0    0    2    0    0    0    1    0    0    0
## 7     0    0    0    0    0    0    0    0    0    0    0    0    0
## 8     0    0    0    0    0    0    0    0    0    0    0    0    0
## 9     0    0    0    0    0    1    0    0    0    4    0    0    0
## 10    0    0    0    0    0    0    0    0    0    0    0    0    0
## 11    0    0    0    0    0    0    0    0    0    0    0    0    0
## 12    0    0    0    0    0    0    0    0    0    0    0    0    0
## 13    0    0    0    0    0    0    0    0    0    0    0    0    0
## 14    0    0    0    0    0    0    0    0    0    0    0    0    0
## 15    0    0    0    0    0    1    0    0    0    0    0    0    0
## 16    1    0    1    0    1    1    0    0    0    1    0    0    0
## 17    2    1    1    0    1    1    0    0    0    2    0    2    1
## 18    3    2    1    0    1    1    0    0    1    2    0    2    1
## 19    1    2    1    1    1    2    1    0    1    5    1    3    1
## 20    2    3    2    2    1    4    1    0    2    5    2    5    2
## 21    3    3    2    2    2    4    3    1    3    5    3    5    2
## 22    4    3    3    2    3    4    4    2    4    5    4    5    2
## 23    0    0    0    0    0    0    0    0    0    1    0    2    0
## 24    0    0    1    0    0    0    0    0    2    2    1    5    0
## 25    0    0    0    1    0    0    0    0    1    1    0    3    0
## 26    1    2    2    1    1    3    2    1    4    4    2    5    2
## 27    1    3    3    1    2    5    3    2    5    5    4    5    3
## 28    2    4    4    2    4    4    3    3    5    5    5    5    4
## 29    4    5    5    2    3    3    4    4    5    5    4    5    4
## 30    5    5    3    5    5    5    5    5    5    5    5    5    5
```

La tabla `doubs$species` contiene los nombre de las 27 especies de peces.

``` r
doubs$species
##                     Scientific             French           English code
## 1                 Cottus gobio             chabot european bullhead Cogo
## 2           Salmo trutta fario       truite fario       brown trout Satr
## 3            Phoxinus phoxinus             vairon            minnow Phph
## 4       Nemacheilus barbatulus      loche franche       stone loach Neba
## 5          Thymallus thymallus              ombre          grayling Thth
## 6     Telestes soufia agassizi            blageon           blageon Teso
## 7           Chondrostoma nasus               hotu              nase Chna
## 8       Chondostroma toxostoma          toxostome         toxostoma Chto
## 9          Leuciscus leuciscus           vandoise       common dace Lele
## 10 Leuciscus cephalus cephalus           chevaine              chub Lece
## 11               Barbus barbus barbeau fluviatile            barbel Baba
## 12       Spirlinus bipunctatus            spirlin           spirlin Spbi
## 13                 Gobio gobio             goujon           gudgeon Gogo
## 14                 Esox lucius            brochet              pike Eslu
## 15           Perca fluviatilis  perche fluviatile             perch Pefl
## 16              Rhodeus amarus           bouviere        bitterling Rham
## 17            Lepomis gibbosus      perche-soleil       pumpkinseed Legi
## 18  Scardinius erythrophtalmus           rotengle              rudd Scer
## 19             Cyprinus carpio              carpe              carp Cyca
## 20                 Tinca tinca             tanche             tench Titi
## 21               Abramis brama              breme  freshwater bream Abbr
## 22             Ictalurus melas       poisson chat    black bullhead Icme
## 23              Acerina cernua           gremille             ruffe Acce
## 24             Rutilus rutilus             gardon             roach Ruru
## 25             Blicca bjoerkna   breme bordeliere      silver bream Blbj
## 26           Alburnus alburnus            ablette             bleak Alal
## 27           Anguilla anguilla           anguille               eel Anan
```

Las cuatro columnas corresponden a: `Scientific`-nombre científico, `French` y `English`-nombres comunes en francés y en inglés, `code` códigos de cuatro caracteres usados como nombres de columnas en la tabla `doubs$fish`.

### Diagrama de dispersión

Lee sobre el [diagrama de dispersión](https://es.wikipedia.org/wiki/Diagrama_de_dispersi%C3%B3n). Si observas detenedimante las variables `dfs` y `flo` de la [tabla `doubs$env`](#doubs), quizá no detectes a golpe de vista que existe correlación entre ambas, y es precisamente en este punto donde los gráficos te pueden ayudar.

``` r
library(tidyverse)
```

> **Nota**. Si no realizas tu asignación en el servidor RStudio habilitado por el profesor, debes asegurarte de instalar la colección `tidyverse` (`install.packages(tidyverse, dependencies=T)`).

El gráfico de dispersión a continuación muestra que existe correlación positiva entre las variables seleccionadas.

``` r
ggplot(data = doubs$env) +
  geom_point(mapping = aes(x = dfs, y = flo))
```

![](../img/intro-dfscatter-1.png)

Lógicamente, como es de esperar, a mayor distancia de la cabecera, mayor el caudal. Destacan también dos observaciones atípicas en el extremo superior derecho del gráfico, que corresponden a dos puntos de colecta que obtuvieron valores de flujo muy altos. Volveré sobre estos valores extremos (*outliers*) maś adelante.

`ggplot` crea el sistema de coordenadas a partir del objeto introducido en el argumento `data`, es decir, a partir del conjunto de datos (`ggplot` convierte este objeto a un `data.frame` si al entrar en la función aún no lo es). Por lo tanto, si ejecutaras `ggplot(data = dfs_flo)` obtendrás un gráfico vacío.

A partir de este punto, se pueden añadir una o más capas. En este caso, se añadió una de puntos mediante `geom_point`. Las capas usan el argumento `mapping` para definir la posición y el rol de cada variable en el gráfico. Por lo tanto, los elementos básicos son crear el sistema de coordenadas (`ggplot`), especificar los datos, crear una capa (e.g. `geom_point`) y decclarar cómo se posicionarán las variables. [Aquí](https://www.rstudio.com/wp-content/uploads/2015/03/ggplot2-cheatsheet.pdf) tienes una guía de referencia sobre las capas más comunes.

Puedes editar la forma y el tamaño de todos los elementos del gráfico: rótulos, simbología, cuadrícula, ejes, etc. Existen múltiples argumentos disponibles para gráficos estéticos, que encontrarás en guías de `ggplot2` en línea, como [ésta](https://www.rdocumentation.org/packages/ggplot2/versions/3.2.1) y [esta](https://swcarpentry.github.io/r-novice-gapminder-es/08-plot-ggplot2/index.html). También puedes ver [esta galería](http://www.ggplot2-exts.org/gallery/) para conocer distintas formas de visualizar datos. Puedes también consultar Wickham (2016), un material de contenido exhaustivo y de referencia, donde verás las distintas capas y configuraciones estéticas.

Mostraré los puntos en función de su condición de *outliers*, utilizando distintos colores y formas. No prestes mucha atención a la primera línea de código, sino al gráfico resultante

``` r
doubs$env$flo_outlier <- ifelse(
  doubs$env$flo %in% invisible(boxplot(doubs$env$flo)$out),
  'outlier', 'no outlier')
```

``` r
ggplot(data = doubs$env) +
  geom_point(mapping = aes(x = dfs, y = flo, colour = flo_outlier))
```

![](../img/intro-dfscatter-out-1.png)

``` r
ggplot(data = doubs$env) +
  geom_point(mapping = aes(x = dfs, y = flo, size = flo_outlier))
## Warning: Using size for a discrete variable is not advised.
```

![](../img/intro-dfscatter-out-2.png)

``` r
ggplot(data = doubs$env) +
  geom_point(mapping = aes(x = dfs, y = flo, shape = flo_outlier))
```

![](../img/intro-dfscatter-out-3.png)

Aunque no son muy informativos sin una barra de error, puedes hacer gráficos de barras. Utilizaré la escala semi-cuantitativa de abundancia para responder a la pregunta: ¿cuál es el nivel de abundancia predominante de `Salmo trutta fario` en la muestra?

``` r
ggplot(data = doubs$fish) + geom_bar(aes(x=Satr))
```

![](../img/intro-barplot-1.png)

El gráfico está informando que el nivel de abundancia más común es 0, es decir, la subespecie está ausente en 13 de los 30 sitios, es decir, es más común no encontrarla. Si ordenásemos los datos de `Satr` de menor a mayor, podríamos también percatarnos de lo que informa este gráfico, razón por la que se les considera poco útiles.

``` r
sort(doubs$fish[,2])
##  [1] 0 0 0 0 0 0 0 0 0 0 0 0 0 1 1 1 2 2 3 3 3 3 4 4 5 5 5 5 5 5
```

Las variables cualitativas suelen representarse como conteos de observaciones en este tipo de gráfico. Así, si en tus datos hay variables cualitativas, podrías hacer gráficos de barra, pero no olvides explorar cómo incluir la barra de error.

Por ejemplo, si probar con otros pares de variables, par a par, pero `ggplot2` trae funciones incorporadas para asistirte en dicha tarea, construyendo facetas o paneles de gráficos.

### Panel de correlaciones

El paquete `ez`, apoyándose en `ggplot2`, construye gráficos de dispersión, gráficos de densidad e imprime a su vez el valor del coeficiente `r`. Muy útil cuando se quiere explorar muchas variables al mismo tiempo.

``` r
library(ez)
ezCor(
  doubs$env[sapply(doubs$env, is.numeric)],
  r_size_lims = c(4,8),
  label_size = 7
)
```

![](../img/intro-ezscatter-1.png)

> **Nota**. la función `ezCor` sólo admite `data.frame` con columnas numéricas.

Aunque los paquetes de análisis de datos ecológicos no están "saborizados" al estilo `tidyverse`, al menos el EDA lo podrás realizar utilizando tuberías de esta potente colección de paquetes.

``` r
dfs_flo <- doubs$env %>% select(dfs, flo)
dfs_flo
##     dfs  flo
## 1     3   84
## 2    22  100
## 3   102  180
## 4   185  253
## 5   215  264
## 6   324  286
## 7   268  400
## 8   491  130
## 9   705  480
## 10  990 1000
## 11 1234 1990
## 12 1324 2000
## 13 1436 2110
## 14 1522 2120
## 15 1645 2300
## 16 1859 1610
## 17 1985 2430
## 18 2110 2500
## 19 2246 2590
## 20 2477 2680
## 21 2812 2720
## 22 2940 2790
## 23 3043 2880
## 24 3147 2976
## 25 3278 3870
## 26 3579 3910
## 27 3732 3960
## 28 3947 4320
## 29 4220 6770
## 30 4530 6900
```

El operador `%>%`, bautizado como "pipa" (*pipe*), pertenece al paquete `magrittr`, el cual es importado automáticamente cuando se instala la colección `tidyverse`. Este operador utiliza la salida de la función a su izquierda y la coloca como primer argumento de la función a la derecha. Así, la sentencia anterior se lee como "del objeto `doubs$env`, selecciona las columnas `dfs` y `flo` y con el resultado crea el objeto `dfs_flo`".

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
-   *"En RStudio, ¿Qué atajo de teclado es que usan para poner el operador de asignación `<-`?"* Debería funcionarte `ALT+-`, pero recuerda, sólo lo podrás usar en RStudio.
-   *"¿Y el *pipe\* `%>%`?"\* `CTRL+SHIFT+M`.
-   Más atajos de teclado de RStudio: `ALT+SHIFT+K`.
-   *"Me quedé trancá' en la consola de R con un signo de `+`. ¿Qué hago pa' salir de eso?"* Suele resolverse presionando la tecla `Escape` (`Esc`). Lee [este texto](https://support.rstudio.com/hc/en-us/community/posts/200792676-stuck-on-).

Referencias
-----------

Borcard, D., Gillet, F., & Legendre, P. (2018). *Numerical ecology with r*. Springer.

Verneaux, J. (1973). *Cours d’eau de franche-comté (massif du jura): Recherches écologiques sur le réseau hydrographique du doubs: Essai de biotypologie* (PhD thesis). Institut des Sciences Naturelles.

Wickham, H. (2016). *Ggplot2: Elegant graphics for data analysis*. Springer.

Wickham, H., & Grolemund, G. (2017). *R for data science: Import, tidy, transform, visualize, and model data* (1st ed.). Retrieved from <http://r4ds.had.co.nz/>
