# Analisis exploratorio sobre disparidades regionales en salud de Argentina

## Objetivo del Proyecto

El objetivo de este trabajo será realizar un analisis de las disparidades regionales en la salud.    
Se analizará por regiones si existen diferencias significativas en la prevalencia de enfermedades crónicas no transmisibles como diabetes, hipertensión y colesterol y las causas que llevan a estas diferencias (si existieran) en dichas regiones.

## Origen de los datos

Para el análisis se utilizarán los datos de la "Encuesta Nacional de Factores de Riesgo" realizada por el INDEC a adulos mayores de 18 años en Argentina.  
Para el análisis actual se utilizarán los resultados del año 2018:   
[Resultado encuesta](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://www.indec.gob.ar/ftp/cuadros/sociedad/cuadros_preliminares_enfr_2018.xls&ved=2ahUKEwiSjvbLl8yGAxUQppUCHbLeAQ4QFnoECDIQAQ&usg=AOvVaw2yheKKYGABUq8ZHkNbiPEI) 
[encuesta realizada]( https://www.indec.gob.ar/ftp/cuadros/sociedad/cuestionario_enfr_2018.pdf)

## Organización de los archivos

### Fuentes externas: 

1. friesgo2018.txt:  dataset original resultado de la encuesta
2. manual de encuesta.pdf: manual que explica como fueron adquiridos los datos y el significado de cada columna y valores

### Segunda Pre-entrega

1. entrega2.ipynb: notebook con análisis exploratorio de los datos que se presentó como preentrega 2
2. df_friesgo_reduc.csv: csv generado luego de la limpieza de datos en la preentrega 2

### Tercer Pre-entrega

Se debe aclarar que para esta nueva pre-entrega se realizó un nuevo análisis exploratorio con las correcciones sugeridas en la revisión de la pre-entrega 2 y orientando el análisis a los objetivos buscados por lo que las notebooks de la pre-entrega 2 quedan desestimadas para este trabajo.

Para esta etapa se crearon 4 notebooks diferentes:

1. Procesamiento_columnas.ipynb: notebook que elimina columnas innecesarias, renombra columnas, elimina filas con NAN, se realiza escalado y codificado de columnas, etc.
2. friesgo_2018_reduc.csv: CSV generado a partir del procesamiento de columnas y utilizado como entrada para las notebooks siguientes
3. analisis_descriptivo.ipynb: Se realizan analisis de los datos para ver si se observan diferencias entre las distintas enfermedades por region. También se analiza la proporción de los datos luego del procesamiento de la etapa anterior
4. entrega3_arbolDecision.ipynb: Se ajusta un modelo de arbol de decisión para determinar las causas que producen diferencias en las tres enfermedades analizadas por región. A este modelo luego se mejoran los hiperparámetros mediante grid search


### Cuarta Pre-entrega

El objetivo de esta pre-entrega es la aplicación de un algoritmo No supervisado.
Se eligieron dos algoritmos de clusterización. El análisis busca agrupar en clusters los datos (sin tener en cuenta las columnas objetivo del análisis de la etapa anterior) y se compararán los grupos obtenidos con las regiones de forma de determinar si las regiones son realmente importantes en la agrupación de los datos.

Para esta etapa se reutilizan los siguientes archivos:

1. Procesamiento_columnas.ipynb: notebook que elimina columnas innecesarias, renombra columnas, elimina filas con NAN, se realiza escalado y codificado de columnas, etc.
2. friesgo_2018_reduc.csv: CSV generado a partir del procesamiento de columnas y utilizado como entrada para las notebooks siguientes
3. analisis_descriptivo.ipynb: Se realizan analisis de los datos para ver si se observan diferencias entre las distintas enfermedades por region. 

Se crean las siguientes notebooks:

1. entrega4_KMEANS.ipynb: Análisis de los objetivos exlpicados con la aplicación del algoritmo KMEANS para clusterización 
4. entrega4_DBScan.ipynb: Análisis de los objetivos exlpicados con la aplicación del algoritmo DBScan para clusterización
