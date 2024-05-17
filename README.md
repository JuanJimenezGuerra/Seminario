# Proyecto de Segmentación de Clientes
## Grupo:
- Grupo 03
# Implementación:
## Análisis Exploratorio:
Comenzamos con un análisis detallado del conjunto de datos, compuesto por 28,302 filas y 186 columnas. Observamos que el dataset incluye 29 columnas con valores float64, 4 columnas con valores int64 y 153 columnas con datos de tipo object.
Con el fin de garantizar la calidad de nuestros datos, tomamos varias medidas durante el proceso de limpieza:
- Eliminamos las columnas que contenían más del 50% de datos nulos, con especial atención a aquellas con más del 95% de valores faltantes. También excluimos las columnas de ID's, aquellas con un único valor en todos los registros y las relacionadas con fechas, ya que no aportaban información relevante para nuestro análisis de clustering.
- Estandarizamos las variables categóricas mediante su agrupación en conjuntos homogéneos, lo que facilita su procesamiento y comprensión.
- Identificamos una alta correlación entre ciertas variables numéricas y decidimos conservar solo una de ellas, ajustando los valores atípicos de la edad según las indicaciones del negocio.
- Para abordar los datos faltantes, asignamos valores utilizando la moda para variables categóricas, el promedio para variables numéricas y, en casos excepcionales, creamos una nueva categoría denominada “Unknown”. Además, renombramos las variables de entrada para una mayor claridad en sus nombres.

## Preparación de datos para el modelo:
Para garantizar una contribución equitativa de todas las variables a nuestro modelo de clustering, escalamos las variables numéricas del DataFrame utilizando la función normalize. Además, para manejar las variables categóricas, aplicamos la técnica de one-hot encoding utilizando la función de Dummies. Esto nos permite convertir las variables categóricas en variables binarias.

## Creación del dataset:
Se realiza la creación del conjunto de datos listo para implementar un algoritmo de clusterización utilizando la técnica K-means.

Se ha determinado el número óptimo de clusters para el modelo utilizando el método del codo y el coeficiente de silueta.


#Análisis Avanzado:
Para confirmar las correlaciones entre nuestras variables numéricas, hemos revisado varios gráficos. Esto nos permitirá comprender mejor la estructura de los datos y su idoneidad para el modelo de clustering.

# Ejecución:
