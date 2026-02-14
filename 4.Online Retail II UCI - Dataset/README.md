# Retail Intelligence Pipeline: End-to-End Data Engineering & Customer Analytics

![SQL](https://img.shields.io/badge/SQL-SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Python](https://img.shields.io/badge/Python-Pandas-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

## 📌 Descripción del Proyecto
Este proyecto documenta la construcción de un pipeline de datos completo para un dataset de retail de más de 500k registros transaccionales. El objetivo principal fue transformar datos crudos en insights accionables mediante una arquitectura robusta, aplicando análisis de **Churn (Fuga de clientes)** y segmentación avanzada **RFM**.

## ⚙️ Metodología de Trabajo: Proceso ETL
Para garantizar la integridad y calidad de la información, el proyecto se desarrolló bajo una metodología rigurosa de 6 pasos:
1. **Extracción:** Ingesta de archivos planos y conexión de fuentes.
2. **Limpieza:** Identificación y tratamiento de nulos, duplicados e inconsistencias.
3. **Transformación:** Normalización de tablas y creación de métricas de negocio.
4. **Carga:** Migración de datos procesados a un entorno SQL.
5. **Análisis:** Aplicación de lógica estadística y segmentación de clientes.
6. **Visualización:** Diseño de dashboards estratégicos para la toma de decisiones.

---

## 🛠️ Desarrollo Técnico

### 1. Análisis Exploratorio y Limpieza (Python)
Utilicé **Python (Pandas)** como motor principal para el procesamiento inicial de los datos:
* **Limpieza Profunda:** Normalización de descripciones de productos y resolución de problemas de integridad (IDs de clientes huérfanos, formatos, registros nulos y eliminación de duplicados).
* **Análisis Visual:** Uso de **Matplotlib** y **Seaborn** para identificar distribuciones, tendencias temporales y detectar *outliers* antes de la fase de carga.

### 2. Procesamiento Avanzado de Datos (SQL)
La lógica de negocio pesada se consolidó en **SQLite**, priorizando la eficiencia y la escalabilidad del análisis:
* **Common Table Expressions (CTEs):** Implementadas para estructurar consultas complejas en pasos lógicos y legibles.
* **Window Functions:** Aplicadas para calcular el comportamiento histórico del consumidor, pieza clave para determinar la **Tasa de Churn** (fuga de clientes).
* **Arquitectura Relacional:** Diseño de un esquema de datos optimizado para su consumo en herramientas de BI.

### 3. Descubrimiento Estratégico: Metodología RFM
Durante la fase de análisis, se integró la metodología **RFM** (Recencia, Frecuencia, Valor Monetario) como una herramienta de mejor ajuste a una organización de retail. Este descubrimiento permitió clasificar a los clientes en segmentos estratégicos como *Campeones, Clientes Leales y Usuarios en Riesgo*, proporcionando una capa de inteligencia de negocio superior al reporte estándar.

### 4. Visualización y Entrega (Power BI)
El dashboard final fue diseñado bajo una estética profesional de retail, enfocándose en la experiencia del usuario (UX):
* **KPIs Estratégicos:** Visualización clara de Ticket Promedio, Volumen de Ventas y Retención de Clientes.
* **Ayuda Contextual:** Implementación de *tooltips* explicativos para facilitar la interpretación de métricas a stakeholders no técnicos.
* **Higiene del Modelo:** Ocultamiento de cálculos técnicos para un entorno de autoservicio de datos limpio.
![Dashboard en acción](demo_dashboard.gif)
---

## 🚀 Habilidades Clave Demostradas
* **Data Engineering:** Diseño de procesos ETL y gestión de bases de datos relacionales.
* **SQL Avanzado:** Uso de CTEs y Window Functions para analítica descriptiva de alto nivel.
* **Análisis de Negocio:** Cálculo de métricas de retención (Churn) y segmentación RFM.
* **Data Storytelling:** Capacidad de comunicar hallazgos complejos a través de una narrativa visual profesional.

---

### 📂 Estructura del Repositorio
* `/scripts`: Proceso de limpieza y EDA con Python, consultas integradas con SQL bajo la lógica de CTEs y funciones de ventana. Incluye fuente de datos en documento CSV, base de datos creada en Python y notebook de Jupyter
* `/dashboard`: Archivo `.pbix` con el informe inter activo final.

---