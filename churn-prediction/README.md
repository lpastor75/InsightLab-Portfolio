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

## 📊 Data Source

El dataset utilizado en este proyecto corresponde al **Telco Customer Churn**, ampliamente utilizado en problemas de analítica predictiva para modelar el abandono de clientes en el sector de telecomunicaciones.

Este conjunto de datos fue proporcionado originalmente por :contentReference[oaicite:0]{index=0} como parte de los datos de ejemplo de su plataforma Cognos Analytics.

🔗 **Fuente oficial (IBM):**  
https://www.ibm.com/docs/en/cognos-analytics/11.2.x?topic=samples-telco-customer-churn

Para facilitar su uso en entornos de desarrollo y aprendizaje, existe una versión pública accesible a través de Kaggle, que mantiene la misma estructura y variables que el dataset original.

---

### 🧾 Descripción del dataset

El dataset contiene información detallada sobre clientes de una empresa de telecomunicaciones, incluyendo:

- Datos demográficos del cliente  
- Servicios contratados  
- Tipo y duración del contrato  
- Información de facturación  
- Historial de permanencia  

La variable objetivo es **`Churn`**, que indica si el cliente ha abandonado el servicio (*Yes*) o continúa activo (*No*).

---

### 🎯 Aplicación en el proyecto

Este dataset permite abordar un problema clásico de **clasificación binaria**, cuyo objetivo es predecir la probabilidad de abandono de un cliente.

Los resultados del modelo pueden ser utilizados para:

- Identificar clientes con alto riesgo de churn  
- Diseñar estrategias de retención personalizadas  
- Optimizar campañas de fidelización  
- Reducir costes asociados a la pérdida de clientes
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

```bash
churn-prediction/
│
├── data/                          # Raw dataset
│
├── churn_prediction.ipynb         # Main analysis notebook
├── README.md                      # Project documentation
└── requirements.txt               # Dependencies
```

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
