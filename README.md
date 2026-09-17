# 📊 Proyecto de Análisis de Datos: Comportamiento y Segmentación de Clientes | ConnectaTel

## 🏢 Contexto del Negocio
**ConnectaTel** es una compañía de telecomunicaciones con operaciones en México y Colombia. Este proyecto forma parte del análisis integral para entender cómo los usuarios utilizan realmente los servicios móviles (llamadas y mensajes). El objetivo principal es identificar patrones de consumo, detectar comportamientos atípicos (outliers / *power users*) y segmentar a la base de clientes para optimizar la oferta comercial y mejorar la experiencia del usuario.

---

## 🛠️ Herramientas y Tecnologías
* **Lenguaje:** Python
* **Librerías de Análisis y Procesamiento:** `pandas`, `numpy`
* **Librerías de Visualización:** `seaborn`, `matplotlib`
* **Entorno de Trabajo:** Jupyter Notebook

---

## 🗂️ Estructura de los Datasets
El análisis integra tres fuentes de información principales:
1. **`plans.csv`**: Catálogo de planes actuales (precio, minutos incluidos, GB incluidos y costo por excedente).
2. **`users_latam.csv`**: Información demográfica y de registro de los clientes (edad, ciudad, fecha de registro, plan contratado y estado de *churn*).
3. **`usage.csv`**: Detalle de la actividad real generada por los usuarios (llamadas, duración, mensajes).

---

## 🔍 Fases del Proyecto y Metodología

1. **Integración y Limpieza de Datos:** 
   * Carga y unificación de las fuentes de datos (`plans`, `users_latam`, `usage`).
   * Validación de tipos de datos, manejo de valores nulos y estandarización de registros.
2. **Análisis Estadístico y Detección de Outliers:**
   * Uso del Rango Intercuartílico (IQR) para identificar límites superiores en variables de actividad (`cant_mensajes`, `cant_llamadas`, `cant_minutos_llamada`).
   * Evaluación de valores extremos, determinando su validez como *power users* / clientes de alto valor (*whales*) en lugar de errores de sistema.
3. **Ingeniería de Características y Segmentación:**
   * **Grupo de Uso (`grupo_uso`):** Clasificación en *Bajo uso*, *Uso medio* y *Alto uso* basada en umbrales combinados de mensajes y llamadas.
   * **Grupo de Edad (`grupo_edad`):** Segmentación etaria en *Jóvenes* (<30 años), *Adultos* (30-59 años) y *Adultos Mayores* (60+ años).
4. **Visualización de Datos:**
   * Generación de gráficos de distribución (`sns.countplot`, boxplots) para contrastar el comportamiento entre segmentos.
5. **Insights Ejecutivos y Recomendaciones:**
   * Traducción de los hallazgos técnicos en propuestas comerciales orientadas a la retención de la masa crítica de adultos, la monetización de *power users* y estrategias de atracción para el segmento joven.

---

## 💡 Principales Hallazgos y Conclusiones
* **Masa Crítica:** El segmento de **Adultos** (aprox. 2,000 usuarios) y el grupo de **Uso medio** (casi 3,000 usuarios) concentran el núcleo principal de ingresos y estabilidad operativa de la compañía.
* **Comportamientos Extremos:** Se identificaron *outliers* significativos en los minutos de llamada (alcanzando hasta 155.69 minutos, muy por encima del límite IQR), definiendo un valioso segmento de *power users*.
* **Oportunidad de Mercado:** El segmento **Joven** registró menor participación (aprox. 750 usuarios), abriendo la puerta a campañas de captación digital enfocadas y planes a la medida.

---

## 🚀 Cómo Reproducir el Análisis
1. Clona este repositorio en tu máquina local:
 https://github.com/DanielaMuriel-Data/Telecom-analysis.git

---

# 📊 Data Analysis Project: Customer Behavior & Segmentation | ConnectaTel

## 🏢 Business Context
**ConnectaTel** is a telecommunications company operating in Mexico and Colombia. This project is part of an end-to-end analysis to understand how users actually utilize mobile services (calls and messages). The core objective is to identify consumption patterns, detect atypical behaviors (outliers / *power users*), and segment the customer base to optimize commercial offerings and enhance user experience.

---

## 🛠️ Tools & Technologies
* **Language:** Python
* **Analysis & Processing Libraries:** `pandas`, `numpy`
* **Visualization Libraries:** `seaborn`, `matplotlib`
* **Work Environment:** Jupyter Notebook

---

## 🗂️ Dataset Structure
The analysis integrates three main data sources:
1. **`plans.csv`**: Current plan catalog (price, included minutes, included GB, and extra usage cost).
2. **`users_latam.csv`**: Customer demographics and registration data (age, city, registration date, contracted plan, and churn status).
3. **`usage.csv`**: Real user activity details (calls, duration, messages).

---

## 🔍 Project Phases & Methodology

1. **Data Integration & Cleaning:** 
   * Loading and merging data sources (`plans`, `users_latam`, `usage`).
   * Data type validation, missing value handling, and record standardization.
2. **Statistical Analysis & Outlier Detection:**
   * Using the Interquartile Range (IQR) to identify upper limits in activity variables (`cant_mensajes`, `cant_llamadas`, `cant_minutos_llamada`).
   * Evaluating extreme values, determining their validity as *power users* / high-value clients (*whales*) rather than system errors.
3. **Feature Engineering & Segmentation:**
   * **Usage Group (`grupo_uso`):** Classification into *Bajo uso* (Low usage), *Uso medio* (Medium usage), and *Alto uso* (High usage) based on combined message and call thresholds.
   * **Age Group (`grupo_edad`):** Age segmentation into *Jóvenes* (<30 years), *Adultos* (30-59 years), and *Adultos Mayores* (60+ years).
4. **Data Visualization:**
   * Generating distribution plots (`sns.countplot`, boxplots) to contrast behaviors across segments.
5. **Executive Insights & Recommendations:**
   * Translating technical findings into commercial proposals aimed at retaining the critical adult mass, monetizing *power users*, and attracting the younger segment.

---

## 💡 Key Findings & Conclusions
* **Critical Mass:** The **Adults** segment (approx. 2,000 users) and the **Medium Usage** group (nearly 3,000 users) concentrate the core revenue and operational stability of the company.
* **Extreme Behaviors:** Significant *outliers* were identified in call minutes (reaching up to 155.69 minutes, well above the IQR limit), defining a valuable segment of *power users* (*whales*).
* **Market Opportunity:** The **Youth** segment showed lower participation (approx. 750 users), opening the door to targeted digital acquisition campaigns and customized plans.

---

## 🚀 How to Reproduce the Analysis
1. Clone this repository to your local machine:
 https://github.com/DanielaMuriel-Data/Telecom-analysis.git

