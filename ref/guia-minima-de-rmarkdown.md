
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

-   Encabezado YAML, la parte inicial rodeada de ---
-   Trozos o bloques de código, rodeados por \`\`\`
-   Texto, el cual admite estilos y formatos de texto, como en Markdown, pero con más opciones, dependiendo del tipo de archivo de salida que desees generar.

Cada una de estas partes las encontrarás bien explicadas en el (capítulo 27 de Wickham & Grolemund, 2017)(<https://es.r4ds.hadley.nz/r-markdown.html>), incluyendo una guía de referencia para las opciones.

Para crear un archivo `.Rmd` ve a `File>New File>R Markdown ...`. Un asistente te preguntará qué tipo de salida necesitas. Por ejemplo, puedes elegir documentos PDF, Word, HTML en la sección `Document` del asistente, pero también podrías elegir plantillas de revistas científicas u otras salidas estandarizada (como archivos Markdown estilo GitHub) yendo a la sección `From Template`.

<figure>
<img src="../img/rmd-guide-template.png" width="400">
</figure>
Los bloques de código los puede ejecutar con el botón `Run` ![](../img/rmd-guide-run.png), localizado en la barra superior del archivo `.Rmd`. Puedes (recomiendo) configurar que los bloques de código se ejecuten en la consola, haciendo clic en la rueda dentada de la misma barra y eligiendo `Chunk Output in Console`:

<figure>
<img src="../img/rmd-guide-chunk-output-console.png" width="200">
</figure>
Referencias
-----------

Wickham, H., & Grolemund, G. (2017). *R for data science: Import, tidy, transform, visualize, and model data* (1st ed.). Retrieved from <http://r4ds.had.co.nz/>
