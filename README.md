# Actividad Integradora 1
### Equipo 2:
Héctor Gibrán González Leal   [A01282278]  
Julio César García Flores     [A00516860]  
Gustavo De Los Ríos Alatorre  [A01410922]  
Jacobo Cruz Romero            [A01067040]  
David Garza Gonzalez          [A00820764]

En este notebook estaremos desarrollando una aplicación para realizar **sentiment analysis** sobre tweets tomados directamente de la API de Twitter, 
así como otras aplicaciones como clasificación de comentarios de Reddit y Youtube, además de lyrics de canciones de Genius.com.

## Para correr la aplicación:
Aquí se proporcionan todos los archivos relevantes para correr la aplicación. El archivo principal es el Jupyter Notebook, y los demás archivos son necesarios para
poder correr correctamente este Notebook. Dentro de este se proporcionan explicaciones del código que se realizó, así como el razonamiento detrás de la lógica que se
usó en el desarrollo de este proyecto.

Para correr el Notebook en Google Colab, este se debe cargar al ambiente, y además, los otros archivos (especialmente el requirements.txt) deben subirse al ambiente 
para que todo funcione adecuadamente.

## Funcionalidades adicionales
A contuación se describen las 3 funcionalidades adicionales que se implementaron:
### 1. Implementación de un modelo BERT
Siguiendo este [tutorial](https://www.tensorflow.org/tutorials/text/classify_text_with_bert), pudimos importar un modelo ya entrenado de BERT, y aplicar transfer learning
para especializar el modelo con nuestro set de datos. Una vez que se entrena el modelo, este se incorpora en el Vote Classifier para que participe en la clasificación de 
los textos.

### 2. Clasificación de comentarios de Youtube
Utilizando la [API de Youtube](https://developers.google.com/youtube/v3/docs/commentThreads/list) pudimos realizar requests para traer los comentarios de un video 
en especifico. Una vez que se tienen los comentarios, podemos procesarlos y obtener sus clasificaciones.

### 3. Clasificación de Lyrics de Genius.com
Utilizando la [API de Genius](http://genius.com/api-clients) pudimos realizar requests para traer lyrics de canciones. Estas luego son procesadas para poder sacar
clasificaciones por verso.

## Notas adicionales
- Todos los APIs mencionados requieren tokens o llaves, estos no se proporcionan en el Notebook, por lo que se tendrán que incluir para poder realizar exitosamente
las requests.
- Para obtener una llave para la API de Youtube se puede seguir el siguiente [tutorial](https://developers.google.com/youtube/registering_an_application?hl=es-419).
- Para una llave del API de Genius se puede revisar la primera parte de este [link](https://melaniewalsh.github.io/Intro-Cultural-Analytics/Data-Collection/Genius-API.html).
- Para la clasificación de audio, se proporcionan dos archivos de ejemplo en formato WAV que se pueden hacer. Nuevamente, sólo basta con cargarlos en el ambiente de
Colab para poder usarlos.
