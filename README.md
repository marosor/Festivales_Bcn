### Análisis de los datos de los festivales artísticos de Barcelona 2013-2022
===

Descripción:

Estudio de las características de los festivales culturales de la ciudad de Barcelona en el período comprendido entre 2013 y 2022.

Objetivos:

En este análisis exploratorio de datos me he enfocado en el panorama de los festivales barceloneses, atendiendo a las siguientes hipótesis:
* El sector público programa festivales de ámbitos desatendidos por los programadores privados <br>
* La mayoría de los festivales se concentra justo antes y después de los meses de calor y playa <br>
* Los festivales gratuitos son los que convocan mayor número de asistentes <br>
* En Barcelona ha crecido la tendencia a programar macrofestivales 

Para ello:<br>
* he analizado los primeros 50 festivales de cada año en función del número de asistentes
* los he estudiado según ámbito artístico, titularidad pública o privada, entrada gratuita o de pago, número de ediciones, més y época del año

Además, he obserbado la posible relación entre estas variables, año por año y en la década en conjunto, atendiendo a peculiaridades, elementos comunes, tendencias y excepciones.

La estructurade archivos que componen dicho análisis consta, entre otros, de:
##### Carpeta data
* Archivos originales en formato csv, uno por cada año del festival
* Archivos csv procesados listos para analizar
##### Carpeta notebooks
* Funciones de análisis
* Preparación de datos
* Análisis univariable (uno diferente por cada año)
* Análisis bivariable
* Análisis década
* Análisis y Resultados EDA
* Anexo
##### Carpeta docs
* Memoria EDA Festivales
* Presentación .ppt Cómo y cuánto se festivalea en Barcelona

Tecnologías:
El presente EDA se ha realizado mediante el uso de las siguientes librerías de Python:
* pandas
* numpy
* matplotlib
* seaborn

La fuente de los datos es el propio [Ayuntamiento de Barcelona en su portal de datos abiertos](https://opendata-ajuntament.barcelona.cat/data/es/dataset/dades-festivals)

## Paper Information
- Title:  Análisis de los datos de los festivales artísticos de Barcelona 2013-2022
- Authors:  Marcela Rosemberg Oro
