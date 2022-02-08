# Universidad Autónoma de Santo Domingo (UASD) <br/>
Programa de Biogeografía (GEO-131) <br/>
14 de Septiembre de 2021 (semestre 2021-02) <br/>
*José Ramón Martínez Batlle*

## Básicos:

* Correo: jmartinez19@uasd.edu.do

* Lugar y horario: Zoom, Martes de 4 a 8 pm

* [Programa (hipervínculo recursivo)](programa-biogeografia-geo1310.md)

## Recursos informáticos de la asignatura

Sitúa apropiadamente los recursos de los que dispondrás en esta asignatura, los cuales describo [aquí](guia-redaccion-manuscrito.md#ecosistema).

## Descripción

La ciencia está en crisis, una crisis de reproducibilidad. Difícilmente un equipo científico reproduce el resultado que obtuvo otro. Se atribuye este déficit a que, al publicar los resultados, no se aportan ni las fuentes, ni los métodos empleados. El panorama está cambiando, pero la única forma de aumentar la reproducibilidad consiste en abrir las fuentes y utilizar métodos reproducibles que normalmente implican utilizar código abierto. La biogeografía no escapa a esta realidad, por lo que en esta asignatura intentarás contribuir a romper el círculo cerrado del conocimiento, empleando métodos para producir en abierto.

Puedes sospechar desde ya que R estará de fondo (a fin de cuentas, este tali usa mucho R), sobre todo por tratarse de una asignatura meramente ecológica. Sin embargo, son bienvenidos todos los lenguajes de programación que quieras utilizar. Si sabes python, C o cualquier otro lenguaje con el que puedas ayudarte a responder preguntas ecológicas, puedes usarlos sin inconveniente alguno. La única condición es que tienes que publicar tu código y tus fuentes. Hay una comunidad allá fuera que explica cómo atender los típicos desafíos y los mensajes de error, y yo también podré ayudar. Además, esa misma comunidad también podría interesarse por o necesitar tus aportes.

La biogeografía es la ciencia que __intenta documentar y entender los patrones espaciales de la diversidad biológica__. Modernamente estudia todos los patrones de variación geográfica (y temporal) de la diversidad biológica de elementos naturales (desde genes hasta comunidad y ecosistema) asociados a gradientes de variables tales como el área, el aislamiento, la latitud, la profundidad o la elevación. También se le suele definir como el estudio de la distribución de organismos, tanto en el presente como en el pasado.

## Resultados esperados

Al finalizar la asignatura, esta afirmación debería ser cierta: aplicas y redactas métodos de ecología numérica utilizando datos de terceros o propios, especialmente utilizas código reproducible para aplicar técnicas de análisis de la biodiversidad y, quizá, algo de análisis espacial. Complementariamente, intentas aprender en cabeza ajena sobre fundamentos de biogeografía. Comprendes los principios geográficos y ecológicos de la biogeografía, así como los procesos biogeográficos y la historia de la Tierra.

## Evaluación

| Ítem                                                       | % de la  nota final |
| ---------------------------------------------------------- | ------------------: |
| [Manuscrito (basado en datos pre-existentes)](#manuscrito) |                 50% |
| [Presentación oral](#presentación-oral)                    |                 20% |
| [Asignaciones](#asignaciones)                              |                 30% |

Sí sí, lo que viste, no hay examen.

Brevemente, cada ítem a evaluar consistirá en lo siguiente (más detalles por medio de asignaciones a lo largo del curso):

### Manuscrito

Tratará sobre un grupo de organismos, se elaborará siguiendo las fases enumeradas a continuación:

1. Formulación del problema/pregunta(s) de investigación, siendo preceptiva la sencillez de diseño. Las preguntas de investigación a responder las diseñarás tú.

2. Revisión bibliográfica. Busca fuentes en línea, pero evita abrumarte con la enorme disponibilidad de publicaciones científicas sobre biogeografía y ecología. Prefiere las publicaciones disponibles en acceso libre, y no olvides el [Sci-Hub](https://sci-hub.se).

3. Selección de metodología, incluyendo técnicas cuantitativas de forma preceptiva.

4. Recogida de datos a partir de servicios en línea (guiado por el profesor), incluyendo análisis exploratorio-limpieza.

5. Análisis de datos.

6. Redacción. Volver eterna y recursivamente a 5 hasta que la redacción quede "nítida".

Los criterios de evaluación que usaré para el manuscrito son:

1. Cumplimiento de los requisitos exigidos por el [Anuario de Investigaciones Científicas](https://www.uasd.edu.do/index.php/publicaciones-cientificas) de la UASD.

2. Redacción coherente y concisa.

3. Resultados, con el debido apoyo estadístico y gráfico, que respondan a las preguntas formuladas.

4. Concisa extracción de conclusiones. Los resultados negativos son igualmente válidos.

Para preparar tu manuscrito, sigue las normas para autores/as del [Anuario de Investigaciones Científicas de la UASD](docs/instrucciones-para-autores-anuario-investigaciones-cientificas-UASD.pdf). Fungiré como editor ficticio de la revista, e incluso como revisor (*reviewer&nbsp;#2*).

* Como verás, el manuscrito requiere los siguientes ítems:
    * Título.
    * Nombre de autor/a.
    * Resumen y palabras clave.
    * *Abstract* y *keywords* (optativo).
    * Introducción.
    * Metodología.
    * Resultados.
    * Discusión.
    * Agradecimientos (optativo).
    * Referencias citadas.
    * *Script* reproducible
    * Declaración de cumplimientos legales y de no conflictos de intereses (optativo).
    * Otros requerimientos (ponle atención también a esta parte en las [normas](docs/instrucciones-para-autores-anuario-investigaciones-cientificas-UASD.pdf)).

Toma en consideración lo siguiente:

* No impartiré lecciones sobre redacción ni sobre procesadores de texto, por lo que se recomienda consultar material tanto vía web como en el economato, como forma de mejorar dichas capacidades. 

* El plagio y la falsificación de datos supondrán la reprobación inmediata de la asignatura.

* Te recomiendo consultar [uno o varios artículos de cualquier número del Anuario](https://www.uasd.edu.do/index.php/publicaciones-cientificas), para que te familiarices con el estilo de redacción.

### Presentación oral

Dispondrás de 15 minutos para presentar oralmente tu trabajo al final del semestre. Valoraré el dominio que muestres sobre tu trabajo.

## Escribir código/pedir ayuda

En cuanto a escribir código, te adelanto que, para superar las dificultades y los desafíos inherentes de las asignaciones y el manuscrito, tendrás que:

1. Contar con el profesor. No te abandonaré a tu suerte al analizar datos. No hay horario para pedirme ayuda, y pregunta lo que quieras preguntar, yo responderé cuando pueda. Intentaré darte soluciones cuando te tranques, pero con la condición de que, antes de preguntarme, intentes avanzar soluciones del problema. Lee los puntos 3 y 4 más abajo.

2. Sufrir. Nadie dijo que fajarse con biogeografía/ecología mediante R fuese placentero. A diferencia de los software de pago, aquí no hay un botoncito mágico que lo resuelve todo. Cuesta esfuerzo, mucho; eso sí, es gratis, como todas las cosas buenas. Además, te obliga a la abstracción y a la resolución de problemas, algo que siempre viene bien en términos profesionales y académicos. Adelanto también que este mismo principio aplica a la redacción; escribir concisamente apoyándote en tus resultados es tarea complicada. Por lo tanto, sufre, pero con motivo.

3. Pedir ayuda. Escríbeme o pide ayuda a tus compañeros y compañeras cuando te surjan dudas. Tienes varias alternativas, elige la que prefieras:
      a. Vía el foro de la asignatura (vía más eficiente y preferida).
      b. A mi correo: jmartinez19\@uasd.edu.do
      c. Creando *issues* en GitHub.

4. Al hilo del punto anterior, utilizar estrategias proactivas para pedir ayuda. Elimina esta expresión de tu vocabulario: "da error". Con eso nadie podrá ayudarte. Lo importante es informar qué intentaste hacer y qué error o problema te surgió. Por ello, cuando pidas ayuda, deberás ofrecer un ejemplo reproducible. En su lugar prefiere estas expresiones *"intente este procedimiento ... , dio este error, luego intenté esta solución ... pero no consigo dar con el fallo"*. Plantea tu problema con código reproducible siempre que puedas. Si envías captura de pantalla, no olvides dar contexto: tras qué surgió el error, qué intentaste para resolverlo. Otras estrategias son: consultar posibles soluciones a tu problema en foros ya existentes (como stackoverflow), probar alternativas, documentar lo que hiciste, explicar qué entiendes que pudo provocar el error. En definitiva, sólo pide ayuda cuando realmente llegues a un "tranque" y siempre intenta una solución por tu cuenta.

No tendrás que preocuparte por el hardware (ya me ensucio yo las manos con esa cosa tan mundana llamada computadora), pero sí ocúpate por escribir código con sentido (y preguntar siempre que lo necesites, no lo olvides), por razonar bien tus asignaciones y, especialmente, por escribir bien tu manuscrito; escribe que se te entienda, yo pediré a monesvol para que te ilumine. Dispondrás de un servidor de RStudio de modestas prestaciones administrado por "yo mesmamente", con los paquetes requeridos en el curso ya pre-instalados. Así podrás realizar tus asignaciones sobre biogeografía y tu manuscrito sin preocuparte de instalaciones de software/paquetes.


## Contenido teórico
1. Introducción e historia de la biogeografía. Brown y Lomolino (1998) capítulos 1 y 2. Okolodkov (2010) capítulos 1 y 2.
2. Contexto físico: la "plantilla" geográfica Smith y Smith (2007), segunda parte (capítulos 3 a 5). Brown y Lomolino (1998), capítulo 3.
3. Distribución de especies. Brown y Lomolino (1998), capítulo 4.
4. Distribución de comunidades. Brown y Lomolino (1998), capítulo 5.
5. Los cambios en la Tierra. Brown y Lomolino (1998), capítulo 6.
6. Especiación y extinción. Brown y Lomolino (1998), capítulo 8.
7. Dispersión. Brown y Lomolino (1998), capítulo 9.
8. Historia de los linajes. Brown y Lomolino (1998), capítulo 11.
9. Biogeografía insular. Brown y Lomolino (1998), capítulos 13 y 14

## Referencias bibliográficas
* Consulta el foro de la asignatura.
