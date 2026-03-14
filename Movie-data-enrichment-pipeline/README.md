# 🎬 Movie Data Pipeline

### Integración de datos de IMDb y TMDb con MongoDB

## 📌 Descripción

Este proyecto implementa un **pipeline de ingeniería de datos** que integra datasets públicos de **IMDb** con información adicional obtenida mediante la **API de TMDb**.

El objetivo es construir un dataset enriquecido de películas combinando múltiples fuentes de datos, procesarlo con Python y almacenarlo en **MongoDB** para permitir consultas flexibles y análisis posteriores.

El proyecto reproduce un flujo típico de trabajo en ingeniería de datos:

* ingestión de datasets
* enriquecimiento mediante APIs externas
* procesamiento y limpieza de datos
* almacenamiento en base de datos NoSQL
* consultas analíticas sobre el dataset resultante

---

# ⚙️ Tecnologías utilizadas

* **Python**
* **Pandas** – procesamiento y transformación de datos
* **Requests** – consumo de APIs REST
* **MongoDB** – almacenamiento de datos semiestructurados
* **Jupyter Notebook** – desarrollo del pipeline
* **IMDb Datasets** – fuente de datos principal
* **TMDb API** – enriquecimiento de metadatos

---

# 🏗️ Arquitectura del pipeline

El flujo de procesamiento de datos es el siguiente:

```
IMDb datasets
      │
      ▼
Carga y filtrado de datos
      │
      ▼
Integración de ratings
      │
      ▼
Enriquecimiento mediante TMDb API
      │
      ▼
Integración de metadatos
      │
      ▼
Almacenamiento en MongoDB
      │
      ▼
Consultas y análisis
```

---

# 📊 Fuentes de datos

### IMDb datasets

Se utilizan datasets públicos de IMDb:

* `title.basics`
* `title.ratings`

Estos datasets contienen información sobre:

* títulos
* fechas de lanzamiento
* géneros
* valoraciones de usuarios

### TMDb API

La API de TMDb se utiliza para enriquecer los datos con información adicional:

* presupuesto
* ingresos
* popularidad
* idioma original
* fecha de estreno

---

# 🚀 Instalación

Clonar el repositorio:

```
git clone https://github.com/tuusuario/movie-data-pipeline.git
cd movie-data-pipeline
```

Instalar dependencias:

```
pip install -r requirements.txt
```

---

# ▶️ Ejecución

Abrir el notebook:

```
notebooks/movie_dataset_engineering.ipynb
```

El notebook ejecuta todo el pipeline:

1. carga de datasets de IMDb
2. filtrado de películas relevantes
3. enriquecimiento mediante TMDb API
4. almacenamiento en MongoDB
5. consultas sobre la base de datos

---

# 💾 Sistema de backup

Para evitar repetir llamadas a la API y mejorar la eficiencia del pipeline, los resultados de TMDb se almacenan en un **backup JSON incremental**.

Esto permite:

* reanudar la ejecución si el proceso se interrumpe
* evitar llamadas duplicadas a la API
* reducir tiempos de ejecución

---

# 🔎 Ejemplos de consultas

El proyecto incluye ejemplos de consultas sobre MongoDB como:

* películas mejor valoradas
* filtrado por género
* búsquedas por palabras clave
* análisis de popularidad

---

# 📂 Estructura del repositorio

```
movie-data-pipeline
│
├── notebooks
│   └── movie_dataset_engineering.ipynb
│
├── data
│
├── requirements.txt
└── README.md
```

---

# 🎯 Objetivo del proyecto

Este proyecto forma parte de mi portfolio de **Data Engineering y Data Science** y demuestra habilidades en:

* integración de múltiples fuentes de datos
* consumo de APIs
* procesamiento de datos con Python
* modelado y almacenamiento en bases de datos NoSQL
* construcción de pipelines de datos reproducibles

---

# 📬 Autor

Proyecto desarrollado como parte de mi portfolio de proyectos de **Ingeniería de Datos en la Nube y Ciencia de Datos**.
