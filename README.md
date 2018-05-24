# diccionario
Diccionario del diablo, ejemplo AJAX con jQuery

En el archivo devil.js se encuentra el procesamiento de 2 tipos de peticiones AJAX:

La primera es como lo que se ha trabajado en clase, se emplea .load

La segunda realiza una petición AJAX a un archivo en formato JSON (JavaScript Object Notation), donde todo se almacena en arreglos del tipo:

{ "name":"John", "age":31, "city":"New York" }

Dentro del mismo archivo, especial atención a la instrucción: 

event.preventDefault();, 

Ya que al revisar el fuente HTML, cada letra del diccionario es una etiqueta del tipo <a href="letter-a.html">A</a>, sin embargo preventDefault() evita que se lleve a cabo la acción de ir a letter-a.html y en su lugar se lleva a cabo la acción indicada a continuación, es decir, cargar el elemento html o json indicado.

En ambos casos, el contenido se carga en el div que tiene el id "dictionary", sólo que para el caso del archivo json, es necesario darle formato HTML antes de imprimilo en pantalla.

La ventaja de json sobre HTML, es que los datos pesan menos y es sólo hasta el momento de cargar el elemento que se "genera al vuelo" el HTML que será mostrado.

La idea es completar el diccionario (sólo funcionan las letras A y B) empleando otras formas de realizar peticiones AJAX, por ejemplo con .get, .post o cualquier otro elemento de jQuery, disponibles en:

http://api.jquery.com/category/ajax/
