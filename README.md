# Proyecto: Optimización de Modelos con Optuna 

**Autora:** Mary Huaiquin  
**Curso:** Machine Learning – Módulo 4  
**Plataforma:** Google Colab  
**Lenguaje:** Python 3  

---

## Estructura del repositorio

| Archivo / Carpeta | Descripción |
|-------------------|-------------|
| `Act2M4Optuna.ipynb` | Notebook principal con la implementación del proceso de ajuste de hiperparámetros con **Optuna**. Incluye preprocesamiento, modelo base y optimización con TPE, además de evaluación y comparación de resultados. |
| `README_Act2M4.md` | Descripción del general del proyecto |

---

## S – Situation

Actividad 2 del **Módulo 4** de Machine Learning.  
El objetivo fue aplicar **búsqueda automatizada de hiperparámetros** para mejorar el rendimiento de un modelo de clasificación utilizando un conjunto de datos multiclase de alta dimensionalidad.  

Se trabajó en **Google Colab**, empleando pipelines de preprocesamiento y validación cruzada estratificada.  
El dataset provenía de un caso sintético de predicción de enfermedades con múltiples variables clínicas, ideal para probar optimizadores automáticos.

---

## T – Task

- Construir un **modelo base** de clasificación (por ejemplo, Random Forest).  
- Definir un **espacio de búsqueda** razonable para los hiperparámetros más influyentes.  
- Implementar **Optuna** con el sampler **TPE** y validación cruzada para estimar el desempeño.  
- Comparar el rendimiento del modelo base versus el modelo optimizado, reportando métricas y observaciones.  

---

## A – Action

1. **Preprocesamiento de datos:** imputación de faltantes, codificación *One-Hot* para variables categóricas y estandarización de variables numéricas mediante un `ColumnTransformer` dentro de un `Pipeline` de scikit-learn.  
2. **Modelo base:** entrenamiento de un `RandomForestClassifier` para establecer un punto de referencia inicial.  
3. **Optimización con Optuna:**  
   - Definición de una función objetivo que entrena y evalúa el pipeline completo usando validación cruzada estratificada (k=3).  
   - Exploración de hiperparámetros como `n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`, `max_features` y `bootstrap`.  
   - Uso de la métrica **F1-macro** como criterio de optimización.  
4. **Entrenamiento final:** reentrenamiento con los **mejores hiperparámetros** encontrados y evaluación final en el conjunto de prueba.  
5. **Documentación:** registro de resultados, métricas comparativas y análisis crítico del proceso.

---

## R – Result

- El modelo optimizado con **Optuna** mejoró el desempeño respecto al modelo base en la métrica **F1-macro**, manteniendo estabilidad en **Accuracy** y **AUC**.  
- Los hiperparámetros más influyentes fueron `n_estimators`, `max_depth` y `min_samples_leaf`.  
- El proceso de búsqueda se volvió más eficiente gracias al **pruning automático**, que detuvo combinaciones poco prometedoras.  

> En datasets sintéticos altamente determinísticos, las métricas se aproximaron a 1.0, lo que permitió reflexionar sobre los efectos del **sobreajuste** y la importancia de la validación con datos reales.

---

## Reflexión

Este proyecto me permitió comprender cómo las técnicas de **optimización de hiperparámetros** pueden mejorar el rendimiento de un modelo cuando se aplican de manera controlada.  
Aprendí que el **espacio de búsqueda**, la **métrica de validación** y la **calidad de los datos** son factores determinantes para obtener resultados significativos.  

También comprendí que las métricas perfectas no siempre indican éxito, y que un análisis crítico es fundamental para evitar conclusiones erróneas.  
La principal lección fue aprender a usar Optuna de manera profesional y reflexionar sobre la reproducibilidad y transparencia de los experimentos en Machine Learning.

---

## Cómo ejecutar el proyecto

1. Abrir `Act2M4Optuna.ipynb` en **Google Colab**.  
2. Ejecutar las celdas en orden, desde el preprocesamiento hasta la evaluación final.  
3. Al finalizar, se mostrarán las **métricas comparativas** (modelo base vs modelo optimizado) y los **mejores hiperparámetros** encontrados.

---

## Entorno y versiones utilizadas

Este proyecto se desarrolló en **Python 3.10** (Google Colab) con las siguientes versiones:

- numpy == 1.26.4  
- pandas == 2.2.2  
- scikit-learn == 1.4.2  
- optuna == 3.6.1  
- matplotlib == 3.8.4  
- seaborn == 0.13.2  

Para replicar el entorno, se sugiere crear un archivo `requirements.txt` con estas versiones.

---

## Lecciones aprendidas

- La **optimización de hiperparámetros** es esencial para obtener modelos más robustos y equilibrados.  
- Un espacio de búsqueda adecuado y métricas representativas garantizan resultados confiables.  
- **Optuna** es una herramienta versátil y eficiente para problemas de clasificación.  
- Validar con datos independientes es crucial para evitar sobreajuste y asegurar aplicabilidad.

---

**Etiquetas:**  
#MachineLearning #Optuna #Optimización #Hiperparámetros #Python #GoogleColab #Educativo
