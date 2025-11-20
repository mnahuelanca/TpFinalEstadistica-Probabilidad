# Proyecto Final: Análisis Estadístico de Hábitos Estudiantiles y Rendimiento Académico

Este repositorio contiene el proyecto final para la asignatura de **Probabilidad y Estadística para la Gestión de Datos**, parte de la **Tecnicatura en Ciencia de Datos e IA**.

El objetivo principal de este trabajo es analizar cómo diversos hábitos de estilo de vida (estudio, sueño, redes sociales, trabajo) influyen en el rendimiento académico de los estudiantes, utilizando técnicas estadísticas y modelos de regresión lineal.

## 📋 Tabla de Contenidos
- [Descripción del Proyecto](#descripción-del-proyecto)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Dataset](#dataset)
- [Metodología de Análisis](#metodología-de-análisis)
- [Resultados y Modelado](#resultados-y-modelado)
- [Conclusiones Clave](#conclusiones-clave)
- [Autor](#autor)

## 📖 Descripción del Proyecto
El proyecto integra contenidos de probabilidad y estadística descriptiva e inferencial. Se exploran relaciones entre variables cuantitativas y cualitativas para responder preguntas como:
* ¿Las horas de estudio determinan la nota final?
* ¿El uso de redes sociales afecta negativamente el rendimiento?
* ¿Trabajar a tiempo parcial disminuye las calificaciones?
* ¿Se cumple el Teorema del Límite Central en la distribución de edades?

## 🛠 Tecnologías Utilizadas
El análisis fue realizado en **Python** utilizando las siguientes librerías:

* **Pandas**: Manipulación y limpieza de datos.
* **Numpy**: Cálculos numéricos y manejo de arrays.
* **Matplotlib & Seaborn**: Visualización de datos (Histogramas, Boxplots, Scatterplots, Heatmaps).
* **Scikit-learn**: Creación del modelo de Regresión Lineal y métricas de evaluación.

## 📂 Dataset
Se utilizó el archivo `habitos_estudiantes.csv`, el cual contiene 1000 registros de estudiantes con atributos como:
* `study_hours_per_day`: Horas de estudio.
* `social_media_hours`: Horas en redes sociales.
* `part_time_job`: Si trabaja o no (Yes/No).
* `exam_score`: Nota final del examen.
* `attendance_percentage`: Porcentaje de asistencia.
* Otros: Edad, horas de sueño, actividades extracurriculares.

## 🔍 Metodología de Análisis
1.  **Análisis Exploratorio (EDA)**: Cálculo de medidas de tendencia central (media) y dispersión (desvío estándar).
2.  **Simulación Estadística**: Verificación del **Teorema del Límite Central** mediante el muestreo iterativo de la variable `age`.
3.  **Visualización**:
    * Histogramas para distribuciones.
    * Boxplots para analizar el impacto del trabajo (`part_time_job`) en las notas.
    * Scatterplots para correlaciones bivariadas.
    * Heatmap de correlación de Pearson.
4.  **Modelado Predictivo**: Implementación de una **Regresión Lineal Simple** para predecir el puntaje del examen basado en las horas de estudio.

## 📊 Resultados y Modelado

### Correlaciones
Se encontró una correlación fuerte y positiva entre las horas de estudio y el puntaje del examen. Las redes sociales mostraron una correlación débil negativa.

### Regresión Lineal Simple
Se entrenó un modelo para predecir `exam_score` a partir de `study_hours_per_day`.

**Fórmula del modelo:**
Puntaje = 35.91 + 9.49 x (Horas de Estudio)

**Métricas de Evaluación:**
* **R² (Coeficiente de determinación):** 0.681 (El modelo explica el 68.1% de la variabilidad de la nota).
* **MAE (Error Absoluto Medio):** 7.71 puntos.
* **RMSE (Raíz del Error Cuadrático Medio):** 9.53 puntos.

## 💡 Conclusiones Clave
1.  **El estudio es el rey:** Las horas de estudio son el predictor más fuerte del éxito académico en este dataset.
2.  **Mito del trabajo derribado:** Contrario a la creencia popular, tener un trabajo a tiempo parcial **no disminuye** el promedio de notas. De hecho, los valores atípicos más bajos (outliers) se encontraron en estudiantes que **no** trabajan.
3.  **Redes Sociales y Asistencia:** Aunque influyen, su impacto es secundario y presentan una alta variabilidad.
4.  **Teorema del Límite Central:** Se demostró gráficamente que, al tomar múltiples muestras aleatorias, la distribución de las medias tiende a la normalidad, validando los supuestos estadísticos.

---

**Maximiliano Nahuelanca**
* Tecnicatura en Ciencia de Datos e IA
* Profesor: Gonzalo Ducca