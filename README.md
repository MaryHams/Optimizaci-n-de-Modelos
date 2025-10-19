# Proyecto: Optimización de Modelos de Machine Learning con Optuna y Ray Tune

**Autora:** Mary Huaiquin  
**Curso:** Machine Learning – Módulo 4  
**Plataforma:** Google Colab  
**Lenguaje:** Python 3  

---

## Estructura del Repositorio

| Archivo / Carpeta | Descripción |
|--------------------|-------------|
| `EM4_MHZ.ipynb` | Notebook principal con la implementación completa del proceso de optimización de modelos. Incluye preprocesamiento, modelado base, uso de **Optuna** y **Ray Tune**, comparación de resultados y análisis crítico del sobreajuste. |
| `Evaluacion_Modular_M4_MHZ.pdf` | Informe original entregado para la evaluación modular. |
| `Informe_Extendido_M4_MHZ.docx` | Versión extendida y revisada del informe técnico, con tablas, gráficos y conclusiones profesionales. |
| `README.md` | Descripción general del proyecto bajo el modelo STAR (Situation, Task, Action, Result). |

---

## S – Situation

Este proyecto corresponde a la **Evaluación Modular del Módulo 4** del curso de Machine Learning.  
El objetivo fue aplicar técnicas de **optimización de hiperparámetros** a un modelo de clasificación utilizando el dataset público **“Disease Prediction Using Machine Learning”** disponible en Kaggle.

El conjunto de datos contenía 132 variables y 42 clases de enfermedades, lo que representaba un desafío de alta dimensionalidad.  
El propósito del trabajo fue **comparar distintas estrategias de optimización automática** y analizar su impacto en el rendimiento del modelo.

---

## T – Task

Mi tarea consistió en implementar, probar y comparar dos herramientas avanzadas de optimización:

1. **Optuna**, usando el algoritmo TPE (Tree-structured Parzen Estimator) con pruning automático.  
2. **Ray Tune**, aplicando búsquedas distribuidas en paralelo para mejorar la eficiencia.

Además, debía:
- Entrenar un modelo base con **Random Forest**.  
- Aplicar validación cruzada y métricas de evaluación (Accuracy, Recall, F1, AUC).  
- Comparar los resultados del modelo base y los modelos optimizados.  
- Reflexionar críticamente sobre los resultados y las implicancias del sobreajuste.

---

## A – Action

Para lograrlo, estructuré el notebook en bloques de código secuenciales:

1. **Preprocesamiento de datos:** imputación de valores faltantes, codificación de variables categóricas y normalización.  
2. **Modelo base:** entrenamiento de un Random Forest inicial para establecer un punto de comparación.  
3. **Optimización con Optuna:** definición de la función objetivo, búsqueda de hiperparámetros (n_estimators, max_depth, criterion) y visualización de la convergencia.  
4. **Optimización con Ray Tune:** implementación de un esquema distribuido para comparar velocidad y resultados.  
5. **Evaluación y análisis:** comparación de métricas y detección del sobreajuste (métricas perfectas = 1.0).  
6. **Documentación final:** creación de tablas, conclusiones y recomendaciones prácticas.

Durante el desarrollo, también incluí:
- Visualización del comportamiento de los hiperparámetros.  
- Gráficos de importancia de variables.  
- Análisis crítico sobre la calidad del dataset y los riesgos de sobreajuste.  

---

## R – Result

El modelo optimizado alcanzó **métricas perfectas (Accuracy, Recall, F1 = 1.0)**, lo cual permitió detectar un caso claro de **sobreajuste** debido a la naturaleza sintética del dataset.  

Aunque el modelo “aprendió” completamente los datos de entrenamiento, esta situación evidenció la importancia de validar con datos reales o de distinto origen.  

En términos de herramientas:
- **Optuna** demostró ser eficiente y fácil de usar para búsquedas secuenciales.  
- **Ray Tune** ofreció un excelente rendimiento en entornos distribuidos, pero requirió más recursos y configuración.

---

## Reflexión

Este proyecto fue un punto clave en mi aprendizaje, ya que me permitió comprender que **un modelo perfecto no siempre es un modelo útil**.  
Aprendí a interpretar los resultados más allá de las métricas, considerando aspectos como la calidad de los datos, la interpretabilidad y el uso responsable de modelos predictivos en contextos reales (especialmente en salud pública).

La optimización de hiperparámetros es una herramienta poderosa, pero debe aplicarse con criterio.  
La principal lección fue entender que **la validación y la ética en el uso de datos** son tan importantes como la precisión del modelo.

---

## Entorno y versiones utilizadas

- Python: 3.10.12  
- NumPy: 1.26.4  
- Pandas: 2.2.2  
- Scikit-learn: 1.4.2  
- Optuna: 3.6.1  
- Ray[tune]: 2.22.0  
- Matplotlib: 3.8.4  
- Seaborn: 0.13.2  

---

## Cómo ejecutar el proyecto

1. Abrir el notebook `EM4_MHZ.ipynb` en Google Colab.  
2. Ejecutar las celdas de manera secuencial, desde el preprocesamiento hasta la sección de evaluación.  
3. Los resultados (métricas, tablas y figuras) se generarán automáticamente dentro del entorno.  

---

**Etiquetas:**  
#MachineLearning #Optimización #Optuna #RayTune #RandomForest #GoogleColab #Educativo
