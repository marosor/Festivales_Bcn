# Análisis de los festivales artísticos de Barcelona, 2013–2022

Exploratory Data Analysis (EDA) sobre la oferta, las características y la asistencia de los festivales artísticos de Barcelona durante el periodo 2013–2022.

## Sobre el proyecto

Este proyecto explora qué nos pueden contar los datos abiertos sobre el **sector de los festivales artísticos de Barcelona**.

El análisis parte de los registros anuales publicados por el Ajuntament de Barcelona y combina exploración univariable, análisis de relaciones entre variables y análisis longitudinal de la década.

El objetivo no es únicamente describir los datos, sino **explorar patrones, contrastar algunas intuiciones iniciales y generar nuevas preguntas a partir de los resultados**.

---

## Preguntas e hipótesis

El análisis se estructuró alrededor de cuatro hipótesis iniciales:

**H1 · Público y privado**  
> El sector público programa ámbitos menos atendidos por la iniciativa privada.

**H2 · Temporalidad**  
> La mayoría de los festivales se concentra alrededor del calor y la playa.

**H3 · Gratuidad**  
> Los festivales gratuitos convocan un mayor número de asistentes.

**H4 · Escala**  
> Ha aumentado la tendencia a programar macrofestivales.

Las hipótesis no se plantearon como afirmaciones que hubiera que demostrar, sino como **intuiciones que el análisis podía confirmar, matizar o cuestionar**.

### Resultado del contraste

| Hipótesis | Resultado |
|---|---|
| **H1 · Público y privado** | **Matizada** |
| **H2 · Temporalidad** | **Matizada** |
| **H3 · Gratuidad** | **No confirmada** |
| **H4 · Escala** | **Confirmada con matices** |

---

# Datos

### Fuente

**Ajuntament de Barcelona — portal de datos abiertos**

El proyecto utiliza diez recursos anuales correspondientes al periodo **2013–2022**.

Los datasets contienen información sobre los festivales, incluyendo variables como:

- año
- festival
- ámbito artístico
- edición
- titularidad
- asistencia
- fecha de inicio
- entrada

Además de estas variables originales, durante el proceso de preparación se construyeron variables derivadas necesarias para el análisis.

---

# Construcción del universo de análisis

El registro original contiene eventos y categorías que no eran comparables con el concepto de festival utilizado en este estudio.

Por ello, el primer paso consistió en **definir el universo analítico**.

Se aplicaron criterios de selección y exclusión y, posteriormente, se conservaron los festivales que cumplían los criterios definidos de **popularidad y continuidad** durante el periodo.

El universo final está formado por:

> **67 festivales**

Este universo debe interpretarse como el **universo analítico del proyecto**, no como un inventario exhaustivo de todos los festivales de Barcelona.

---

# Preparación y transformación de los datos

Los diez datasets anuales fueron procesados mediante un flujo común de preparación.

Entre las operaciones realizadas se encuentran:

- limpieza de registros;
- exclusión de categorías no pertinentes;
- homogeneización de variables;
- transformación de fechas;
- cálculo de variables temporales;
- preparación de la variable de asistencia;
- construcción de la variable de entrada;
- creación de categorías para analizar la escala de los festivales.

### Variables derivadas

Durante el proyecto se construyeron, entre otras:

**Mes · Estación · Asistentes · Entrada**

La variable **Entrada** fue construida a partir de información adicional recopilada sobre los festivales para poder distinguir entre diferentes modalidades de acceso.

---

# Escala de los festivales

Para analizar los festivales según su volumen de asistencia se construyeron cuatro categorías:

**Pequeño · Mediano · Grande · Macro**

La categoría **macrofestival** es una clasificación analítica construida durante el proyecto.

Su umbral se definió mediante el **percentil 85 (P85) de asistencia**.

---

# Cómo se realizó el EDA

El análisis se desarrolló en diferentes niveles.

### 1. Análisis univariable

Se realizó una exploración independiente de cada año para conocer las distribuciones de las variables, detectar particularidades y formular posibles preguntas.

### 2. Análisis bivariable

Se exploraron relaciones entre variables, entre ellas:

