# Naive Bayes

## Objetivo del ejercicio

Desarrollar un modelo de aprendizaje supervisado para predecir si un estudiante aprobará o no, utilizando el algoritmo Gaussian Naive Bayes de scikit-learn.

## ¿Cómo funciona Naive Bayes?

Naive Bayes es un algoritmo de clasificación basado en probabilidades y en el teorema de Bayes.

Se denomina *naive* porque supone que las variables predictoras son independientes entre sí, una vez conocida la clase.

En este ejercicio utilicé `GaussianNB`, una variante adecuada para trabajar con variables numéricas que modela sus distribuciones mediante una distribución normal.

## Datos utilizados

Los datos se obtienen de la tabla `estudiantes` de una base de datos MySQL.

La variable objetivo es `aprobo`:

- `0`: No aprobó.
- `1`: Aprobó.

## Desarrollo del ejercicio

1. Conexión a MySQL y carga de datos con pandas.
2. Preparación de las variables predictoras.
3. Tratamiento de valores faltantes con `SimpleImputer`.
4. División de datos en entrenamiento y prueba.
5. Entrenamiento del clasificador `GaussianNB` mediante `Pipeline`.
6. Validación cruzada del modelo.
7. Evaluación mediante accuracy, matriz de confusión y reporte de clasificación.
8. Predicción del resultado de un estudiante nuevo.
9. Cálculo de probabilidades de aprobación y no aprobación mediante `predict_proba()`.

## Qué aprendí

En esta práctica aprendí a utilizar un algoritmo probabilístico para resolver un problema de clasificación.

También comprendí la diferencia entre obtener una clase predicha y obtener la probabilidad que el modelo asigna a cada clase.

## Herramientas utilizadas

- Python
- pandas
- scikit-learn
- SQLAlchemy y PyMySQL
- python-dotenv
- MySQL
- Jupyter Notebook

## Archivo del ejercicio

`ml_estudiantes_naive_bayes.ipynb`

Para ejecutar el notebook es necesario disponer de la tabla `estudiantes` y configurar localmente las variables de entorno para la conexión a MySQL.

*Ejercicio realizado durante la materia Procesamiento de Aprendizaje Automático.*
