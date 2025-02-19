<style>
  .bold-title {
    font-weight: bold;
  }
</style>

# (PART\*) CURSO DE INGENIERÍA DE PROMPTS {-}


# (PART\*) BLOQUE 1 {-}

# Introducción

<style>
  .figure {
    text-align: center;
  }
  .figure .caption {
    text-align: center;
  }
</style>

<div class="justificar-texto">

La ingeniería de prompts se refiere a la creación de instrucciones o prompts dados a grandes modelos de lenguaje o LLMs, como CHTGPT, para obtener respuestas deseadas. Podemos pensar en la ingeniería de prompts como la elaboración de una receta para una comida deliciosa. Así como un chef experto selecciona y combina cuidadosamente los ingredientes para crear un plato delicioso, la ingeniería de prompts implica diseñar cuidadosamente los prompts que guían efectivamente al modelo hacia la producción de la salida deseada.

La ingeniería de prompts es esencial para producir buenas salidas porque la calidad de las respuestas que obtenemos depende en gran medida de los prompts proporcionados, donde los prompts de alta calidad llevan a respuestas de alta calidad y los prompts de baja calidad llevan a respuestas de baja calidad. En este curso, dominaremos los principios de la ingeniería de prompts y las mejores prácticas para construir sistemas de IA que aprovechen las capacidades de los modelos de lenguaje. Ver la Figura \@ref(fig:CURSO-111111).
</div>

<div class="figure" style="text-align: center">
<img src="FIG1.jpg" alt="Descripción gráfica del buen funcionamiento de Chat GPT. (Hecho con Python)." width="60%" />
<p class="caption">(\#fig:CURSO-111111)Descripción gráfica del buen funcionamiento de Chat GPT. (Hecho con Python).</p>
</div>




## Uso de la API de OpenAI

<div class="justificar-texto">
Profundizaremos en varios tipos de prompts y algunas aplicaciones comerciales y aplicaremos estas habilidades utilizando la aplicación de Shiny que he creado y de la cual dejo el link:


https://testestestest.shinyapps.io/TFGUOC/

La API de OpenAI permite la interacción con los modelos de OpenAI. Para usar la API, debemos obtener la clave iniciando sesión, visitando la página de claves API, creando una nueva clave secreta y copiándola para uso futuro. Si extraviamos nuestra clave, debemos eliminarla y generar una nueva.

La API proporciona varios puntos de acceso, pero el principal utilizado para chatear es la finalización del chat. Este punto de acceso es perfecto para tareas de turno único y diálogos interactivos, lo que lo hace ideal para aplicaciones conversacionales como asistentes virtuales y chatbots. Cada mensaje de la API tiene uno de los tres roles: usuario, asistente o sistema. Los mensajes del sistema proporcionan instrucciones para guiar el comportamiento del modelo durante una conversación. Los mensajes de usuario son prompts del usuario. Y los mensajes de asistente son las respuestas a los prompts del usuario. 

En el caso de mi aplicación si se quiere solo el rol de usuario se deberá utilizar la aplicación Prompt tal y como se muestra en la Figura \@ref(fig:CURSO-15).




<div class="figure" style="text-align: center">
<img src="FIG19.jpg" alt="Aplicación Usuario utilizada solo como rol de usuario." width="60%" />
<p class="caption">(\#fig:CURSO-15)Aplicación Usuario utilizada solo como rol de usuario.</p>
</div>


Si se quieren usar los 3 roles (usuario, asistente o sistema) pasaremos a utilizar la segunda aplicación llamada Usuario/(Sistema o asistente) ya que la entrada llamada SISTEMA DE PROMPT servirá tanto como Asistente o Sistema y la otra entrada es la del PROMPT DEL USUARIO tal y como se ve en la Figura \@ref(fig:CURSO-16).



<div class="figure" style="text-align: center">
<img src="FIG20.jpg" alt="Aplicación Usuario/(Sistema o Asistente) utilizada si requerimos de los tres roles." width="60%" />
<p class="caption">(\#fig:CURSO-16)Aplicación Usuario/(Sistema o Asistente) utilizada si requerimos de los tres roles.</p>
</div>

Recordemos que la API tiene parámetros de control útiles. Uno de ellos es la temperatura, un valor entre cero y dos que controla la aleatoriedad de la respuesta. Dos hace que la respuesta sea muy aleatoria y 0 la hace determinista. Otro parámetro es Max tokens, que controla la longitud deseada de la respuesta. 

## Nuestra primera interacción con ChatGPT

Supongamos que queremos preguntar “¿Qué es la ingeniería de prompts?” a través de la primera aplicación “Usuario” (Figura \@ref(fig:CURSO-17)). Para los parámetros de control, configuramos la temperatura en 0 para obtener respuestas deterministas, y especificamos Max tokens a 101. Observamos en la Figura 4 que a la pregunta propuesta primero devuelve una descripción, pero la última frase queda incompleta. Para evitar esto debemos mejorar el prompt y le decimos que lo defina en una sola frase y así lo hace. Por último, le hacemos la misma pregunta pero le especificamos que lo debe entender un niño de 5 años y que lo describa en dos frases. 
</div>


<div class="figure" style="text-align: center">
<img src="FIG21.jpg" alt="Aplicación Usuario para preguntar ¿Qué es la ingeniería de prompts?." width="60%" />
<p class="caption">(\#fig:CURSO-17)Aplicación Usuario para preguntar ¿Qué es la ingeniería de prompts?.</p>
</div>


<div style="text-align: center;">
<h3 style="font-weight: bold; text-align: center;">Video Tutorial: Introducción</h3>
  <iframe width="500" height="400" src="https://www.youtube-nocookie.com/embed/YlOZlJaoiOI?rel=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
