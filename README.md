# Proyecto de Clasificación de Ingresos con Redes Neuronales

Este proyecto implementa un pipeline completo de aprendizaje supervisado para clasificar ingresos anuales utilizando el dataset Adult (Census Income). El trabajo se desarrolló en Google Colab e incluye preprocesamiento riguroso, experimentación con tres modelos de redes neuronales y documentación formal según estándares ICONTEC.

## 1. Descripción General

El objetivo del proyecto es predecir si una persona gana más de 50K USD al año a partir de variables demográficas, laborales y educativas. Para ello se ejecutan tres arquitecturas distintas:

* Perceptrón (modelo lineal base)
* Red neuronal de una capa oculta
* Red neuronal profunda con 10 capas ocultas

El proyecto permite comparar la capacidad representacional, estabilidad y rendimiento de cada modelo.

## 2. Estructura del Proyecto

* **Cuaderno 0:** Preprocesamiento completo del dataset Adult. Incluye imputación, normalización, codificación One-Hot, estratificación y exportación de datos procesados en formato `.npy`.
* **Cuaderno 1:** Implementación y evaluación del perceptrón.
* **Cuaderno 2:** Entrenamiento de una red neuronal con una capa oculta.
* **Cuaderno 3:** Entrenamiento de una red neuronal profunda con 10 capas ocultas. Incluye curvas de pérdida, exactitud y análisis comparativo.

## 3. Dataset

El proyecto utiliza el dataset Adult del repositorio UCI. El conjunto incluye más de 48.000 registros con información sobre:

* Edad
* Nivel educativo
* Ocupación
* Estado civil
* Horas trabajadas
* Ganancias y pérdidas de capital
* País de origen

La variable objetivo es el ingreso anual, binarizado como:

* `0` para <=50K
* `1` para >50K

## 4. Preprocesamiento

Las principales transformaciones aplicadas en el Cuaderno 0 son:

* Conversión de valores faltantes (?) a NaN
* Imputación de variables numéricas (mediana) y categóricas (moda)
* Normalización con StandardScaler
* Codificación One-Hot para variables categóricas
* Separación estratificada entre entrenamiento y prueba
* Exportación de X_train, X_test, y_train y y_test en formato `.npy`

## 5. Modelos Implementados

### Perceptrón

Modelo lineal que sirve como línea base. Tiene bajo poder representacional y dificultades frente a relaciones no lineales.

### Red de una capa oculta

Incluye activación sigmoide y mejora significativamente al perceptrón. Capta relaciones no lineales simples.

### Red profunda de 10 capas ocultas

Arquitectura con 10 capas ocultas, cada una con 10 neuronas y activación sigmoide. Presenta mayor estabilidad en entrenamiento y generalización.

## 6. Métricas de Evaluación

Se utilizan:

* Accuracy
* Precisión
* Recall
* F1-score
* Matriz de confusión

Estas métricas permiten evaluar el desempeño global y el comportamiento del modelo frente a la clase minoritaria.

## 7. Resultados y Comparación

Los resultados muestran que:

* El perceptrón obtiene el rendimiento más bajo.
* La red de una capa mejora significativamente.
* La red profunda ofrece la mejor estabilidad entre entrenamiento y validación, con un rendimiento general más consistente.

## 8. Requisitos para Reproducir el Proyecto

* Google Colab o entorno Python 3.10+
* Librerías: NumPy, Pandas, Scikit-learn, Matplotlib, Seaborn, TensorFlow
* Archivos `.npy` generados en el Cuaderno 0

## 9. Ejecución

1. Ejecutar el Cuaderno 0 para generar los conjuntos `.npy`.
2. Ejecutar los Cuadernos 1, 2 y 3 para entrenar y evaluar cada modelo.
3. Analizar gráficas y matrices de confusión para la comparación final.

## 10. Documentación

El proyecto incluye un informe formal bajo la norma ICONTEC, con:

* Introducción
* Marco teórico
* Metodología
* Análisis del desarrollo
* Resultados
* Conclusiones y recomendaciones
* Glosario y cronograma

## 11. Autoría

Proyecto desarrollado en Google Colab como parte del curso de Introduccion a IA
