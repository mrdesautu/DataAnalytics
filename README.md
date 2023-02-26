

 <h1 align=center> *PROYECTO INDIVIDUAL Nº1* </h1>

 # <h1 align=center>**`Machine Learning Operations (MLOps)`**</h1>


# <h1 align=center>**`AUTOR: MARTIN RODRIGO, MORALES`**</h1>


<p align="center">
<img src="https://user-images.githubusercontent.com/67664604/217914153-1eb00e25-ac08-4dfa-aaf8-53c09038f082.png"  height=300>
</p>

<br/>                          



+ Contexto: se nos solicito desde una en una start-up, que provee servicios de agregación de plataformas de streaming. Los siguientes requisitos.  

## **OBJETIVOS DEL TRABAJO:**


**`REALIZAR UN PROCESO DE ETL`**:
+ En este proceso se ejecutaron las solicitudes (y solo estas) que fueron solicitadas. Ya que el resultado y la corroboracion del mismo dependen de este proceso. se utilizó la libreria Pandas y sqldf para modificar el dataset recibido. Se tuvo en cuenta en todo momento el objetivo final del trabajo.  

**`CONFECCION DE QUERYS`**:
+ El proyecto solicita que se respondamos a ciertas consultas en base al dataset otorgado. Para la escritura de estas se tuvo que tener en cuenta el lenguaje en que estas serían escritas, ya que posteriormente se debian 'deployar'. Es por ello que se evito usar librerias no compatibles con el servidor desde el que se cargarían. Considerando las condiciones de su confeccion relacionadas a todo el proceso del proyecyo. Por lo que se montaron sin la libreria 'sqldf'. 

