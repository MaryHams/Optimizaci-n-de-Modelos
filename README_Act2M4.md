# 🩺 Clasificación Médica – Optimización de Modelos (Módulo 4)

## 📖 Descripción General

Este proyecto corresponde a la **Actividad de la Sesión 2 del Módulo 4** del curso de *Machine Learning*, cuyo objetivo fue **construir un modelo de clasificación médica** para predecir la probabilidad de diabetes en pacientes, utilizando el dataset **Pima Indians Diabetes Dataset**.

A partir de este conjunto de datos, se entrenaron modelos de **Random Forest** aplicando distintas estrategias de optimización de hiperparámetros para mejorar su desempeño.

---

## 📂 Contenido del Repositorio

| Archivo | Descripción |
|----------|--------------|
| `Act2M4_MHZ.ipynb` | Implementación de un modelo base con **RandomForestClassifier**, seguido de **Grid Search** y **Random Search**. Incluye análisis comparativo de métricas y tiempos de ejecución. |
| `Act2M4Optuna.ipynb` | Versión extendida donde se utiliza **Optuna** para la optimización automática de hiperparámetros. Se compara su rendimiento con las estrategias anteriores. |
| `README.md` | Documento explicativo del proyecto y reflexión personal. |

---

## ⚙️ Decisiones Técnicas

- **Modelo base:** Se eligió `RandomForestClassifier` por su estabilidad, facilidad de uso y buen rendimiento en tareas de clasificación médica.
- **Preprocesamiento:** Se aplicó `StandardScaler` para escalar las variables numéricas y se dividieron los datos en entrenamiento (70%) y prueba (30%).
- **Optimización de hiperparámetros:**
  - **Grid Search:** Se definió una malla de combinaciones fijas de parámetros (`n_estimators`, `max_depth`, `min_samples_split`), buscando el mejor conjunto mediante búsqueda exhaustiva.
  - **Random Search:** Se probaron combinaciones aleatorias dentro de rangos más amplios, reduciendo significativamente el tiempo de cómputo.
  - **Optuna:** En el segundo notebook, se exploró una alternativa más automatizada, capaz de encontrar configuraciones óptimas mediante técnicas de *sampling* y *pruning*.
- **Evaluación del modelo:** Se utilizaron métricas de desempeño como *accuracy*, *recall*, *F1-score* y *AUC*, junto con el tiempo de ejecución para comparar eficiencia.

---

## 📊 Resultados Principales

| Método | Accuracy | F1-Score | Tiempo (s) | Observación |
|--------|-----------|----------|-------------|--------------|
| Modelo Base | Medio | Medio | Bajo | Modelo sin optimización |
| Grid Search | Alto | Alto | Mayor | Precisión mejorada, pero mayor tiempo de cómputo |
| Random Search | Similar o mejor | Similar o mejor | Menor | Equilibrio entre desempeño y eficiencia |
| Optuna | Mejor | Mejor | Razonable | Excelente balance entre rendimiento y tiempo |

---

## 💭 Reflexión Final

> Esta actividad me ayudó a entender de forma práctica cómo los **hiperparámetros influyen directamente en el rendimiento de los modelos**.  
> Al principio me costó visualizar por qué era necesario ajustar tantos parámetros, pero al comparar los métodos comprendí que **no solo se trata de encontrar el mejor modelo, sino también de hacerlo de manera eficiente**.  
>
> Me sorprendió que el **Random Search** lograra resultados muy cercanos al Grid Search en mucho menos tiempo, y que herramientas como **Optuna** puedan automatizar aún más ese proceso.  
>
> En el futuro me gustaría explorar otros modelos y probar estrategias más avanzadas de optimización, pero esta experiencia me dio una base sólida sobre cómo enfrentar los ajustes de modelos en Machine Learning y cómo evaluar su desempeño de forma más crítica. 🚀

---

## 🧠 Tecnologías y Librerías

- Python 3.x  
- Scikit-learn  
- Optuna  
- Pandas  
- Numpy  
- Matplotlib / Seaborn  

---

## 👩‍💻 Autora

**Mary H. Z.**  
Proyecto desarrollado como parte del curso *Machine Learning – Módulo 4*  
(Actividad de ajuste de hiperparámetros y optimización de modelos)
