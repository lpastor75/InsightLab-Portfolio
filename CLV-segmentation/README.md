# 📊 Customer Lifetime Value & Customer Segmentation

Proyecto de Machine Learning enfocado en la estimación del valor de vida del cliente (*Customer Lifetime Value, CLV*) y la segmentación de clientes mediante técnicas no supervisadas.

El objetivo es transformar datos de clientes en información accionable para apoyar decisiones de negocio en marketing y retención.

---

## 🎯 Objetivos

- Estimar el **Customer Lifetime Value (CLV)** mediante modelos de regresión.
- Evaluar y comparar distintos enfoques predictivos.
- Identificar segmentos de clientes mediante **clustering (KMeans)**.
- Aplicar transformación de variables, escalado y feature engineering.
- Extraer insights orientados a negocio a partir de los resultados.

---

## 📁 Estructura del proyecto

CLV-project/
│
├── data/
│ ├── clv/
│ │ └── Marketing-Customer-Value-Analysis.csv
│ └── segmentation/
│ └── online12M.csv
│
├── clv_segmentation.ipynb
├── README.md
└── requirements.txt

---

## 📦 Datasets

### 🔹 Customer Lifetime Value (CLV)
Dataset proporcionado por IBM con información de clientes de campañas de marketing.

- Fuente: IBM Cognos Analytics Samples  
- Documentación: https://www.ibm.com/docs/en/cognos-analytics/11.2.x?topic=samples-telco-customer-churn  

---

### 🔹 Dataset de segmentación (RFM)
Dataset basado en transacciones de comercio electrónico utilizado para construir variables RFM:

- Recency: tiempo desde la última compra  
- Frequency: número de compras  
- Monetary Value: gasto total  

---

## ⚙️ Tecnologías utilizadas

- Python
- Pandas, NumPy
- Scikit-learn
- Seaborn, Matplotlib

---

## 🧠 Metodología

### 1. Preprocesamiento
- Tratamiento de variables categóricas y numéricas
- Conversión de fechas a variables numéricas
- Eliminación de outliers en CLV
- Transformación logarítmica para variables sesgadas

---

### 2. Modelado predictivo (CLV)

Se entrenan distintos modelos de regresión:

- Regresión Lineal
- Árbol de Decisión
- Optimización de hiperparámetros con `GridSearchCV`

**Métricas utilizadas:**
- R² (coeficiente de determinación)
- MAE (Mean Absolute Error)

---

### 3. Segmentación de clientes

Se aplica un enfoque RFM (Recency, Frequency, Monetary Value):

- Transformación logarítmica para reducir sesgo
- Estandarización de variables
- Selección del número óptimo de clusters (método del codo)
- Clustering con **KMeans**

---

## 📊 Resultados

### 🔹 Modelos de CLV
- La regresión lineal muestra capacidad predictiva limitada.
- Los árboles de decisión mejoran el ajuste, pero requieren control de complejidad.
- La optimización de hiperparámetros reduce el sobreajuste.

---

### 🔹 Segmentación de clientes
Se identifican perfiles diferenciados de clientes:

- Clientes de alto valor
- Clientes inactivos
- Clientes recurrentes
- Clientes ocasionales de bajo gasto

---

## 💡 Insights de negocio

- El comportamiento de compra no es lineal, lo que limita modelos simples.
- La segmentación RFM permite identificar grupos accionables para campañas de marketing.
- El control de complejidad en modelos de árbol es clave para generalización.

---

## 🚀 Próximos pasos

- Implementación de modelos más avanzados (Random Forest, XGBoost)
- Clustering alternativo (DBSCAN, Gaussian Mixture Models)
- Automatización del pipeline con `sklearn Pipeline`
- Despliegue del modelo como API

---

## 👨‍💻 Autor

Proyecto de portfolio en Data Science & Machine Learning enfocado en problemas reales de negocio: predicción de valor del cliente y segmentación para marketing.