# 📊 Customer Churn Prediction

Proyecto de Machine Learning orientado a la **predicción del abandono de clientes (churn)** en una empresa del sector telecomunicaciones.

---

## 🚀 Descripción del proyecto

El abandono de clientes es uno de los principales problemas de negocio en empresas de servicios por suscripción. Retener clientes es significativamente más barato que adquirir nuevos.

Este proyecto desarrolla un modelo predictivo capaz de identificar clientes con alta probabilidad de abandono, permitiendo actuar de forma anticipada mediante estrategias de retención.

---

## 🎯 Objetivos

* Analizar los factores que influyen en el churn
* Construir modelos predictivos robustos
* Evaluar el rendimiento con métricas adecuadas (especialmente **recall**)
* Simular un entorno real con datos no vistos
* Extraer conclusiones accionables para negocio

---

## 🧠 Dataset

* Dataset: **Telco Customer Churn**
* Fuente: IBM / Kaggle
* Contiene información sobre:

  * Datos demográficos
  * Servicios contratados
  * Tipo de contrato
  * Facturación
  * Antigüedad del cliente

---

## 🔍 Análisis exploratorio (EDA)

Se realizó un análisis exhaustivo para entender el comportamiento de los datos:

* 📉 **Desbalanceo moderado** (~27% churn)
* 📊 Variables clave identificadas:

  * `tenure` (antigüedad)
  * `Contract`
  * `MonthlyCharges`
* 📈 Clientes con contratos mensuales presentan mayor churn
* 🔗 Correlación relevante entre variables financieras

---

## ⚙️ Preprocesamiento

Se implementó un pipeline completo y reproducible:

* Transformación de variables:

  * `Contract` → ordinal
  * `TotalCharges` → numérica
* Tratamiento de nulos:

  * Imputación (mean / median)
* Escalado:

  * `StandardScaler`
* Codificación:

  * `OneHotEncoder`

Todo integrado mediante:

* `Pipeline`
* `ColumnTransformer`

---

## 🧪 Modelos evaluados

Se compararon distintos algoritmos:

* 🔹 Regresión Logística
* 🌳 Árbol de Decisión
* ⚡ Support Vector Machine (SVM)

Optimización mediante:

* `GridSearchCV`
* Validación cruzada (`StratifiedKFold`)
* Métrica principal: **Recall**

---

## 📈 Resultados

| Modelo              | AUC   | Observaciones     |
| ------------------- | ----- | ----------------- |
| Regresión Logística | ~0.85 | Mejor recall      |
| Árbol de decisión   | ~0.84 | Más interpretable |
| SVM                 | ~0.85 | Mayor precisión   |

### 🏆 Modelo seleccionado: Regresión Logística

* Mejor capacidad para detectar churn
* Menor número de falsos negativos
* Más alineado con el objetivo de negocio

---

## 📊 Métricas clave

* **Recall** → Prioridad del proyecto
* Precision
* F1-score
* ROC-AUC
* Curva Precision-Recall

---

## 🧩 Decisiones importantes

* Uso de pipelines para evitar **data leakage**
* Separación train/test antes de modelado
* Optimización orientada a negocio (no solo accuracy)
* Evaluación con datos no vistos

---

## 💡 Insights de negocio

* Clientes con baja antigüedad tienen alto riesgo
* Contratos mensuales son el segmento más vulnerable
* Estrategias de retención deberían enfocarse en:

  * Nuevos clientes
  * Planes mensuales

---

## 🛠️ Tecnologías utilizadas

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

## 📁 Estructura del proyecto

## 📁 Estructura del proyecto

├── data/
├── churn_prediction.ipynb
├── README.md
└── requirements.txt

---

## ▶️ Cómo ejecutar el proyecto

```bash
# Clonar repositorio
git clone <repo-url>

# Crear entorno
conda create -n churn_env python=3.10
conda activate churn_env

# Instalar dependencias
pip install -r requirements.txt

# Ejecutar notebook
jupyter notebook
```

---

## 📌 Mejoras futuras

* Modelos avanzados (XGBoost, LightGBM)
* Interpretabilidad (SHAP, feature importance)
* Deploy del modelo (API / Streamlit)
* Monitorización en producción

---

## 👨‍💻 Autor

**Luis Pastor Nuevo**

---

## ⭐ Conclusión

Este proyecto demuestra un flujo completo de Machine Learning aplicado a negocio, desde el análisis exploratorio hasta la validación en datos reales, priorizando métricas alineadas con el impacto empresarial.

---