- ámbito artístico × titularidad
- ámbito artístico × entrada
- ámbito artístico × asistencia
- temporalidad × ámbito

### 3. Análisis de década

Los diez años se integraron para estudiar la evolución del fenómeno durante el periodo completo.

En los datasets anuales, **cada fila representa un festival de ese año**.

En el dataset consolidado de la década, **cada fila representa un festival del universo analizado**, utilizando los datos agregados correspondientes al periodo.

No existen varios registros del mismo festival para un mismo año.

### 4. Análisis y resultados

Finalmente se contrastaron las hipótesis iniciales y se sintetizaron los principales patrones, matices y limitaciones encontrados.

---

# Principales resultados

### La música concentra gran parte del fenómeno

La música es el ámbito con mayor presencia y concentra también una parte muy importante de la asistencia.

### La temporalidad depende de cómo agrupamos los datos

El patrón observado cambia según trabajemos con **meses o estaciones**.

Esta diferencia constituye también un aprendizaje metodológico: la forma en que construimos y agrupamos una variable condiciona la lectura que podemos hacer de los datos.

### Público y privado presentan composiciones diferentes

La iniciativa privada domina cuantitativamente el universo analizado y aparecen diferencias en la composición de los ámbitos según titularidad.

### La gratuidad no implica automáticamente mayor asistencia

Los datos no confirman la hipótesis de que los festivales gratuitos convoquen necesariamente a más asistentes.

### Los festivales de mayor escala ganan peso

La presencia de festivales de mayor escala aumenta durante parte de la década, aunque la pandemia interrumpe esta evolución y la recuperación posterior no alcanza el máximo previo.

---

# Qué permiten observar los datos

El análisis permite estudiar:

**oferta · asistencia · temporalidad · ámbito · titularidad · acceso · escala · evolución**

Pero estas variables no permiten, por sí solas, explicar:

**causas · motivaciones · preferencias individuales · impacto cultural/económico/territorial · causalidad**

Encontrar una asociación o un patrón no significa explicar por qué se produce.

> **Un patrón observado no equivale a una explicación.**

---

# Nuevas preguntas

Una de las funciones del EDA en este proyecto ha sido generar nuevas preguntas a partir de los resultados.

Entre ellas:

- ¿Qué explica la concentración temporal de los festivales?
- ¿Por qué algunos ámbitos movilizan más asistencia que otros?
- ¿Qué caracteriza a los festivales que alcanzan mayor escala?
- ¿Qué cambió durante la pandemia y la recuperación posterior?
- ¿Qué otras fuentes de datos permitirían explicar los patrones observados?

El análisis exploratorio funciona así como un **punto de partida para nuevas investigaciones**, no necesariamente como un punto final.

---

# Estructura del repositorio

```text
SRC/
│
├── data/
│   ├── 2013_festivals-assistents.csv
│   ├── 2014_festivals-assistents.csv
│   ├── 2015_festivals-assistents.csv
│   ├── 2016_festivals-assistents.csv
│   ├── 2017_festivals-assistents.csv
│   ├── 2018_festivals-assistents-order-name.csv
│   ├── 2019_festivals-assistents-order-name.csv
│   ├── 2020_festivals-assistents-order-name.csv
│   ├── 2021_festivals-assistents-order-name.csv
│   ├── 2022_festivals-assistents-order-name.csv
│   ├── festivals_bcn_13_procesado.pkl
│   ├── festivals_bcn_14_procesado.pkl
│   ├── festivals_bcn_15_procesado.pkl
│   ├── festivals_bcn_16_procesado.pkl
│   ├── festivals_bcn_17_procesado.pkl
│   ├── festivals_bcn_18_procesado.pkl
│   ├── festivals_bcn_19_procesado.pkl
│   ├── festivals_bcn_20_procesado.pkl
│   ├── festivals_bcn_21_procesado.pkl
│   └── festivals_bcn_22_procesado.pkl
│
├── docs/
│   ├── Memoria_EDA_Festivales.ipynb
│   └── Presentacion_Como_cuanto_se_festivalea_en_Barcelona
│
├── images/
│   └── portada.jpg
│
├── notebooks/
│   ├── Analisis_bivariable.ipynb
│   ├── Analisis_decada.ipynb
│   ├── Analisis_univariable_2013.ipynb
│   ├── Analisis_univariable_2014.ipynb
│   ├── Analisis_univariable_2015.ipynb
│   ├── Analisis_univariable_2016.ipynb
│   ├── Analisis_univariable_2017.ipynb
│   ├── Analisis_univariable_2018.ipynb
│   ├── Analisis_univariable_2019.ipynb
│   ├── Analisis_univariable_2020.ipynb
│   ├── Analisis_univariable_2021.ipynb
│   ├── Analisis_univariable_2022.ipynb
│   ├── Analisis_y_Resultados_EDA_Festivales.ipynb
│   ├── Anexo.ipynb
│   ├── Funciones_de_analisis.ipynb
│   └── Preparacion_datos.ipynb
│
└── README.md
```

