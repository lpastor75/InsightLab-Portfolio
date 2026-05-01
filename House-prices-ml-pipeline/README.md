# 🏠 House Prices — Machine Learning Pipeline

Proyecto de Machine Learning de extremo a extremo para la predicción del precio de viviendas utilizando el dataset **House Prices: Advanced Regression Techniques (Kaggle)**.

Incluye:
- Análisis exploratorio
- Feature engineering
- Modelado supervisado
- Optimización de hiperparámetros
- Interpretabilidad (SHAP + PDP)
- Reducción de dimensionalidad (PCA, t-SNE)
- Clustering no supervisado

---

## 📁 Estructura del proyecto

house-prices-ml/
│
├── data/
│ ├── houses_raw.csv
│ ├── houses_prep.csv
│
├── notebooks/
│ ├── 01_data_preparation.ipynb
│ ├── 02_modeling_analysis.ipynb
│
├── requirements.txt
├── README.md
└── report.pdf (opcional)


---

## 📌 Objetivo

El objetivo del proyecto es construir un modelo de regresión capaz de predecir el precio de viviendas con alta precisión, interpretando además qué variables influyen más en la predicción.

---

## 🧠 Modelos utilizados

Se comparan distintos enfoques:

- Regresión Ridge
- Árbol de decisión
- Random Forest (modelo principal)
- K-Nearest Neighbors (KNN)

---

## ⚙️ Feature Engineering

Se aplican transformaciones para mejorar el rendimiento:

- Log-transform en variables sesgadas (`SalePrice`, `GrLivArea`)
- Transformación cíclica de variables temporales (`MoSold`)
- Eliminación de outliers con Isolation Forest

---

## 📊 Evaluación de modelos

Las métricas utilizadas:

- R² (train / validation / test)
- MAE (Mean Absolute Error)

Ejemplo de salida:

Random Forest
R2 -> Train: 0.98 | Val: 0.86 | Test: 0.87
MAE -> Test: ~18,000


---

## 🔍 Interpretabilidad

Se utilizan técnicas para explicar el modelo:

### 📌 Partial Dependence Plots (PDP)
Analizan el impacto marginal de variables como:
- `OverallQual`
- `GrLivArea`

### 📌 SHAP Values
- Explicación global y local del modelo
- Identificación de variables más influyentes

---

## 📉 Reducción de dimensionalidad

### PCA
Permite visualizar la estructura del dataset en 2 dimensiones.

### t-SNE
Captura relaciones no lineales para visualización de clusters.

---

## 🧩 Clustering

Se aplica:

- Gaussian Mixture Model (GMM)

Permite identificar grupos de viviendas con características similares.

---

## 📈 Resultados principales

- Random Forest es el modelo más robusto
- `OverallQual` y `GrLivArea` son las variables más importantes
- Feature engineering mejora significativamente el rendimiento
- PCA y t-SNE revelan estructura interna en los datos
- El dataset contiene clusters naturales de viviendas

---

## 🚀 Cómo ejecutar el proyecto

### 1. Clonar el repositorio

```bash
git clone https://github.com/tuusuario/house-prices-ml.git
cd house-prices-ml
```

### 2. Crear entorno virtual (opcional pero recomendado)

python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

### 3. Instalar dependencias

pip install -r requirements.txt

### 4. Ejecutar notebooks

Abrir Jupyter:

jupyter notebook

Y ejecutar en orden:

01_data_preparation.ipynb
02_modeling_analysis.ipynb


📦 Dependencias

Ver requirements.txt

📌 Dataset

Kaggle: House Prices — Advanced Regression Techniques
https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques

👨‍💻 Autor

**Luis Pastor Nuevo**

Proyecto desarrollado como práctica de Machine Learning aplicado a regresión y análisis exploratorio avanzado.