## © Derechos de Autor
Todos los derechos reservados.

# Análisis y Predicción del Consumo Energético

Este proyecto analiza el consumo energético de una comunidad en París, utilizando técnicas de análisis de datos y aprendizaje automático para identificar patrones de consumo y predecir tendencias.

## Objetivos
- Comprender la evolución del consumo energético en diferentes sectores.
- Evaluar la calidad de los datos y detectar anomalías.
- Aplicar técnicas de clustering para segmentar los tipos de consumo.
- Implementar modelos de predicción basados en series temporales.

## Tecnologías Seleccionadas

### 1. Dask
**Descripción:**
Dask es un framework de computación distribuida diseñado para extender las capacidades de Pandas y NumPy en Python, facilitando el manejo de grandes volúmenes de datos que no caben en memoria RAM.

- **Operaciones Distribuidas:** Permite procesar datasets particionados utilizando múltiples CPUs en paralelo.
- **Compatibilidad con Scikit-learn y TensorFlow:** Facilita el preprocesamiento distribuido y la implementación de modelos escalables.

**Justificación:**
El dataset del proyecto contiene más de 2 millones de registros recolectados minuto a minuto, lo que impone desafíos de capacidad y rendimiento en herramientas tradicionales.

- **Procesamiento de Series Temporales:** Resampleo, normalización y creación de secuencias optimizadas.
- **Clustering Distribuido:** Integración con Dask-ML para aplicar algoritmos como K-means en grandes volúmenes de datos.

**Ventajas:**
- Escalabilidad eficiente para datasets masivos.
- Operaciones en memoria adaptadas a sistemas con recursos limitados.

**Desventajas:**
- Curva de aprendizaje debido a su naturaleza distribuida.

### 2. Dask-ML
**Descripción:**
Dask-ML es una extensión de Scikit-learn que optimiza algoritmos de Machine Learning para la computación distribuida con Dask.

- Soporta algoritmos como K-means, GridSearchCV y métricas a gran escala.
- Utiliza particiones de Dask para entrenar modelos en paralelo.

**Justificación:**
El proyecto requiere aplicar técnicas de Clustering (K-means) y optimización de hiperparámetros mediante GridSearch de manera eficiente en datasets distribuidos.

**Ventajas:**
- Permite escalar modelos de Machine Learning en sistemas con recursos limitados.
- Facilita el ajuste de hiperparámetros y evaluación paralelizada.

### 3. TensorFlow/Keras
**Descripción:**
Biblioteca de aprendizaje profundo utilizada para implementar redes neuronales, como LSTM (Long Short-Term Memory).

- Entrenamiento eficiente en GPUs.
- Integración con datos resampleados desde Dask para series temporales.

**Justificación:**
Se requiere un modelo LSTM para capturar dependencias no lineales y temporales en los datos de consumo energético. TensorFlow permite optimizar la red neuronal y acelerar el entrenamiento.

**Ventajas:**
- Compatible con procesamiento en la nube (Google Colab con GPU).
- Permite ajustar parámetros como learning rate, unidades y secuencias temporales.

### 4. Matplotlib y Seaborn
**Descripción:**
Bibliotecas de visualización utilizadas para análisis exploratorio y representación de datos a nivel local.

**Justificación:**
Facilitan la exploración inicial y la identificación de patrones y distribuciones en los datos.


## Contenido del Proyecto
- `dataset/`: Datos utilizados para el análisis. https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption
- `notebooks/`: Cuadernos de Jupyter con el análisis y visualizaciones.

## Uso
Para ejecutar el análisis, clona este repositorio y abre los cuadernos de Jupyter en un entorno con las librerías necesarias instaladas:
```bash
pip install -r requirements.txt
jupyter notebook
```

## Contribución
Este es un proyecto de investigación personal. Si deseas contribuir, por favor abre un issue o un pull request.

---

## © Copyright
All rights reserved.

# Energy Consumption Analysis and Prediction

This project analyzes energy consumption in a Parisian community, using data analysis and machine learning techniques to identify consumption patterns and predict trends.

## Objectives
- Understand the evolution of energy consumption in different sectors.
- Evaluate data quality and detect anomalies.
- Apply clustering techniques to segment consumption types.
- Implement predictive models based on time series.

## Selected Technologies

### 1. Dask
**Description:**
Dask is a distributed computing framework that extends Pandas and NumPy capabilities, making it easier to handle large datasets that do not fit in RAM.

- **Distributed Operations:** Processes partitioned datasets using multiple CPUs in parallel.
- **Compatibility with Scikit-learn and TensorFlow:** Enables distributed preprocessing and scalable model implementation.

**Justification:**
The dataset contains over 2 million records collected minute by minute, posing performance and capacity challenges for traditional tools.

- **Time Series Processing:** Resampling, normalization, and optimized sequence creation.
- **Distributed Clustering:** Integration with Dask-ML to apply algorithms like K-means on large datasets.

**Advantages:**
- Efficient scalability for massive datasets.
- In-memory operations adapted to limited-resource systems.

**Disadvantages:**
- Learning curve due to its distributed nature.

### 2. Dask-ML
**Description:**
Dask-ML is an extension of Scikit-learn optimized for distributed machine learning computation with Dask.

- Supports algorithms like K-means, GridSearchCV, and large-scale metrics.
- Uses Dask partitions to train models in parallel.

**Justification:**
The project requires clustering techniques (K-means) and hyperparameter tuning via GridSearch efficiently on distributed datasets.

**Advantages:**
- Enables scalable machine learning models on resource-limited systems.
- Facilitates hyperparameter tuning and parallel evaluation.

### 3. TensorFlow/Keras
**Description:**
Deep learning library used to implement neural networks, such as LSTMs (Long Short-Term Memory).

- Efficient GPU training.
- Integration with resampled data from Dask for time series analysis.

**Justification:**
An LSTM model is required to capture nonlinear and temporal dependencies in energy consumption data. TensorFlow optimizes the neural network and accelerates training.

**Advantages:**
- Compatible with cloud processing (Google Colab with GPU).
- Allows tuning parameters like learning rate, units, and time sequences.

### 4. Matplotlib and Seaborn
**Description:**
Visualization libraries used for exploratory analysis and data representation at a local level.

**Justification:**
They facilitate initial exploration and pattern identification in the data.

## Project Content
- `dataset/`: Data used for the analysis. https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption
- `notebooks/`: Jupyter notebooks with analysis and visualizations.

## Usage
To run the analysis, clone this repository and open the Jupyter notebooks in an environment with the required libraries installed:
```bash
pip install -r requirements.txt
jupyter notebook
```

## Contribution
This is a personal research project. If you wish to contribute, please open an issue or a pull request.