---

# Recorrido recomendado

Si quieres seguir el proceso completo del análisis, se recomienda este recorrido:

### 1. Preparación de los datos

[Preparacion_datos.ipynb](notebooks/Preparacion_datos.ipynb)

Este notebook contiene el proceso de preparación y transformación de los datos antes del análisis.

↓

### 2. Exploración univariable

La exploración inicial se realizó año por año:

- [Analisis_univariable_2013.ipynb](notebooks/Analisis_univariable_2013.ipynb)
- [Analisis_univariable_2014.ipynb](notebooks/Analisis_univariable_2014.ipynb)
- [Analisis_univariable_2015.ipynb](notebooks/Analisis_univariable_2015.ipynb)
- [Analisis_univariable_2016.ipynb](notebooks/Analisis_univariable_2016.ipynb)
- [Analisis_univariable_2017.ipynb](notebooks/Analisis_univariable_2017.ipynb)
- [Analisis_univariable_2018.ipynb](notebooks/Analisis_univariable_2018.ipynb)
- [Analisis_univariable_2019.ipynb](notebooks/Analisis_univariable_2019.ipynb)
- [Analisis_univariable_2020.ipynb](notebooks/Analisis_univariable_2020.ipynb)
- [Analisis_univariable_2021.ipynb](notebooks/Analisis_univariable_2021.ipynb)
- [Analisis_univariable_2022.ipynb](notebooks/Analisis_univariable_2022.ipynb)

↓

### 3. Análisis bivariable

[Analisis_bivariable.ipynb](notebooks/Analisis_bivariable.ipynb)

Exploración de relaciones entre diferentes variables del dataset.

↓

### 4. Análisis de la década

[Analisis_decada.ipynb](notebooks/Analisis_decada.ipynb)

Integración de los datos para estudiar la evolución de los festivales durante el periodo 2013–2022.

↓

### 5. Análisis y resultados

[Analisis_y_Resultados_EDA_Festivales.ipynb](notebooks/Analisis_y_Resultados_EDA_Festivales.ipynb)

Síntesis de los principales resultados del análisis y contraste de las hipótesis planteadas.

---

# Recursos complementarios

### Funciones de análisis

[Funciones_de_analisis.ipynb](notebooks/Funciones_de_analisis.ipynb)

Funciones utilizadas durante el procesamiento y análisis.

### Anexo

[Anexo.ipynb](notebooks/Anexo.ipynb)

Material complementario del análisis.

### Memoria

[Memoria_EDA_Festivales.ipynb](docs/Memoria_EDA_Festivales.ipynb)

Documentación adicional del proyecto.

### Presentación

[Presentación del proyecto](docs/)

Presentación de los principales resultados del EDA.

---

# Tecnologías

El análisis se ha desarrollado en **Python**, utilizando principalmente:

- [pandas](https://pandas.pydata.org/)
- [NumPy](https://numpy.org/)
- [Matplotlib](https://matplotlib.org/)

---

# Documentación

El repositorio incluye:

- datos originales de 2013–2022;
- datos procesados;
- notebooks de preparación;
- notebooks de análisis univariable;
- análisis bivariable;
- análisis longitudinal de la década;
- síntesis de resultados;
- memoria del proyecto;
- presentación del análisis.

---

# Autoría

**Marcela Rosemberg Oro**

Exploratory Data Analysis aplicado al sector cultural.
