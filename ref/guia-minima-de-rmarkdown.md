
<!-- Este .md fue generado a partir del .Rmd homónimo. Edítese el .Rmd -->
Guía mínima de RMarkdown
========================

Con RMarkdown puedes hacer tu artículo, tu trabajo de la universidad, tu informe, tu presentación de diapositivas, tu página web, tu libro, tu ... . Tu texto, tus figuras, tus referencias bibliográficas, tu código reproducible y los resultados de tu código, todo en un único lugar. RMarkdown es un *notebook* donde puedes hacer todo el flujo de trabajo reproducible para facilitarte la tarea de comunicar tus resultados. No necesitas más justificación, porque pa'colmo, el tali lo exige, qué más justificación que esa. Vamo' al mambo.

Lo básico
---------

    ---
    output: github_document
    bibliography: biblio.bib
    csl: apa.csl
    ---

    ```{r, echo = FALSE}
    knitr::opts_chunk$set(
      # results='hold',
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

    Lee sobre el [diagrama de dispersión](https://es.wikipedia.org/wiki/Diagrama_de_dispersi%C3%B3n). Si observas detenidamente las variables `dfs` y `flo` de la [tabla `doubs$env`](#doubs), quizá no detectes a golpe de vista que existe correlación entre ambas; es precisamente en este punto donde los gráficos te pueden ayudar.

    ```{r, message=FALSE}
    library(tidyverse)
    ```

    ...

    El gráfico de dispersión a continuación muestra que existe  correlación positiva entre las variables seleccionadas.

    ```{r intro-doubscatter}
    ggplot(data = doubs$env) +
      geom_point(mapping = aes(x = dfs, y = flo))
    ```

Referencias
-----------
