# Universidad Autónoma de Santo Domingo (UASD) <br/>
Programa de Biogeografía (GEO-131) <br/>
Semestre 2019-02 <br/>
*José Ramón Martínez Batlle*

## Básicos:
* Profesor: José Ramón Martínez Batlle
* Carrera: Licenciatura en Geografía (optativa para Licenciatura en Biología)
* Correo: jmartinez19@uasd.edu.do
* Página web: https://www.geografiafisica.org/
* Twitter: @geografiard
* Lugar y horario: Aula FC-203 (SIGCART), Martes de 2 a 6 pm

## URLs del contenido del curso:
* [Programa (hipervínculo recursivo)](programa-biogeografia-geo1310.md)
* Asignaciones: se enviarán por correo electrónico

## Descripción

La ciencia está en crisis, una crisis de reproducibilidad. Difícilmente un equipo científico reproduce el resultado que obtuvo otro. Se atribuye este déficit a que, al publicar los resultados, no se aportan ni las fuentes, ni los métodos empleados. El panorama está cambiando, pero la única forma de aumentar la reproducibilidad consiste en abrir las fuentes y utilizar métodos reproducibles que normalmente implican utilizar código abierto. La biogeografía no escapa a esta realidad, por lo que en esta asignatura intentarás contribuir a romper el círculo cerrado del conocimiento, empleando métodos para producir en abierto.

Puedes sospechar desde ya que R estará de fondo (a fin de cuentas, este tali usa mucho R), sobre todo por tratarse de una asignatura meramente ecológica. Sin embargo, son bienvenidos todos los lenguajes de programación que quieras utilizar. Si sabes python, C o cualquier otro lenguaje con el que puedas ayudarte a responder preguntas ecológicas, puedes usarlos sin inconveniente alguno. La única condición es que tienes que publicar tu código y tus fuentes. Hay una comunidad allá fuera que explica cómo atender los típicos desafíos y los mensajes de error, y yo también podré ayudar. Además, esa misma comunidad también podría interesarse por o necesitar tus aportes.

La biogeografía es la ciencia que intenta documentar y entender los patrones espaciales de la diversidad biológica. Modernamente estudia todos los patrones de variación geográfica (y temporal) de la diversidad biológica de elementos naturales (desde genes hasta comunidad y ecosistema) asociados a gradientes de variables tales como el área, el aislamiento, la latitud, la profundidad o la elevación. También se le suele definir como el estudio de la distribución de organismos, tanto en el presente como en el pasado.

## Resultados esperados

Al finalizar la asignatura, esta afirmación debería ser cierta: aplicas y redactas métodos de ecología numérica utilizando tus propios datos, especialmente utilizas código reproducible para aplicar técnicas de diseño de estudios de campo, análisis de la biodiversidad y, quizá, algo de análisis espacial. Complementariamente, intentas aprender en cabeza ajena sobre fundamentos de biogeografía. Comprendes los principios geográficos y ecológicos de la biogeografía, así como los procesos biogeográficos y la historia de la Tierra.

## Evaluación

