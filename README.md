¡Aquí tienes el README con formato, claro y conciso!

# 📊 Análisis Exploratorio del Conjunto de Datos de Préstamos de Kiva

## 🚀 Conclusión del Proyecto

Este proyecto consistió en un **Análisis Exploratorio de Datos (EDA)** exhaustivo sobre el conjunto de datos de préstamos de la plataforma **Kiva.org** (financiación colectiva). El objetivo principal fue comprender las características de los préstamos, identificar patrones clave y visualizar tendencias geográficas y temporales.

El *dataset* principal, `'Kiva Crowdfunding'`, fue descargado de Kaggle y proporcionado por la organización Kiva.org.

---

## 🛠️ Herramientas y Librerías Principales

| Categoría | Librerías Utilizadas | Propósito |
| :--- | :--- | :--- |
| **Manipulación** | `pandas`, `numpy` | Limpieza, preparación y operaciones numéricas de datos. |
| **Visualización Estándar** | `matplotlib`, `seaborn` | Creación de gráficos estadísticos y de distribución. |
| **Geoespacial** | `geopandas`, `folium` | Análisis geoespacial y creación de mapas coropléticos interactivos. |
| **Diagnóstico** | `missingno` | Visualización y análisis de datos faltantes. |

---

## ✅ Pasos Clave y Resultados Obtenidos

A través de rigurosos pasos de preprocesamiento y análisis, se obtuvieron las siguientes ideas y resultados clave:

### 1. Limpieza y Preparación de Datos

* **Eliminación de Columnas:** Se eliminaron columnas con alta redundancia o gran cantidad de valores faltantes (ej. `country_code`, `tags`, `partner_id`, `borrower_genders`, `date`, `funded_time`, `region`, `use`).
* **Conversión de Tiempo:** Las columnas de tiempo (`posted_time`, `disbursed_time`) fueron convertidas al formato `datetime` y normalizadas.
* **Clasificación de Préstamos:** Se identificaron y categorizaron los préstamos como **'pre\_disbursed'** o **'post\_disbursed'** basándose en la relación temporal entre el tiempo de publicación y el desembolso.

### 2. Análisis de Distribución de Montos

* **Categorización:** Los montos de los préstamos (`loan_amount`) se clasificaron en cuatro categorías (`micro`, `small`, `medium`, `large`) para un análisis más granular.
* **Hallazgo:** Se reveló que la mayoría de los préstamos se concentran en las categorías **'micro'** y **'small'**.
* **Detección de Outliers:** Se detectaron y cuantificaron los *outliers* en las categorías de monto, crucial para entender la variabilidad y posibles anomalías.

### 3. Impacto Geográfico y Sectorial

* **Países Principales:** Se identificaron los **10 países con mayores montos financiados**, destacando las regiones con mayor actividad crediticia.
* **Sectores Apoyados:** Se analizó la distribución de préstamos por **sector**, mostrando cuáles son las áreas de negocio más apoyadas por Kiva (ej. agricultura, servicios, comercio minorista).

### 4. Análisis Temporal y Geoespacial

* **Tendencias Temporales:** Se exploró la evolución mensual de los **montos promedio** y los **montos financiados totales** para observar tendencias a lo largo del tiempo.
* **Visualización Global:** Se creó un **mapa coroplético interactivo** usando `geopandas` y `folium` para visualizar los montos totales de préstamo por país, ofreciendo una perspectiva global del impacto de Kiva. 

---

## 💡 Conclusión General

Este proyecto proporcionó una comprensión profunda de la dinámica de los préstamos de Kiva. Se demostró la importancia de una **limpieza de datos rigurosa** y un análisis exploratorio detallado para descubrir información valiosa. Los resultados permiten identificar las categorías de préstamos más comunes, así como los países y sectores con mayor actividad crediticia.

Los *insights* obtenidos de este análisis pueden ser utilizados por Kiva o investigadores para tomar **decisiones informadas** sobre la asignación de recursos y para futuras investigaciones sobre el impacto de los microcréditos.

El conjunto de datos limpio y preprocesado se ha guardado como **`df_clean.csv`** para facilitar análisis posteriores.
