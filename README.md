# 📊 Análisis Visual y Exploratorio de Factores Económicos (NUTS 2) (España | UE)

> **Proyecto Final - Análisis Exploratorio de Datos y Visualización (AEDV)**
> 
[![R](https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white)](https://www.r-project.org/)
[![Methodology](https://img.shields.io/badge/Methodology-CRISP--DM-orange?style=flat-square)]()
[![Data](https://img.shields.io/badge/Source-Eurostat-blue?style=flat-square)](https://ec.europa.eu/eurostat)
[![Tecnologías](https://skillicons.dev/icons?i=r,github,windows&perline=4)](https://skillicons.dev)
## 📝 Descripción
Este proyecto realiza un análisis profundo de los ingresos de los hogares en regiones europeas, siendo uno de los focos centrales España (**NUTS 2**). 
Se ha estructurado siguiendo el estándar **CRISP-DM** (*Cross-Industry Standard Process for Data Mining*) para garantizar un flujo de trabajo reproducible y orientado a resultados técnicos y de negocio.

## 🚀 Accesos directos
* 📄 **[Ver Memoria del Proyecto (Web)](https://aythamilorenzo.github.io/Analisis-ingresos-de-los-hogares-NUTS2/ModeloMemoriaProyectoPersonalAEDV.html)**
* 🌍 **[Ver Cuadro de Mandos del Proyecto (Web)](https://aythamilorenzo.shinyapps.io/dashboardproyectopersonal/)**

## 🔄 Ciclo de Vida del Proyecto

### 1. Business Understanding
El objetivo principal es identificar y cuantificar las disparidades económicas regionales dentro de la Unión Europea. Se busca responder a:
* ¿Cuáles son las brechas de ingresos entre las regiones más y menos favorecidas?
* ¿Existe un patrón geográfico claro (Norte-Sur / Este-Oeste)?

### 2. Data Understanding
Utilización de microdatos oficiales de **Eurostat**, específicamente el dataset `nama_10r_2hhinc`. Se analizan variables de ingresos brutos, impuestos y transferencias sociales para calcular la renta disponible real por habitante. Además
se utiliza un dataset secundario de poblacion para convertir datos a **per cápita**.

### 3. Data Preparation
* **Filtrado:** Limpieza de niveles jerárquicos NUTS 0 y 1 para aislar el análisis en el nivel regional (NUTS 2).
* **Merging:** Cruce de datos económicos con censos de población para obtener métricas per cápita.
* **Wrangling:** Gestión de valores ausentes (NAs) y normalización de moneda.

### 4. Modeling
* **Análisis Exploratorio (EDA):** Generación de estadísticas descriptivas robustas.
* **Geospatial Analysis:** Creación de mapas coropléticos utilizando la librería `sf` para visualizar la distribución espacial de la riqueza.

### 5. Evaluation
Contraste de los hallazgos con los informes de cohesión de la Comisión Europea. Los resultados confirman la persistencia de brechas estructurales a pesar de los fondos de convergencia.

### 6. Deployment
Despliegue de resultados mediante un informe dinámico en **R Markdown**, diseñado para ser exportado a PDF o HTML, y un **cuadro de mandos** desarrollado con la librería shiny, permitiendo una lectura técnica y ejecutiva simultánea.

---


## 📂 Estructura del Proyecto
* `utilidades.R`: Scripts de soporte con funciones utilizadas en las distintas gráficas.
* `ModeloMemoriaProyectoPersonalAEDV.Rmd`: Código en bruto sobre el desarrollo del proyecto.
* `ModeloMemoriaProyectoPersonalAEDV.html`: Cuaderno maestro con el desarrollo de las 6 fases.
* `poblacion.csv` / `nama_10r_2hhinc.csv`: Datasets utilizados en el análisis.
* `portada.jpg`: Imagen utilizada como portada del html del proyecto.
* `ODS.xlsx`: Hoja de excel con los objetivos de desarrollo sostenible visibles en la fase de introducción del proyecto.
* `DashboardProyectoPersonal.Rmd`: Código en bruto sobre el desarrollo del cuadro.

---

## ✅ Dependencias

* **IDE**: `RStudio`
* **Librerías utilizadas**: `DT`, `googlesheets4`, `kableExtra`, `flexdashboard`, `highcharter`, `fpp3`, `openxlsx`, `leaflet`, `geojsonio`, `plotly`, `ggplot2`, `gganimate`, `tidyverse`, `eurostat`, `knitr`
* **Otros documentos**: `utilidades.R`