| Ítem | % de la \ nota final |
|-|-:|
| [Manuscrito](#manuscrito) | 25% |
| [Presentación oral](#presentación-oral) | 5% |
| [Trabajo de campo e identificación](#trabajo-de-campo-e-identificación) | 30% |
| [Código informático reproducible](#código-informático-reproducible) | 20% |
| [Examen parcial 1](#examen-parcial-1) | 10%<sup>1</sup> |
| [Examen parcial 2](#examen-parcial-2) | 10%<sup>1</sup> |

<sup>1</sup> Implementaré un sistema adaptativo. Si a la fecha del examen parcial 1 (medio término), has realizado las asignaciones prácticas solicitadas (ver sección [Fechas de evaluación](#fechas-de-evaluación)), el valor de ambos exámenes será el que aparece en la tabla de referencia (10% cada uno). En caso contrario, evaluaré de la siguiente manera: examen parcial 1 50%, examen parcial 50%.

Brevemente, cada ítem a evaluar consistirá en lo siguiente (más detalles por medio de asignaciones a lo largo del curso):

### Manuscrito

Tratará sobre hormigas del campus de la UASD, se elaborará siguiendo las siguientes fases:
1. Formulación del problema/pregunta(s) de investigación, siendo preceptiva la sencillez de diseño. Las preguntas de investigación a responder las diseñarás tú.
2. Revisión bibliográfica. Busca fuentes en línea, pero evita abrumarte con la enorme disponibilidad de publicaciones científicas sobre biogeografía y ecología. Prefiere las publicaciones disponibles en acceso libre.
3. Selección de metodología, incluyendo técnicas cuantitativas de forma preceptiva. 
4. Recogida de datos de campo.
5. Análisis de datos.
6. Redacción.

Los criterios de evaluación que usaré para el manuscrito son:
1. Cumplimiento de los requisitos exigidos por el Anuario, tanto los de forma (estilos de documento) como los de fondo.
2. Redacción coherente y concisa. 
3. Resultados, con el debido apoyo estadístico y gráfico, que respondan a las preguntas formuladas.
4. Concisa extracción de conclusiones. Los resultados negativos son igualmente válidos.

Para preparar tu manuscrito, sigue las normas para autores/as del [Anuario de Investigaciones Científicas de la UASD](docs/instrucciones-para-autores-anuario-investigaciones-cientificas-UASD.pdf). Fungiré como editor ficticio de la revista, e incluso como revisor.

* Como verás, el manuscrito requiere los siguientes ítems:
    * Título.
    * Nombre de autor/a.
    * Resumen y palabras clave.
    * *Abstract* y *keywords* (optativo).
    * Metodología.
    * Resultados.
    * Discusión.
    * Agradecimientos (optativo).
    * Referencias citadas.
    * Declaración de cumplimientos legales y de no conflictos de intereses (optativo).
    * Otros requerimientos (ponle atención también a esta parte en las [normas](docs/instrucciones-para-autores-anuario-investigaciones-cientificas-UASD.pdf)).

Toma en consideración lo siguiente:
* No impartiré lecciones sobre redacción ni sobre procesadores de texto, por lo que se recomienda consultar material tanto vía web como en el economato, como forma de mejorar dichas capacidades. 
* El plagio y la falsificación de datos supondrán la reprobación inmediata de la asignatura.
* Te recomiendo consultar [uno o varios artículos de cualquier número del Anuario](https://www.uasd.edu.do/index.php/publicaciones-cientificas), para que te familiarices con el estilo de redacción.

### Presentación oral

Dispondrás de 15 minutos para presentar oralmente tu trabajo al final del semestre. Valoraré el dominio que muestres sobre tu trabajo.

### Trabajo de campo e identificación

Tomarás al menos 10 muestras (a mayor número, mejor) en igual número de polígonos (*plots*) previamente delimitados del campus de la UASD. Utilizarás el método del cebo de atún (en clase explicaré por qué).

En cada polígono colocarás al menos 16 estaciones de cebo de atún directamente en el suelo, formando una malla cuadrada de 4x4 estaciones colocada aproximadamente en el centro del polígono. Separarás cada estación al menos 2 metros entre sí, por lo que la malla tendrá 8x8=64m<sup>2</sup> de tamaño.

Dejarás los cebos por 30 minutos y luego colectarás las hormigas que visiten cada estación con un pincel humedecido en alcohol (puedes utilizar otro equipamiento), en el mismo orden que los colocaste. Colectarás las hormigas de las 16 estaciones de un polígono en un único frasco con alcohol al 80% (cualquier pote de compota te vale). Recalco: un polígono contendrá 16 estaciones y las hormigas de todas las estaciones de un mismo polígono se mezclarán en un único frasco. Por lo tanto, al finalizar el trabajo de campo deberás tener 10 frascos, uno por polígono.

En cada polígono registrarás la actividad de las hormigas, en función del número de ellas que encuentres (daré más detalles). También tomarás algunos datos "ambientales" básicos mediante formularios electrónicos. Fíjate en cuestiones relevantes para las hormigas, por ejemplo si se trata de una zona de paso de personas, si hay basurero cercano, si el suelo es de concreto o de tierra o de hierba, si conoces las especies arbóreas también anótalas, 

Identificarás, con mi ayuda, todos los individuos hasta nivel de género; si quieres llegar hasta especie es opción tuya, y existen buenas claves para ello. Dado que las hormigas son insectos sociales, utilizarás datos de presencia/ausencia, por lo que no contarás individuos. Tus análisis se basarán en incidencia. Más detalles en el aula. 

Nota: Si tienes experiencia, o quieres asumir retos, puedes implementar métodos de muestreo diferentes y más intensivos que el planteado. Ahora bien, para la asignatura, sólo es necesario implementar el mencionado.

### Código informático reproducible

Por correo electrónico, te enviaré asignaciones para desarrollar tu código reproducible.
Orientaré con ejemplos y soluciones de forma pública a través de `issues` que abrirás tú o yo en el GitHub. De esta forma las discusiones quedan disponibles para otras personas.
Al abrir un `issue` de GitHub debes plantear el problema al que te enfrentas, cómo has intentado resolverlo o qué soluciones has probado. Si se trata de cuestión relacionada con programación o análisis de datos, deberás facilitar **código reproducible y mensaje de error (si lo hubiere)**. Evita el típico comentario "da error", puesto que no conduce a nada.

### Exámenes

Bueno, sobre ésto tengo poco que decir, sólo que preferiría no evaluar contenido teórico.

## Fechas de evaluación

| Fecha | ¿Qué evaluaré? |
| - | - |
| 24 de Septiembre | **Manuscrito**: asignaciones sobre introducción y metodología realizadas <br/> **Trabajo de campo e identificación**: todas las asignaciones realizadas <br/> **Código informático reproducible**: lo asignado hasta la semana anterior |
| 22 de Octubre (medio término) | **Manuscrito**: asignaciones sobre resultados realizadas <br/> **Código informático reproducible**: lo asignado hasta la semana anterior <br/> **Examen parcial 1** |
| 19 de Noviembre | **Manuscrito**: asignaciones sobre resultados y discusión realizadas <br/> **Código informático reproducible**: lo asignado hasta la semana anterior |
| Diciembre, por precisar (final) | **Manuscrito**: todas las asignaciones completadas <br/> **Código informático reproducible**: todas las asignaciones completadas <br/> **Examen parcial 2** |

## Contenido teórico
1. Introducción e historia de la biogeografía. Brown y Lomolino (1998) capítulos 1 y 2. Okolodkov (2010) capítulos 1 y 2.
2. Contexto físico: la "plantilla" geográfica Smith y Smith (2007), segunda parte (capítulos 4 a 6). Brown y Lomolino (1998), capítulo 3.
3. Distribución de especies. Brown y Lomolino (1998), capítulo 4.
4. Distribución de comunidades. Brown y Lomolino (1998), capítulo 5.
5. Los cambios en la Tierra. Brown y Lomolino (1998), capítulo 6.
6. Especiación y extinción. Brown y Lomolino (1998), capítulo 8.
7. Dispersión. Brown y Lomolino (1998), capítulo 9.
8. Historia de los linajes. Brown y Lomolino (1998), capítulo 11.
9. Biogeografía insular. Brown y Lomolino (1998), capítulos 13 y 14

## Referencias bibliográficas
* Consulta tu buzón de correo.