# 📊 Challenge de Ciencia de Datos - Análisis de Evasión de Clientes (Churn) en Telecom X

## 🎯 Objetivo del Proyecto
El propósito de este proyecto es realizar un **Análisis Exploratorio de Datos (EDA)** detallado sobre el problema de la **Evasión de Clientes (Churn)** en la empresa **Telecom X**. El objetivo final fue identificar y cuantificar los factores de mayor riesgo para la pérdida de clientes, generando un **Informe de Insights** que sirva como base estratégica para la prevención y el desarrollo de modelos predictivos.

## 🔑 Análisis y Hallazgos Clave
El análisis se centró en un riguroso proceso **ETL (Extracción, Transformación y Carga)** para preparar los datos, seguido del análisis bivariado de las variables de servicio, demográficas y financieras contra la variable objetivo `Evasion`.

## 💡 Conclusión Ejecutiva
Basado en la evaluación integral, se concluye que el riesgo de evasión está directamente ligado al **bajo compromiso contractual** y a la **insatisfacción con servicios de alto valor**. El enfoque estratégico debe ser doble: **incentivar la migración de contratos mensuales a anuales** y **monitorear proactivamente la calidad del servicio premium** (Fibra Óptica) en los primeros seis meses de relación con el cliente.

## 📈 Métricas y Análisis Clave
* **Tasa de Evasión (Churn Rate):** Se calculó la proporción de clientes que evadieron, estableciendo la urgencia del problema (aproximadamente **26.5%** de tasa de churn).
* **Riesgo por Compromiso (Tipo de Contrato):** Se demostró que los clientes con **Contratos Mensuales** tienen el mayor riesgo, con una tasa de evasión muy superior a la de los contratos de largo plazo.
* **Riesgo por Antigüedad:** El análisis de la distribución de `Antiguedad_Meses` reveló que la evasión es primordialmente un problema de **clientes nuevos** (mediana de antigüedad significativamente más baja para el grupo que evadió).
* **Riesgo Financiero:** Se identificó que clientes con **Costo Mensual alto** (paquetes premium) son más propensos a la evasión, indicando una posible disconformidad entre el precio y la calidad percibida.
* **Correlación de Servicios (Feature Engineering):** Se creó la variable `Cantidad_Servicios` y se demostró una correlación negativa: a mayor cantidad de *add-ons* contratados (e.g., Soporte Técnico, Seguridad Online), **menor es la probabilidad de evasión**.

## 📊 Visualizaciones Clave
Se generaron gráficos esenciales para validar y comunicar los insights más fuertes:
1.  **Gráfico de Barras de Churn Rate:** Muestra la distribución general de la evasión en el dataset.
2.  **Gráfico de Barras Apiladas (Tipo de Contrato):** Compara la tasa de evasión por el tipo de compromiso contractual, identificando el Contrato Mensual como el factor de riesgo crítico.
3.  **Boxplot (Antigüedad vs. Evasión):** Evidencia la rápida pérdida de clientes nuevos frente a la estabilidad de los clientes antiguos.

## 💻 Estructura y Tecnologías
El proyecto se desarrolló siguiendo el flujo de trabajo de análisis de datos con énfasis en la preparación del dataset:
* **Consolidación y Aplanamiento:** Conversión de la estructura anidada JSON a un DataFrame tabular plano y limpio.
* **Limpieza de Datos:** Corrección del error de tipo de dato en la columna `Total_Gastado` y estandarización de variables binarias a 0/1.
* **Feature Engineering:** Creación de las columnas `Costo_Diario` y `Cantidad_Servicios`.

### Tecnologías Utilizadas
* **Python:** Lenguaje principal de análisis.
* **Pandas / NumPy:** Para ETL, Feature Engineering y el cálculo de la matriz de correlación.
* **Matplotlib / Seaborn:** Para la generación de visualizaciones bivariadas y univariadas.
* **Scikit-Learn:** Para la implementación de modelos de Machine Learning (Regresión Logística y Random Forest) y técnicas de balanceo (SMOTE).

## 📁 Contenido del Repositorio
* **TelecomX_LATAM.ipynb:** Contiene todo el código fuente del análisis, desde la carga y limpieza de datos hasta el cálculo de todas las métricas, la generación de visualizaciones, y el informe final.
* **README.md:** Documento actual que presenta la justificación, hallazgos clave, y la recomendación final del análisis.

## ✨ Posibles Mejoras (Adicionales)
* **Modelado Predictivo Avanzado:** Utilizar técnicas de *Hyperparameter Tuning* en modelos como XGBoost o LightGBM para mejorar el F1-Score.
* **Análisis de Rentabilidad:** Calcular el **Costo de Adquisición del Cliente (CAC)** y compararlo con el **Valor de Vida del Cliente (LTV)** para los diferentes segmentos de riesgo identificados.
