# Prompting de Varios Pasos


<style>
  .figure {
    text-align: center;
  }
  .figure .caption {
    text-align: center;
  }
</style>

<div class="justificar-texto">

## Introducción al Prompting de Varios Pasos

Exploremos el prompting de varios pasos, que guía el comportamiento del modelo para generar salidas efectivas. El prompting de varios pasos es una técnica donde desglosamos un objetivo final en una serie de pasos pequeños. El modelo tiene que pasar por cada paso antes de dar la salida final. Estos pasos facilitan las cosas para el modelo y aumentan las probabilidades de éxito. Las tareas secuenciales como generar un texto coherente a partir de un esquema dado, se benefician de los prompts de varios pasos ya que a menudo necesitan completar una serie de pasos en un orden específico. Las tareas cognitivas como evaluar la corrección de una solución también utilizan prompts de varios pasos ya que implican procesamiento cognitivo, resolución de problemas y toma de decisiones. Podemos pensar en los prompts de varios pasos como mapas del tesoro, así como un mapa del tesoro proporciona una secuencia de pistas e instrucciones para descubrir tesoros ocultos, un prompt de varios pasos descompone una tarea compleja en pasos más pequeños y manejables que el modelo debe seguir para alcanzar el resultado deseado.

## Ejemplos de Prompting de Varios Pasos

Supongamos que queremos escribir un blog de viajes. Podríamos comenzar con un prompt de un solo paso, pidiendo al modelo que cree todo el blog sin detalles adicionales. En este ejemplo, el modelo generará texto sobre un viaje aleatorio a través de un país, Islandia, con un itinerario día por día. Para dar más detalles sobre lo que debe cubrirse en el blog, creamos un prompt de varios pasos que pide al modelo que lo escriba en tres pasos: presentar el destino, compartir aventuras personales y resumir el viaje. Nótese que la elección del destino es insignificante y el enfoque está solo en la estructura del blog. El modelo genera un blog de viajes coherente según nuestras instrucciones, con una introducción a Japón, una aventura y el resumen. Ver Figura \@ref(fig:CURSO-34).


<div class="figure" style="text-align: center">
<img src="FIG34.jpg" alt="Ejemplo de prompting de varios pasos." width="60%" />
<p class="caption">(\#fig:CURSO-34)Ejemplo de prompting de varios pasos.</p>
</div>

## Aplicaciones Cognitivas del Prompting de Varios Pasos


Otra aplicación del prompting de varios pasos son las tareas cognitivas como analizar la corrección de una solución. Supongamos que necesitamos verificar la corrección de un código en Python que contiene funciones que implementan cálculos básicos como suma, resta, multiplicación y división. Supongamos que la cadena del calculador contiene el contenido de los archivos que queremos verificar. Como se observa, incluye funciones que aceptan 2 números como entrada y realizan suma, resta, multiplicación o división, devolviendo los resultados correspondientes. Como punto de partida, podríamos considerar elaborar un prompt de un solo paso que encargue al modelo evaluar la corrección del código proporcionado. Aunque el modelo responde con un “sí”, diciéndonos que el código es correcto, no sabemos cómo se realizó la evaluación. Podríamos necesitar evaluar según criterios específicos o conocimientos del dominio. Por ejemplo, aunque la sintaxis es correcta, la función de división no maneja la división por cero, y podríamos querer que esto se considere en la evaluación. Para lograr eso, usamos un prompt de varios pasos donde en el paso uno verificamos la corrección de la sintaxis y en el paso dos verificamos si se maneja la división por cero. Después de estos cambios, la salida del modelo da retroalimentación sobre cada paso y nos dice que la sintaxis es correcta, pero la división por cero no se maneja.


## Diferencias entre Prompts de Varios Pasos y Cadena de Pensamiento

Revisemos las diferencias entre los prompts de varios pasos y los prompts de cadena de pensamiento. Mientras que los pasos y los disparos juegan roles cruciales en el control del comportamiento del modelo, los pasos son instrucciones que le dicen explícitamente al modelo qué hacer. Actúan como una hoja de ruta para el modelo al proporcionar orientación específica.

Los disparos son preguntas y respuestas de ejemplo de las que el modelo aprende. Demuestran cómo el modelo debe responder a ciertas entradas. El modelo observa estos ejemplos y aprende a generalizar a partir de ellos.



<div style="text-align: center;">
<h3 style="font-weight: bold; text-align: center;">Video Tutorial: Prompting de varios pasos</h3>
  <iframe width="500" height="400" src="https://www.youtube-nocookie.com/embed/Wbikyqy5tjw?rel=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>


</div>

