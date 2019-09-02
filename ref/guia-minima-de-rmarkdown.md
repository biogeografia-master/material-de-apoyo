
<!-- Este .md fue generado a partir del .Rmd homónimo. Edítese el .Rmd -->
Guía mínima de RMarkdown
========================

Con RMarkdown puedes hacer tu artículo, tu trabajo de la universidad, tu informe, tu presentación de diapositivas, tu página web, tu libro y mucho más. RMarkdown integra las distintas partes de tu trabajo en un único lugar: texto, figuras, referencias bibliográficas, ódigo reproducible y los resultados de dicho código.

RMarkdown es un *notebook* donde puedes hacer todo el flujo de trabajo reproducible para facilitarte la tarea de comunicar tus resultados. Profundiza con la versión en español de Wickham & Grolemund (2017), el cual es igualmente mi referente. No necesitas más justificación, porque pa'colmo, el tali lo exige, qué más justificación que esa. Vamo' al mambo.

Lo básico
---------

Así comienza y continúa un archivo Rmd que, como verás, es texto plano:

    ---
    output: github_document
    bibliography: biblio.bib
    csl: apa.csl
    ---

    ```{r setup, include=FALSE}
    knitr::opts_chunk$set(
      echo = TRUE,
      collapse=TRUE,
      fig.path = "../img/"
    )
    ```

    <!-- Este .md fue generado a partir del .Rmd homónimo. Edítese el .Rmd -->

    # Introducción a R y análisis exploratorio de datos (EDA)

    ...

    ```{r}
    library(ade4)
    data(doubs)
    ```

    ...

    ### Diagrama de dispersión

    Lee sobre el [diagrama de dispersión](https://es.wikipedia.org/wiki/Diagrama_de_dispersi%C3%B3n).
    Si observas detenidamente las variables `dfs` y `flo` de la [tabla `doubs$env`](#doubs), quizá
    no detectes a golpe de vista que existe correlación entre ambas; es precisamente en este punto
    donde los gráficos te pueden ayudar.

    ```{r, message=FALSE}
    library(tidyverse)
    ```

    ...

    El gráfico de dispersión a continuación muestra que existe  correlación positiva entre las
    variables seleccionadas.

    ```{r intro-doubscatter}
    ggplot(data = doubs$env) +
      geom_point(mapping = aes(x = dfs, y = flo))
    ```

Las tres partes principales son:

-   Encabezado, donde defines

Cada uno de las partes las encontrarás bien explicadas en el (capítulo 27 de Wickham & Grolemund, 2017)(<https://es.r4ds.hadley.nz/r-markdown.html>), incluyendo una guía de referencia sobre opciones.

Referencias
-----------

Wickham, H., & Grolemund, G. (2017). *R for data science: Import, tidy, transform, visualize, and model data* (1st ed.). Retrieved from <http://r4ds.had.co.nz/>
