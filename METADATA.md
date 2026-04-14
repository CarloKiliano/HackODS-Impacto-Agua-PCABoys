# 📖 Diccionario de Datos y Metadatos: Proyecto PCABoys
**HackODS 2026 - Instituto de Geofísica, UNAM**

Este documento detalla el origen, la vigencia y la estructura de los conjuntos de datos utilizados para el análisis del impacto socioeconómico de la contaminación hídrica en México. La transparencia en los datos es el pilar de nuestra investigación para los ODS 1, 3 y 6.

---

## 🌊 1. Calidad del Agua en México (CONAGUA)
Este dataset contiene los indicadores fisicoquímicos y microbiológicos de los cuerpos de agua superficiales monitoreados a nivel nacional.

* **Fuente:** [CONAGUA - Red Nacional de Medición de Calidad del Agua (RENAMECA)](https://www.gob.mx/conagua/articulos/resultados-de-la-red-nacional-de-medicion-de-calidad-del-agua-renameca?idiom=es)
* **Fecha de descarga:** 02 de abril de 2026
* **Licencia:** [Datos Abiertos de México](https://datos.gob.mx/libreusomx)
* **Archivo:** `CONAGUA_Limpio.csv`

| Variable | Descripción |
| :--- | :--- |
| `CLAVE SITIO` | Identificador único del punto de monitoreo. |
| `FECHA REALIZACIÓN` | Fecha en la que se tomó la muestra de agua. |
| `Año` | Año de registro de la muestra. |
| `COLI_FEC` | Concentración de Coliformes fecales (NMP/100 mL). |
| `COLI_TOT` | Concentración de Coliformes totales (NMP/100 mL). |
| `E_COLI` | Presencia de Escherichia coli (NMP/100 mL). |
| `ENTEROC_FEC` | Concentración de Enterococos fecales (NMP/100 mL). |
| `DBO_TOT` | Demanda Bioquímica de Oxígeno (mg/L). |
| `DQO_TOT` | Demanda Química de Oxígeno (mg/L). |
| `SST` | Sólidos Suspendidos Totales (mg/L). |
| `TURBIEDAD` | Grado de transparencia del agua (UNT). |
| `AS_TOT` | Concentración de Arsénico Total (mg/L). |
| `PB_TOT` | Concentración de Plomo Total (mg/L). |
| `HG_TOT` | Concentración de Mercurio Total (mg/L). |
| `CD_TOT` | Concentración de Cadmio Total (mg/L). |
| `NOMBRE DEL SITIO` | Nombre geográfico del cuerpo de agua monitoreado. |
| `ESTADO` | Entidad federativa. |
| `MUNICIPIO` | Municipio donde se ubica el sitio. |
| `LATITUD` | Coordenada geográfica (Y). |
| `LONGITUD` | Coordenada geográfica (X). |
| `TIPO DE CUERPO DE AGUA` | Clasificación (Río, Presa, Lago, etc.). |

---

## 📉 2. Pobreza y Carencias Sociales (CONEVAL)
Dataset enfocado en los índices de pobreza y la falta de acceso a servicios básicos y de salud a nivel municipal.

* **Fuente:** [CONEVAL - Medición Multidimensional de la Pobreza](https://www.datos.gob.mx/dataset/pobreza_mexico)
* **Fecha de descarga:** 04 de abril de 2026
* **Licencia:** [Datos Abiertos de México](https://datos.gob.mx/libreusomx)
* **Archivo:** `pobreza_analisis_agua_limpio.csv`

| Variable | Descripción |
| :--- | :--- |
| `CVE_ESTADO` | Clave de la entidad federativa. |
| `NOM_ESTADO` | Nombre de la entidad federativa. |
| `MUN` | Clave del municipio. |
| `NOM_MUN` | Nombre del municipio. |
| `AMBITO` | Clasificación de la zona (Urbano / Rural). |
| `POB_TOTAL` | Población total en el municipio. |
| `PCT_POBREZA` | Porcentaje de la población en situación de pobreza. |
| `PCT_Carencia_Servicios_Basicos_Vivienda` | Porcentaje de población con carencia de agua, drenaje o electricidad. |
| `PCT_Carencia_Calidad_Espacio_Vivienda` | Porcentaje de población con materiales precarios en el hogar. |
| `PCT_Carencia_Servicios_Salud` | Porcentaje de población sin acceso a servicios médicos. |

---

## 🏠 3. Infraestructura y Vivienda (INEGI ITER)
Datos censales detallados sobre la disponibilidad de agua y drenaje en las viviendas mexicanas.

* **Fuente:** [INEGI - Censo de Población y Vivienda (Principales resultados por localidad ITER)](https://www.inegi.org.mx/datosabiertos/)
* **Fecha de descarga:** 01 de abril de 2026
* **Licencia:** [Términos de Libre Uso del INEGI](https://www.inegi.org.mx/inegi/terminos.html)
* **Archivo:** `iter_analisis_agua_limpio.csv`

| Variable | Descripción |
| :--- | :--- |
| `NOM_ESTADO` | Nombre del estado. |
| `MUN` | Clave del municipio. |
| `NOM_MUN` | Nombre del municipio. |
| `LOC` | Clave de la localidad. |
| `NOM_LOC` | Nombre de la localidad. |
| `POBTOT` | Población total de la localidad. |
| `VPH_AGUADV` | Viviendas particulares que disponen de agua de red pública. |
| `VPH_AEASP` | Viviendas con agua entubada dentro de la vivienda. |
| `VPH_AGUAFV` | Viviendas con agua entubada fuera de la vivienda pero dentro del lote. |
| `VPH_DRENAJ` | Viviendas que disponen de drenaje. |
| `VPH_NODREN` | Viviendas que NO disponen de drenaje. |
| `VPH_TINACO` | Viviendas que disponen de tinaco. |
| `VPH_CISTER` | Viviendas que disponen de cisterna o aljibe. |
| `VPH_EXCSA` | Viviendas que disponen de sanitario exclusivo. |
| `VPH_LETR` | Viviendas que utilizan letrina o pozo ciego. |
| `VPH_C_SERV` | Viviendas con disposición de todos los servicios básicos. |
| `VPH_NDEAED` |  |

---

## 🏥 4. Morbilidad y Enfermedades Gastrointestinales (SSA)
Registro de la incidencia de enfermedades vinculadas a patógenos hídricos distribuido por grupos de edad.

* **Fuente:** [Secretaría de Salud - Anuarios de Morbilidad](https://www.gob.mx/salud/documentos/datos-abiertos-152127)
* **Fecha de descarga:** 03 de abril de 2026
* **Licencia:** [Datos Abiertos de México](https://datos.gob.mx/libreusomx)
* **Archivo:** `enfermedades_gi_filtrado.csv`

| Variable | Descripción |
| :--- | :--- |
| `CVE_ESTADO` | Clave del estado. |
| `NOM_ESTADO` | Nombre del estado. |
| `CVE_DIAGNO` | Clave del diagnóstico médico. |
| `DES_DIAGNO` | Nombre de la enfermedad (e.g., Tifoidea, Giardiasis). |
| `CVE_CIE10` | Clasificación Internacional de Enfermedades (OMS). |
| `ACUMULADO` | Total de casos registrados en el periodo. |
| `MENORES_1` | Casos registrados en menores de 1 año. |
| `DE01_A_04` | Casos registrados en el rango de 1 a 4 años. |
| `DE05_A_09` | Casos registrados en el rango de 5 a 9 años. |
| `DE10_A_14` | Casos registrados en el rango de 10 a 14 años. |
| `DE15_A_19` | Casos registrados en el rango de 15 a 19 años. |
| `DE20_A_24` | Casos registrados en el rango de 20 a 24 años. |
| `DE25_A_44` | Casos registrados en el rango de 25 a 44 años. |
| `DE45_A_49` | Casos registrados en el rango de 45 a 49 años. |
| `DE50_A_59` | Casos registrados en el rango de 50 a 59 años. |
| `DE60_A_64` | Casos registrados en el rango de 60 a 64 años. |
| `DE65_Y_MAS` | Casos registrados en personas de 65 años o más. |
| `SSA` | Casos atendidos en centros de la Secretaría de Salud. |
| `IMSS_ORD` | Casos atendidos en el IMSS (Régimen Ordinario). |
| `ISSSTE` | Casos atendidos en el ISSSTE. |
| `PEMEX` | Casos atendidos en servicios de PEMEX. |
| `SEDENA` | Casos atendidos en servicios de la Secretaría de la Defensa Nacional. |
| `ENERO` - `DICIEMBRE` | Distribución mensual del número de casos. |
| `PERIODO` | Año de reporte de los datos médicos. |

---
*Documentación generada por el equipo PCABoys para asegurar la reproducibilidad del análisis.*