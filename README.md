# Proyecto de campaña en Banco

Utilizando la información sobre campañas anteriores realizadas por el banco para captar depósitos a largo plazo, se entrena un modelo de Regresión Logística con el objetivo de predecir si un cliente tipo va a realizar un depósito de ésta característica o no.

Primero se realiza un análisis exploratorio de los datos para detectar posibles anomalías en la base de datos importada, para luego en un paso posterior, realizar las transformaciónes que sean necesarias para tener el dataset apto para entrenar el modelo.

Una vez que se tiene la base de datos transformada, se seleccionan las variables que se convertirán en los features del modelo, contemplando la correlación con la variable a predecir (y), así como la correlación lineal entre ellas para prevenir posible multicolinealidad. A continuación, se separa la muestra entre entrenamiento y prueba considerando proporciones de 80-20. 

Se plantea el modelo considerando que la muestra está desbalanceada, por lo que al momento de crear el modelo se incluye el hiperparámetro clases_wehigt otorgando distintos pesos para cada categoría de la variable a predecir y penalizando la clase que menos representada está en la muestra. 

Por último, se analiza el ajuste de la predicción realizada en base a la muestra de prueba.
