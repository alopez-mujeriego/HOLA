# Creación de Salidas Estructuradas y Prompts Condicionales

<style>
  .figure {
    text-align: center;
  }
  .figure .caption {
    text-align: center;
  }
</style>

<div class="justificar-texto">

## Generación de Tablas

Nos enfocaremos ahora en crear salidas estructuradas y usar prompts condicionales. Los modelos de lenguaje no generan naturalmente salidas estructuradas a menos que se les instruya explícitamente. Sin embargo, hay ocasiones en las que necesitamos que la salida se presente en una tabla, lista, párrafo estructurado o un formato personalizado que elijamos. Veamos cómo tratar cada uno de estos casos.
Comenzamos con tablas. Al pedirle al modelo que genere una tabla, debemos mencionar claramente las columnas esperadas. Por ejemplo, podemos instruir al modelo para crear una tabla con 5 películas adecuadas para los amantes de la acción y definir explícitamente las columnas deseadas, título y calificación. En consecuencia, vemos cómo la salida cumple con nuestros requisitos en la Figura \@ref(fig:CURSO-25).





<div class="figure" style="text-align: center">
<img src="FIG25.jpg" alt="Especificando en el prompt que queremos generar una tabla en formato html." width="60%" />
<p class="caption">(\#fig:CURSO-25)Especificando en el prompt que queremos generar una tabla en formato html.</p>
</div>

## Generación de Listas

Otro formato para pedir es una lista. Esta estructura es útil para enumeraciones. Por ejemplo, pedimos al modelo que genere una lista con los nombres de las cinco mejores ciudades para visitar. La salida es una lista numerada de ciudades. Debemos mencionar explícitamente los requisitos específicos sobre cómo debe formatearse la lista de salida en el prompt (Figura \@ref(fig:CURSO-26)). 


<div class="figure" style="text-align: center">
<img src="FIG26.jpg" alt="Especificando en el prompt que queremos generar una lista en formato html." width="60%" />
<p class="caption">(\#fig:CURSO-26)Especificando en el prompt que queremos generar una lista en formato html.</p>
</div>

## Párrafos Estructurados


Podemos querer obtener párrafos con una estructura específica al generar texto. En este caso, debemos mencionar explícitamente los requisitos de formato en el prompt. Por ejemplo, podemos pedir al modelo que genere un párrafo estructurado con títulos y subtítulos claros sobre los beneficios del ejercicio. En la Figura \@ref(fig:CURSO-27) vemos cómo la salida está formateada con tres títulos: Salud física, Salud mental y Bienestar General.


<div class="figure" style="text-align: center">
<img src="FIG27.jpg" alt="Generación de un párrafo estructurado con títulos y subtítulos claros en formato html." width="60%" />
<p class="caption">(\#fig:CURSO-27)Generación de un párrafo estructurado con títulos y subtítulos claros en formato html.</p>
</div>


## Formatos Personalizados

También podemos solicitar un formato de salida personalizado. Supongamos que queremos generar un título para un texto dado y presentar la salida en un estilo particular. Podemos simplificar este proceso desglosando nuestro prompt en partes distintas. Por ejemplo, comenzamos definiendo el texto de entrada, la apertura de una historia de cuento de hadas sobre un niño llamado David, y las instrucciones del modelo para generar un título apropiado. Luego especificamos la cadena de formato de salida, instruyendo al modelo para que formatee el texto y el título de una manera específica para la salida. Finalmente, combinamos las instrucciones, el formato de salida y el texto de entrada en el prompt final. La salida en la Figura \@ref(fig:CURSO-28) cumple con nuestros requisitos al darnos un título sobre las aventuras de David.


<div class="figure" style="text-align: center">
<img src="FIG28.jpg" alt="Solicitando un formato de salida personalizado." width="60%" />
<p class="caption">(\#fig:CURSO-28)Solicitando un formato de salida personalizado.</p>
</div>

## Prompts Condicionales

A veces podemos querer incorporar alguna lógica o condiciones en nuestros prompts. En este caso, usamos prompts condicionales. Si una condición es verdadera, realiza X, de lo contrario realiza Y. Supongamos que queremos que el modelo sugiera un título para un texto proporcionado. Sin embargo, solo queremos que el modelo haga esto si el texto está en español. Para hacer eso, mencionamos explícitamente esta condición en el prompt. Si el texto está en otro idioma, le decimos al modelo que informe a los usuarios que solo entiende español. Ahora, para un texto en francés que describe mi estación favorita, la salida será “Solo entiendo español”. Podemos incorporar múltiples condiciones en nuestro prompt. Por ejemplo, podemos decirle al modelo que genere títulos solo para textos en español que contengan la palabra clave tecnología. Si el texto está escrito en español, verificamos si contiene la palabra clave. Si lo hace, el modelo sugiere un título. De lo contrario, responde con “palabra clave no encontrada”. Se puede ver el resultado con las respuestas esperadas en la Figura \@ref(fig:CURSO-29).


<div class="figure" style="text-align: center">
<img src="FIG29.jpg" alt="Solicitando un formato de salida personalizado. " width="60%" />
<p class="caption">(\#fig:CURSO-29)Solicitando un formato de salida personalizado. </p>
</div>




<div style="text-align: center;">
<h3 style="font-weight: bold; text-align: center;">Video Tutorial: Creación de salidas estructuradas y prompts condicionales</h3>
  <iframe width="500" height="400" src="https://www.youtube-nocookie.com/embed/ut1HRzjuRUM?rel=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

</div>

