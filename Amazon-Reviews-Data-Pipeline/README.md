# Amazon Reviews Data Pipeline

**Distributed Batch & Streaming Processing with Apache Spark and AWS**

## 📌 Overview

Pipeline de procesamiento distribuido sobre el conjunto de datos Amazon Customer Reviews mediante Apache Spark, PySpark y servicios de AWS.

El proyecto integra procesamiento batch, análisis exploratorio, transformación de texto, entrenamiento de modelos de clasificación y procesamiento de eventos en streaming.

## ✨ Main Features

- Procesamiento distribuido con Apache Spark y PySpark.
- Análisis exploratorio de reseñas de productos.
- Limpieza y transformación de datos textuales.
- Entrenamiento de modelos de regresión logística y árbol de decisión mediante Spark ML.
- Evaluación y persistencia de modelos en Amazon S3.
- Procesamiento de eventos mediante Spark Structured Streaming.
- Integración con Amazon Kinesis Data Streams.
- Análisis de sentimiento mediante Amazon Comprehend.
- Simulación local de streaming con clasificación basada en palabras clave.

## 💻 Technologies

- **Cloud:** AWS, Amazon S3, Amazon EMR, Kinesis Data Streams, Amazon Comprehend.
- **Big Data:** Apache Spark, PySpark, Spark Structured Streaming.
- **Machine Learning:** Spark ML, TF-IDF, Logistic Regression, Decision Tree.
- **Programming:** Python, SQL, Boto3.
- **Data Analysis:** Pandas, NumPy, Matplotlib, Seaborn.

## 📋 Data Source

Amazon Customer Reviews — Electronics.

Los datos se obtienen desde el repositorio [polinaeterna/amazon_us_reviews](https://huggingface.co/datasets/polinaeterna/amazon_us_reviews) en Hugging Face, utilizando la configuración `Electronics_v1_00`.

El conjunto de datos debe descargarse y ubicarse en la carpeta `data/` del proyecto. No se incluye en este repositorio.

## 🗂️ Project Structure

```text
Amazon-Reviews-Data-Pipeline/
├── notebooks/
│   └── amazon_reviews_data_pipeline.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## ▶️ Execution

1. Instalar las dependencias de Python indicadas en `requirements.txt`.
2. Configurar Java y Apache Spark.
3. Descargar el conjunto de datos y preparar la carpeta `data/`.
4. Configurar las credenciales y permisos IAM necesarios para los servicios de AWS.
5. Abrir y ejecutar el notebook.

La ejecución local permite trabajar con el procesamiento batch y la simulación de streaming. Las integraciones con S3, Kinesis y Amazon Comprehend requieren la configuración correspondiente de AWS.

