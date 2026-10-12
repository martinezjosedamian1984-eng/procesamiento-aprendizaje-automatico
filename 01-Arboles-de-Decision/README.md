# Árboles de decisión

## Objetivo del ejercicio

Construir un modelo de aprendizaje supervisado para predecir si un estudiante aprobará o no, utilizando información sobre sus hábitos de estudio y rendimiento académico.

El algoritmo utilizado es `DecisionTreeClassifier` de scikit-learn.

## Datos utilizados

Los datos se obtienen desde una base MySQL, de la tabla `estudiantes`.

Las variables predictoras incluyen edad, horas de estudio, asistencia, tareas entregadas, nota parcial, participación en clase, horas de sueño y situación laboral.

La variable objetivo es `aprobo`, con dos clases:

- `0`: No aprobó.
- `1`: Aprobó.

## Desarrollo del ejercicio

1. Conexión a MySQL y carga de datos mediante pandas.
2. Selección de variables predictoras y variable objetivo.
3. Revisión y simulación de valores faltantes.
4. División de datos: 80% para entrenamiento y 20% para prueba.
5. Entrenamiento de un árbol de decisión con profundidad máxima de 4.
6. Validación cruzada con 5 particiones.
7. Evaluación mediante accuracy, matriz de confusión y reporte de clasificación.
8. Comparación del rendimiento entre entrenamiento y prueba.
9. Predicción del resultado de un estudiante nuevo.

## Qué aprendí

En esta práctica trabajé con un modelo que utiliza reglas y condiciones para clasificar estudiantes.

También practiqué el tratamiento de valores faltantes mediante `SimpleImputer` y la utilización de `Pipeline` para organizar el procesamiento y entrenamiento.

Aprendí a evaluar el rendimiento con datos de prueba y a comparar los resultados de entrenamiento y prueba para identificar posibles problemas de sobreajuste.

## Requisitos

- Python
- pandas y NumPy
- scikit-learn
- Matplotlib
- SQLAlchemy y PyMySQL
- python-dotenv
- Una base MySQL con la tabla `estudiantes`

La conexión utiliza variables de entorno: `DB_HOST`, `DB_PORT`, `DB_USER`, `DB_PASSWORD` y `DB_NAME`. Es necesario configurarlas localmente para ejecutar el notebook.

## Archivo

`ml_estudiantes_arbol_decision.ipynb`

Ejercicio práctico realizado durante la materia Procesamiento de Aprendizaje Automático.
