# 🔬 Proyecto_Melanoma: DESARROLLO DE UN MODELO DE INTELIGENCIA ARTIFICIAL BASADO EN REDES NEURONALES CONVOLUCIONALES (CNN) PARA EL DIAGNÓSTICO TEMPRANO DE CÁNCER DE PIEL

## 📌 Introducción

Este repositorio contiene el código fuente para el proyecto de tesis enfocado en el **diagnóstico asistido por computadora (CAD)** de Melanoma, utilizando técnicas de **Deep Learning** y **Computer Vision**.

El objetivo principal es clasificar imágenes dermatoscópicas en dos clases binarias: **Melanoma** (maligno) y **No Melanoma** (benigno).

## 🚀 Metodología y Arquitectura

El modelo de clasificación se implementó utilizando una **Red Neuronal Convolucional (CNN)**, fundamentada en la arquitectura pre-entrenada **VGG16** bajo la técnica de **Transfer Learning (TL)**.

La implementación se realizó en un entorno de **Google Colab**, aprovechando las capacidades de procesamiento de su GPU.

* **Algoritmo de optimización:** Adam
* **Función de Pérdida:** Binary Cross-Entropy (Entropía Cruzada Binaria)
* **Estrategia de Optimización:** Implementación de **Early Stopping** en la Época 3 para mitigar el sobreajuste (*overfitting*), con base en la Pérdida de Validación (mínimo de 0.4954).

## 📊 Resultados Clave

El modelo final fue evaluado en un conjunto de prueba independiente para determinar su rendimiento objetivo.

| Métrica | Valor Reportado | Significado |
| :--- | :--- | :--- |
| **Precisión General (Accuracy)** | **73.79%** | Porcentaje de clasificaciones correctas. |
| **Área Bajo la Curva (AUC)** | **0.8389** | Capacidad discriminatoria global del modelo. |
| **Sensibilidad (Recall)** | **72.15%** | Capacidad de detectar correctamente los casos de Melanoma (Verdaderos Positivos). |
| **Especificidad** | **75.40%** | Capacidad de detectar correctamente los casos No Melanoma (Verdaderos Negativos). |

## 📦 Entregables y Recursos

Este proyecto se compone de dos entregables clave: el código y el conjunto de datos.

| Recurso | Descripción | Enlace/Nombre |
| :--- | :--- | :--- |
| **Código Fuente** | Libreta de Google Colab (`Proyecto_Melanoma.ipynb`) con todo el proceso de carga, preprocesamiento, entrenamiento y evaluación. | [Aquí se genera el enlace de GitHub] |
| **Conjunto de Datos** | Imágenes preprocesadas, aumentadas y listas para el entrenamiento (divididas en `entrenamiento`, `validación` y `prueba`). | [Conjunto de datos preprocesados de melanoma vs. sin melanoma](https://www.kaggle.com/datasets/leydygalindovertel/melanoma-vs-no-melanoma-preprocessed-dataset) |


1.  **Abrir en Colab:** Haga clic en el botón "Open in Colab" (si se incluyó al subirlo).
2.  **Cargar Datos:** El *notebook* asume que el conjunto de datos de Kaggle está montado en el entorno de ejecución.
3.  **Ejecutar celdas:** Ejecute las celdas de manera secuencial para replicar el preprocesamiento, el entrenamiento (el cual se detendrá en la Época 3) y la evaluación de las métricas.
