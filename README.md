# body-performance-ordinal-ml

## 📌 Project Overview
Este proyecto analiza datos de rendimiento físico utilizando modelos de aprendizaje automático ordinales (o adaptados a ellos) en los que la variable objetivo representan niveles de rendimiento ordenados (D<C<B<A).
A diferencia de la clasificación multiclase estándar,la estructura ordinal se tiene en cuenta explícitamente para penalizar los errores de predicción según su gravedad.


## 📊 Dataset
- Source: Kaggle – Body Performance Dataset
- Observaciones: ~13,000 individuos
- Características: antropométricas, fuerza, flexibilidad, resistencia, y variables fisiológicas.
- Target variable: **Clase de rendimiento (ordinal)**

## 🧠 Metodología
1. Análisis exploratorio (EDA)
2. Ingeniería de características (BMI, codificación ordinal)
3. Entrenamiento del modelo y evaluación
4. Interpretabilidad del modelo

### Modelos Implementados
- **LogisticAT (Regresión Logística Ordinal)**
  Modelo ordinal de referencia que asume relaciones lineales  
- **Random Forest Classifier**  
   Baseline no lineal que ignora la estructura ordinal
- **XGBoost with Ordinal Objective**  
  Impplementado usandommodelos de umbral acumulativo  \(P(y > k)\) para preservar el ordenamiento de clases.

## 📈 Métricas de evaluación
Dada la naturaleza ordinal del problema, se usaron las siguientes métricas:
- Accuracy
- Mean Absolute Error (MAE)
- Quadratic Weighted Kappa (QWK)

## 🔍 Interpretabilidad
- Análisis de importancia de las características
- Valores SHAP (explicaciones locales y globales)
- Inspección de predicciones individuales para comprender las transacciones ordinales.

Las variables claves que influyen son:
- Flexibilidad (`sit and bend forward`)
- Abdominales (`sit-ups`)
- Fuerza de agarre
- Body composition (BMI, body fat percentage)


