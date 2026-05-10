# Proyecto MVC - Grupo 1 | Modelo de Rotación Laboral (Churn)

**Asignatura:** Modelización de Variables Categóricas  
**Grupo:** 1  

## Descripción del Proyecto
Este repositorio contiene el desarrollo integral de la **Pregunta G: Modelo de rotación laboral en titulados de máster**. El objetivo principal es identificar los factores críticos que influyen en que un recién graduado abandone su primer empleo, desarrollando un sistema predictivo robusto que permite anticipar el riesgo de fuga de talento mediante técnicas avanzadas de *Machine Learning*.

## Variable Objetivo
Se modeliza la variable categórica `P_CONTI` ("¿Continúa trabajando en su primer empleo?"):
* **Clase 1:** Retención de talento (El profesional continúa en la empresa).
* **Clase 0:** Rotación / Churn (El profesional ha abandonado su primer empleo).

## Estructura del Repositorio
El proyecto se organiza en tres cuadernos de trabajo que cubren el ciclo de vida del dato siguiendo las directrices académicas:

* **`/data`**: Contiene el dataset `EILU_MAST_2019_limpio.csv`. (Nota: Los microdatos originales han sido procesados para gestionar nulos y valores '9').
* **`/notebooks`**: 
    1.  **`01_EDA.ipynb`**: Análisis exploratorio, limpieza de datos y estudio de asociación mediante el estadístico **V de Cramér**.
    2.  **`02_modelo_base.ipynb`**: Creación del *Baseline* con **Regresión Logística** y diseño de Pipeline (One-Hot Encoding + Standard Scaling).
    3.  **`03_modelado_avanzado.ipynb`**: 
        * Comparativa de modelos de ensamble (**Random Forest** y **Gradient Boosting**).
        * **Validación Cruzada Estratificada ($k=5$)** obteniendo un **AUC-ROC medio de 0.7593**.
        * Optimización de hiperparámetros mediante `GridSearchCV`.
        * Experimentación con técnicas de **Target Encoding**.
        * **Fase 4 - Interpretabilidad:** Análisis de mecanismos internos del modelo.

## Marco Teórico: Interpretabilidad y Explicabilidad
Basado en la **Sesión 6.2** del programa, el proyecto aplica los conceptos de:
* **Interpretabilidad:** Capacidad de captar el **"por qué"** de una predicción (grado de comprensión humana de las razones tras una decisión).
* **Explicabilidad:** Habilidad para comprender tanto el **"cómo"** como el **"por qué"**.
* **Métodos Agnósticos (SHAP):** Implementación de valores de Shapley (Teoría de Juegos) para cuantificar la contribución de cada variable (Jornada, Edad, Sueldo) al resultado del modelo, transformando nuestra "caja negra" en un sistema transparente.