**`MONTAJE DE APIs`**:
+ En esta etapa se decidio utilizar la libreria FastAPI, la misma no requiere 'deckerizacion' (ya que realiza el proceso automaticamente), no debiendoe crear la imagen necesaria para correr nuestra API. Se utilizo Deta Space (es una computadora personal que vive en la nube, una "nube personal".)  [Deta] (https://deta.space/discovery/r/4gjwqpgrzpw7ssus) para  hacer el deployment de las aplicaciones. Pruebalas! El nombre de la Api generada es Martinapi, en la misma podras hacer las consultas de las querys mencionadas anteriormente. 
 
+ Deta Space: link de ingreso publico (https://deta.space/discovery/r/4gjwqpgrzpw7ssus)
+ Creator: mrdesautu


**`PROCESO DE UNA EDA`**:
+ Una vez finalizado este proceso se solicitó realizar un análisis exploratorio de los datos, buscando anomalias, correlaciones entre estos, y permitiendonos tener un acercamiento a la forma en que estos estan presentados. En este se realizó: categorización de los tipos de variables, graficas de los tipos de variables para su analisis, deteccion y tratamiento (entre ellos: outliers, valores extremos no compensados, ni explicados), unificacion de categorias sinonimicas, entre otras.  

**`MODELO DE MACHINE LERNING`**:
+ Esta etapa se dividio en dos momentos, ya que el modelo solicitado es un modelo de recomendacion de contenido. Este tipo de modelos son basados en - contenido y en - usuarios. encontrnadose tambien modelos hibridos, que consideran ambos factores. 
- Modelo de recomendacion basado en usuarios:
el primer modelo confeccionado se realizo en base a un usuario selecionado de la base de datos otorgada  [Dataset](https://drive.google.com/drive/folders/1b49OVFJpjPPA1noRBBi1hSmMThXmNzxn) en la carpeta 'ratings'. en ella se obtuvo los usuarios que habian puntuado peliculas similares, con puntajes similares, otorgandoles un 'peso' en función de la similitud que tenia su puntuación con nuestro usuario seleccionado. Se utilizó la correlación de Pearson como medida. en funcion de esta similitud y los valores a las puntuaciones, se realizó un Dataframe que ordenaba las peliculas mejores puntuadas por los usuarios más parecidos a nuestro usuario de prueba. En función de estos valores si el título que se ingresa es mayor a 4 (este nuemer fue determinado de manera arbitraria, las puntuaciones van de 0 a 5) una funcion comparativa recomendará la película.
- Modelo de recomendacion en base a contenido:
Luego de haber realizado el EDA sobre nuestras bases de datos, se consideró que seria interesante implementar un modelo hibrido, es por ello que se decisió hacer una estandarizacion de las variables categoricas utilizables (dentro del dataset de películas) que pudiesen ser utilizadas para un modelo de 'ML'. Se vincularon estas variables a el DataFrame que nos habia arrojado el modelo anterior, ya que se encontraba sectorizado a los usurarios con cierta correlacion a un usuario. El modelo utilizado fue el de K-vecinos, que mediante el analisis de este nos recomendo la utilizacion de 9 klausters de clasificacion.  Por limitaciones temporales y tecnicas no se pudo finalizar el 'workflow' para que cumpliese la operatividad de un modelo de MLOps.No por ellos se quiso dejar de mostrar el proceso, ya que implicó un desafio y aprendizaje significativo para el autor.
Se podria categorizar al proceso de MLops de nivel 0. ya que aunque el modelo se ajusta al usuario solicitado, no recibe retroalimentacion, ni se actualiza automaticamente.  


<br/>


**`VIDEO EXPLICATIVO-YOUTUBE`**:
(https://www.youtube.com/watch?v=oeb-aix2cig)
 

<br/>

## **LIBRERIAS UTILIZADAS:**

+ Pandas: Trabajo con bases de datos
+ Sqldf: Implementacion de lenguaje Sql en python
+ Numpy: Trabajo con arrays
+ Matplotlib: Creacion de graficos
+ Seaborn: Creacion de graficos
+ FastAPI: Creacion de APIs
+ Sklearn: Confeccion de modelos de Machine Learning
+ Math: Implementacion de operaciones matematicas complejas
+ Deta Space: es una computadora personal que vive en la nube, una "nube personal".

## Estructura del proyecto

| Nombre archivo | Contenido|
|----------------|----------|
| **main.py** |  Código que se subio a Deta Space, con las Querys solicitadas |
| **ETL.ipynb** | Limpieza realizada a los Datasets de las plataformas |
| **ETLrating.ipynb** | Limpieza realizada a los Datasets de los usuarios y sus puntuaciones |
| **requierements.txt** | Paqueterías utilizadas |
| **Modelo_de_ML.ipynb** | Modelo en base a correlacion de Pearson |
| **Modelo_de_ML2.ipynb** | Realizacion del EDA sobre el Dataset de las plataformas y montaje del modelo de ML-k-vecinos |
| **dfdef.csv** | Dataset de las 4 plataformas luego del proceso de ETL |
| **user_pearson.csv** | Dataset luego del modelo de recomendacion por Usuario |


+ dataset user Google Drive(https://drive.google.com/file/d/1EL_vLidUTe-33t8oK6NZtSYCjrcZxFxk/view?usp=sharing)


## ANALISIS DE FORTALEZAS Y DIFICULTADES PERSONALES

+ me resulto interesante comentar algo de mi experiencia en la realización de este trabajo

| FORTALEZAS | DIFICULTADES|
|----------------|----------|
|Constancia en una tarea atípica, busqueda de autosuperación| Aceptar las limitaciones técnicas, en la realización de tareas agenas a mis habilidades previas, buscar objetivos realizables |
| Consulta a compañeros, usuarios de internet, paginas en diferentes idiomas en busqueda de soluciones y alternativas para resolver un problema | Busqueda de caminos alternativos ante imposibilidades o tareas que se presentan como irresolubles, teniendo en cuenta conocimiento y tiempo disponible. Planificación. |
|Entender el proceso de práctica y aprendizaje como algo progresivo, buscando siempre superar mi nuvel actual. Sin realizar tareas que no comprendo por el hecho de 'cumplir'. buscando el aprendizaje como primer objetivo |Dificultades en la implementacion de librerias como scikit-surprise, por falta de conocimiento técnico especifico|


+  Gracias por su tiempo! espero haya disfrutado leer este trabajo tanto como yo realizarlo!
# EXITOS! 















  
  



