# ¿Cómo crear un repositorio con tu asignación y, posteriormente, cómo hacerla?

## Crea un repositorio con tu asignación:

1. Desde el navegador, entra en [Github](https://github.com/) e [inicia sesión](https://github.com/login) con tu cuenta. Si usas una PC pública o compartida, es preferible que inicies el navegador en modo incógnito. Si no tienes cuenta de Github, [crea una](https://github.com/join). Ésta será la cuenta que usarás durante el curso.
2. Ve a tu buzón de correo y, en el mensaje enviado por el profesor (podría caer en spam), haz clic en el vínculo (será algo tal que https://<i></i>classroom.github.com/...).
3. Al hacer clic, el navegador te dirigirá a aceptar la asignación (te pedirá que inicies tu cuenta de Github si aún no lo has hecho). Presiona `Accept this assignment`. Cuando quieras volver a tu asignación, puedes usar este vínculo del mensaje de invitación.
4. Automáticamente se creará, en tu cuenta de Github, un repo conteniendo tu asignación. Listo, tienes ya un repo con tu asignación, donde harás tus actualizaciones.

* Nota: estos 4 pasos se ejecutan una sola vez

## Haz tu asignación:

Elige una de dos alternativas en función del tipo de asignación:

A. Usa la interfaz web de GitHub si no vas a ejecutar código. Por ejemplo, usa esta alternativa si vas a hacer un documento de texto en Markdown que contenga tus preguntas de investigación ([tutorial sobre Markdown](https://www.youtube.com/watch?v=y6XdzBNC0_0)). Este interfaz es bastante sencillo. Sigue estos pasos:

1. Inicia una sesión en GitHub con tu usuario/contraseña.
2. Localiza el repo que contiene la asignación, donde podrás hacer cambios a un archivo existente o crear uno nuevo (dependerá de lo asignado):
    1. Para actualizar un archivo existente, haz clic sobre su nombre y luego en el lápiz del encabezado. Haz los cambios que correspondan según lo asignado.
    2. Para crear un nuevo documento, presiona el botón `Create new file`, se creará un documento en blanco, ponle un nombre en la caja `Name your file` y, en el documento, añade el texto que corresponda según lo asignado.
3. Al terminar de añadir texto/hacer cambios, ve al final de la página y presiona `Commit changes`.

Más detalles, en el aula.

B. Utiliza RStudio si vas a ejecutar código de R, como por ejemplo crear objetos de R, importar datos a R, analizar matrices de comunidad, calcular diversidad, crear gráficos de ordenación, hacer análisis de agrupamiento (*cluster analysis*) o tareas similares. Sigue estos pasos:

1. Abre RStudio. Recomiendo utilizar el servidor de RStudio habilitado por el profesor, para lo cual sólo necesitas una conexión a internet y una computadora con navegador. Alternativamente, puedes instalar y ejecutar RStudio Desktop en una computadora de tu preferencia (hay muchos tutoriales disponibles en línea). En cualquier caso, lo importante es que actualices tus cambios en el repo de Github periódicamente (actualiza mientras avanzas, no esperes hasta el final). En el último paso explico cómo actualizar tu repo de GitHub según los cambios que hayas hecho localmente.
2. Crea un proyecto mediante `File>New Project` en RStudio. Esto llamará la ventana `Create Project`. Elige la opción `Version Control`, lo cual hará avanzar automáticamente hacia la Ventana `Create Project from Version Control` automáticamente.
3. En la ventana `Create Project from Version Control`, elige `Git`. Esto hará avanzar automáticamente hacia la ventana "Clone Git Repository". Para rellenar la caja `Repository URL` necesitas ir a tu repo de asignación.
4. Ve al navegador y, en tu repo de asignación, copia la URL del repo presionando el botón verde `Clone or download` ![](img/bt_clone_or_download.png) y luego el botón `Copiar URL del repo` ![](img/bt_copy_repo_url.png). La URL se encuentra ahora en el clipboard.
5. Regresa a RStudio. En la caja `Repository URL`, pega la URL que tienes en el portapapeles (en Linux y Windows, `Ctrl+V`). Dicho texto será algo tal que https://<i></i>github.com/biogeografia-master/<nombredelrepo>.git.
6. En la caja `Project directory name`, puedes dejar el valor por defecto, que será el mismo nombre del repo (por ejemplo, `unidad-0-asignacion-0`). Este será el nombre del directorio donde se clonará el repo.
7. En la caja `Create project as subdirectory of`, debes elegir el lugar donde se colocará el directorio que contendrá el repo. Si lo haces en el servidor RStudio habilitado por el profesor, puedes dejar en este cuadro la opción que te aparece por defecto, que es la virguilla (`~`), y significa `Carpeta personal`, cuya ruta global en el servidor es `/home/<nombredeusuarioenelservidor>/`. Por ejemplo, el repo quedará en la siguiente ruta: `/home/<nombredeusuarioenelservidor>/<nombredelrepo`.
8. Presiona el botón `Create Project`. Automáticamente, RStudio clonará el repositorio de tu asignación localmente. Esta copia local puede ser editada mediante el editor de RStudio y sincronizada con el repo remoto.
9. Al igual que en el interfaz web de GitHub, a partir de este punto, puedes actualizar un archivo existente en tu repo o crear uno nuevo. Todo dependerá de la naturaleza de la asignación:
    1. Para actualizar un archivo existente, abre la pestaña `Files` (revisa los paneles de RStudio) y cliquea sobre el nombre del archivo que te interesa editar. Haz los cambios que correspondan según lo asignado. No te olvides de guardar inmediatamente cualquier cambio que hagas, pero ten en cuenta que estarás guardando sólo la copia local, no la del repo de GitHub (más adelante verás como actualizar el repo remoto).
    2. Para crear un nuevo documento, presiona el botón `Create new file`, se creará un documento en blanco, ponle un nombre en la caja `Name your file` y, en el documento, añade el texto que corresponda según lo asignado.
10. Finalmente, para actualizar cambios desde el repo local al remoto, haz lo siguiente:
    1. Abre la pestaña `Git` (revisa los paneles de RStudio). Si has hecho cambios o has añadido archivos, te encontrarás con una lista de archivos cambiados o añadidos. Haz clic en la marca de cotejo de cada uno de los archivos que te interesa actualizar con el repo remoto.
    2. Presiona el botón `Commit`, lo cual abrirá la ventana de `Review Changes`. Aquí puedes revisar los cambios que has hecho a cada archivo. El texto añadido aparece sombreado en verde, y el borrado en rojo.
    3. En la caja `Commit message` escribe un mensaje de que resuma el conjunto de cambios, por ejemplo, `actualizado archivo de asignación, añadido archivo de script`.
    4. Presiona el botón `Commit`. Con esto, los cambios pasan al `Stage`, pero aún no se han sincronizado con el repo remoto. Aparecerá un cuadro de diálogo informando los cambios realizados, algo como ésto:
    ```[master 9ac56dd] assignment md updated
 1 file changed, 19 insertions(+), 5 deletions(-)```
    5. Presiona el botón `Close`. Volverás al cuadro `Review Changes`. Presiona el botón `Push`. Automáticamente te aparecerá un cuadro para escribir tu usuario y otro para escribir tu contraseña. Si todo sale bien, los cambios se habrán sincronizado y te aparecerá un mensaje de confirmación que te informa sobre la actualización de la rama máster, algo tal que esto:
    <div><img/master_branch_updated.png></div>
11. Si has llegado hasta este punto, ¡Felicidades! Pasaste varios mundos y ya estás preparado/a para realizar tus asignaciones de manera fluida.

¡Servicio público de radio guarachita! No utilices el servidor de RStudio habilitado por el profesor como repositorio central. Por razones de presupuesto y operativas, el servidor está configurado con un mínimo de seguridad. Por lo tanto, los cambios que hagas a tus repos de asignaciones desde el servidor, debes actualizarlos inmediatamente en el repo remoto de GitHub. Aviso emitido.


