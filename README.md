# IRONHACK_ETL

<div style="text-align:center">
    <img src="./images/pulsera.png" alt="portada">
</div>

## Indice:
1.[✍️ Descripción](#descripcion)\
2.[🗒️ Desarrollo](#desarrollo)\
3.[💾 Database](#database)\
4.[📁 Estructura](#Estructura)


## Descripción:<a name="descripcion"/>

Tercer proyecto en Ironhack, donde se realizará un proceso ETL (Extract, Transform, Load), para empezar una base de datos donde se registrarn diversos festivales de música, así como los artistas participantes.


## Desarrollo:<a name="desarrollo"/>

Realizaremos el proceso siguiendo los siguientes pasos:

1- Desde la página de [Dod Magazine](https://www.dodmagazine.es/festivales/) obtendremos la información de un gran número de festivales que se celebran en España en el 2023. De esta página sólo obtendremos los nombres, ya que la estructura de la web, no permite una automatización del proceso de extracción para obtener datos de utilidad. Para la extracción de los datos usaremos la librería de Python Selenium

2- La página de [Songkick](https://www.songkick.com/es/festivals/) tiene una estructura más homogénea que nos permitirá obtener información de una forma más automatizada. Aquí obtendremos información de festivales de 16 paises, además de completar la información obtenida en el paso anterior. Para este proceso de extración nos apoyaremos de nuevo en Selenium y en la parelización de procesos.

3- Por último extraermos la información de los grupos que participen en los festivales que hemos localizado, usando la [API](https://developer.spotify.com/documentation/web-api) de Spotify. Completaremos la informacíon de cada grupo/artista con todos los datos que podamos obtener de la API


## Database: <a name="database"/>

Una vez transformados todos los datos que hayamos podido obtener, cargaremos la informacíon de una base de datos no relacional de Mongo. Los datos aquí obtendios se usaraán para un proyecto futuro, dicho proyecto está en fase de preparación por lo que las relaciones entre las diversas entidades aún no están establecidas, por esta razón es por lo que se ha optado por una opción de base de datos no relaiconal, en vez de una base de datos SQL.

## Estructura:<a name="Estructura"/>

```
root 
|__ data/               # Contiene todos los datos que se han recogido en el proyecto            
|   |__ db_mongo/       # Archivos .json con los datos ya cargados en la DB
|
|__ images/             # Contiene la imágenes que se han usado en el proyecto   
|
|__ jupyter/            # Alberga los 3 notebooks usados en el proyecto
|
|__ .gitignore          # Archivo gitignore     
|
|__ README.md           # Descripción del proyecto