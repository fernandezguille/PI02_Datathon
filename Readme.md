# __PROYECTO INDIVIDUAL 02__
<img src="https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/11/scikit-learn-using-python.png" width="500px">

### Introducción

Éste el el segundo proyecto individual, que forma parte de la formación práctica del bootcamp de Data Science de Henry. El mismo consiste en cargar un dataset sobre hospitalizaciones, separado en dos. Mediante la exploración y el entrenamiento de un Modelo de Machine Learning, se debe predecir si los pacientes pasarán más de 8 días hospitalizados, entrenandolo con una parte del dataset que tiene los resultados, y la otra parte que no lo tiene.
Para averiguar si el modelo tiene buenos resultados, se ha habilitado un Dashboard.

[Consigna completa del PI](https://github.com/soyHenry/Datathon)

## Pasos para realizar el proyecto:
1. EDA (Exploratory data analysis)
2. Preprocesamiento de datos
3. Análisis de correlación
4. Tratamiento de features (eliminado y recategorizacion)
5. Creación del modelo
6. Predicción
7. Conclusiones finales

## Archivos del repositorio
Los archivos raw utilizados para realizar el proyecto se encuentran dentro de la carpeta Datasets, y también el archivo que se creó con los resultados de la predicción. El nombre de las predicciones coincide con el usuario de GitHub.  
Modelo ML.ipynb es el archivo en donde se realizan todos los pasos mencionados.

## EDA
Para el primer paso, se realizó el EDA. Se exploraron los datasets, revisando tipos de datos y faltantes. En base a este análisis, se obtuvieron algunas conclusiones iniciales.

## Preprocesamiento de datos
Se creó el feature de relevancia, se eliminaron duplicados.

## Análisis de correlación
Con la ayuda de las librerías de Python, se evaluó el P valor de las variables categóricas, para evaluar la correlación

## Tratamiento de features
Se eliminan las features irrelevantes, y se realiza la recategorización mediante LabelEncoder y OneHotEncoder

## Creación del modelo
Con el dataset ya codificado, se realiza un modelo de árbol de desición. Utilizando CV y un bucle, se obtiene la profundidad óptima del árbol. Se entrena el modelo con train_test_split.  
<img src="https://static.vecteezy.com/system/resources/previews/001/234/042/original/decision-tree-design-vector.jpg" width="200px">

## Predicción
Con el modelo entrenado, se realiza la predicción del feature, y se lo exporta a un archivo para su posterior evaluación.

## Conclusiones finales
Luego de realizar varias pruebas, con diferentes métodos (dummies, OHE, LE), este modelo fue el que mejor accuracy y recall tuvo, sin tener overfitting.  
Muchas de las columnas tenían una relación con la estadía, como se vió con el P_valor, pero el resultado solo mejora un poco a comparación de realizar el árbol con sólo 3 features.
Al recibir el feedback del modelo, los valores logrados de las métricas son:
+ Accuracy: 0.7512
+ Recall:   0.7847

¡Muchas gracias por llegar hasta aquí!