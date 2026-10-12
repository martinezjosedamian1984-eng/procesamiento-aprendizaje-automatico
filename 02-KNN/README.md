# K vecinos más cercanos (KNN)

## Objetivo del ejercicio

Construir un modelo de aprendizaje supervisado para clasificar estudiantes según sus características académicas, utilizando el algoritmo `KNeighborsClassifier` de scikit-learn.

## ¿Cómo funciona KNN?

KNN clasifica un nuevo estudiante buscando los ejemplos más cercanos dentro de los datos de entrenamiento.

En este ejercicio se utiliza `n_neighbors=5`, por lo que el modelo considera los cinco vecinos más cercanos para decidir la clasificación.

## Preparación y entrenamiento

Durante la práctica se trabajó con:

- Carga de datos desde MySQL.
- Selección de variables predictoras y variable objetivo.
- Tratamiento de valores faltantes mediante `SimpleImputer`.
- Escalado de variables utilizando `StandardScaler`.
- División de los datos en entrenamiento y prueba.
- Entrenamiento de un modelo KNN mediante `Pipeline`.

## Validación y evaluación

Se utilizaron técnicas de evaluación como validación cruzada, accuracy, matriz de confusión y reporte de clasificación.

El escalado es importante porque KNN utiliza distancias matemáticas para comparar los estudiantes. Las variables con escalas diferentes pueden influir de manera desigual en esos cálculos.

## Qué aprendí

En esta práctica aprendí que KNN no construye reglas como un árbol de decisión, sino que clasifica utilizando ejemplos similares.

También comprendí que la cantidad de vecinos elegida y el escalado de las variables pueden influir en las predicciones.

## Requisitos

Python, pandas, NumPy, scikit-learn, Matplotlib, SQLAlchemy, PyMySQL y python-dotenv.

El notebook requiere una base MySQL con la tabla `estudiantes` y variables de entorno configuradas localmente para establecer la conexión.

## Archivo del ejercicio

`ml_estudiantes_knn.ipynb`

Este repositorio documenta las prácticas realizadas durante la materia Procesamiento de Aprendizaje Automático.
