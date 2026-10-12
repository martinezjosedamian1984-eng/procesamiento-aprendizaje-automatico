# Bosque Aleatorio (Random Forest)

## Objetivo del ejercicio

Construir un modelo de aprendizaje supervisado para predecir si un estudiante aprobará o no, utilizando sus características académicas y el algoritmo `RandomForestClassifier` de scikit-learn.

## ¿Cómo funciona Random Forest?

Random Forest combina múltiples árboles de decisión para realizar una predicción.

En esta práctica se utiliza `n_estimators=100`, por lo que el modelo trabaja con 100 árboles. Cada árbol realiza una clasificación y el bosque combina sus resultados para obtener la predicción final.

## Datos utilizados

Los datos se obtienen desde una base MySQL, de la tabla `estudiantes`.

Se utilizan ocho variables predictoras:

- Edad.
- Horas de estudio semanales.
- Porcentaje de asistencia.
- Porcentaje de tareas entregadas.
- Nota parcial.
- Participación en clase.
- Horas de sueño.
- Situación laboral.

La variable objetivo es `aprobo`:

- `0`: No aprobó.
- `1`: Aprobó.

## Desarrollo del ejercicio

1. Conexión a MySQL y carga de datos con pandas.
2. Selección de las variables predictoras y la variable objetivo.
3. Tratamiento de valores faltantes mediante `SimpleImputer`.
4. División de datos en entrenamiento y prueba.
5. Entrenamiento de Random Forest mediante `Pipeline`.
6. Validación cruzada para evaluar el rendimiento del modelo.
7. Evaluación mediante accuracy, matriz de confusión y reporte de clasificación.
8. Comparación del rendimiento entre entrenamiento y prueba.
9. Predicción del resultado de un estudiante nuevo.

## Qué aprendí

En esta práctica aprendí que Random Forest utiliza varios árboles de decisión en lugar de depender de uno solo.

También practiqué la preparación de datos, el entrenamiento y la validación del modelo.

Comprendí la importancia de evaluar las predicciones con datos que el modelo no utilizó durante el entrenamiento y de comparar ambos resultados para detectar posibles problemas de sobreajuste.

## Requisitos

- Python
- pandas y NumPy
- scikit-learn
- Matplotlib
- SQLAlchemy y PyMySQL
- python-dotenv
- Una base MySQL con la tabla `estudiantes`

Para ejecutar el notebook es necesario configurar localmente las variables de entorno utilizadas en la conexión a MySQL.

## Archivo del ejercicio

`ml_estudiantes_randomforest.ipynb`

*Ejercicio realizado durante la materia Procesamiento de Aprendizaje Automático.*
