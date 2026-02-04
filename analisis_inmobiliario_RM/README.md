# 🏠 Análisis del Mercado Inmobiliario - Región Metropolitana (2023)

## 📌 Descripción del Proyecto
Este proyecto se centra en la integración, limpieza y visualización de datos inmobiliarios de la Región Metropolitana de Chile. El objetivo principal fue consolidar datos provenientes de distintas campañas de web scraping para generar un repositorio único y confiable que permita analizar tendencias de precios, oferta por comuna y características de las propiedades.

## 🛠️ Stack Tecnológico
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=microsoftpowerbi&logoColor=black)
* **Python (Pandas, NumPy):** Procesamiento de datos y ETL.
* **Jupyter Notebook:** Documentación y ejecución del pipeline de limpieza.
* **Power BI:** Modelado de datos y dashboard interactivo.

## ⚙️ Proceso de Ingeniería de Datos (ETL)
El procesamiento se dividió en tres etapas críticas documentadas en el notebook de este repositorio:

1. **Carga y Unión:** Se integraron dos datasets provenientes de fuentes distintas(`2023-03-08 Precios Casas RM.csv` y `2023-07-18 Propiedades Web Scrape.csv`).
2. **Data Cleaning:** - **Duplicados:** Se identificaron y eliminaron registros repetidos utilizando la columna `id` como llave primaria, consolidando un dataset de **13,436 propiedades únicas**.
   - **Gestión de Nulos:** Se realizó un diagnóstico de valores faltantes, detectando que la columna `Parking` presentaba **5,021 registros nulos**, lo que condicionó el análisis de esta variable.
   - **Estandarización:** Normalización de formatos numéricos para precios en UF y CLP para asegurar la compatibilidad con Power BI.
3. **Exportación:** Generación del archivo final `df_propiedades.csv`.

## 📈 Visualización
![Dashboard en acción](Demo_dashboard.GIF)

## 📊 Hallazgos y Resultados
A través del dashboard de Power BI se obtuvieron los siguientes insights:

* **Distribución Geográfica:** Identificación de las comunas con mayor volumen de oferta y comparación de precios promedio.
* **Relación de Superficie:** Análisis de la correlación entre `Built Area` y `Price_UF` para detectar desviaciones de mercado.
* **Perfil de Propiedad:** La mayoría de la oferta analizada se concentra en viviendas de 3 a 4 dormitorios, con una presencia relevante de corredores de propiedades (Realtors) específicos en la zona.

## 🚀 Estructura del Repositorio
* `scripts/`: Contiene el notebook `analisis_inmobiliario_RM.ipynb` con el código de limpieza.
* `data/`: Datasets originales y el archivo resultante del proceso ETL.
* `dashboard/`: Archivo `.pbix` con la visualización interactiva.

---
*Proyecto desarrollado como parte del análisis de datos inmobiliarios en la RM.*
