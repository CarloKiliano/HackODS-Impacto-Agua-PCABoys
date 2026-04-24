# 💧 Más que Agua: El Ciclo de la Inacción en México
### Proyecto del equipo **PCABoys** para el HackODS UNAM 2026

> *"Limpiar el agua cuesta menos que seguir pagando hospitales: la inacción es más cara."*

---

## 🌟 La visión del proyecto

Este análisis usa ciencia de datos para demostrar cómo la mala calidad del agua en México (**ODS 6**) detona crisis sanitarias (**ODS 3**) que golpean desproporcionadamente a las comunidades más vulnerables, perpetuando el ciclo de la pobreza (**ODS 1**).

El hallazgo central es territorial: existen **2,009 "Zonas Cero"** —sitios monitoreados donde se combina pobreza estatal ≥40% con contaminación fecal ≥200 NMP/100mL (umbral OMS de contacto humano)— distribuidas en 23 estados del país. En los cinco estados con mayor concentración de estas zonas, el **44% de los casos de enfermedades gastrointestinales son de niños menores de 14 años**, cuando ese grupo representa solo el 25.6% de la población.

La infancia carga **1.7 veces más enfermedad de la que le correspondería demográficamente**.

---

## 📊 Narrativa de datos: del mapa a la acción

### 1. El Problema — Mapa interactivo de Zonas Cero
La narrativa comienza con la visualización geográfica de los cuerpos de agua monitoreados por CONAGUA. El usuario puede filtrar por región (Nacional / Norte / Centro / Sur) y ver cómo se clasifica cada punto según la combinación de contaminación fecal y pobreza estatal. Cada sitio muestra su carga bacteriológica, el porcentaje de pobreza del estado, y la severidad del exceso sobre el límite OMS.

### 2. Las Consecuencias — Dos vistas de la desigualdad

**a) Ranking estatal.** Oaxaca encabeza la lista con **13.86% de viviendas sin drenaje doméstico**, frente al 0.14% de la Ciudad de México. La brecha entre extremos es de **99 veces** — misma nación, dos realidades sanitarias.

**b) El impuesto a la infancia.** En los cinco estados con más Zonas Cero (Veracruz, Jalisco, Michoacán, Sinaloa, Chiapas), la proporción de casos pediátricos duplica el peso demográfico real de la infancia. El costo de la inacción no se mide solo en pesos: se mide en salud y desarrollo infantil perdidos.

### 3. La Solución — Reasignación inteligente de PROAGUA
No proponemos crear nuevos programas, sino dotar de inteligencia territorial al ya existente **Programa de Agua Potable, Drenaje y Saneamiento (PROAGUA)**. Construimos un **Índice de Urgencia** que cruza tres variables observables del Censo INEGI 2020:

- Porcentaje de viviendas sin drenaje doméstico,
- Cantidad absoluta de viviendas afectadas (en escala logarítmica),
- Peso demográfico infantil del municipio.

El resultado: **20 municipios prioritarios** donde cada peso reasignado rinde el mayor retorno social. El primero es Tehuipango, Veracruz, con 80.65% de viviendas sin drenaje.

---

## 📈 Impacto económico documentado

| Concepto | Retorno | Fuente |
| :--- | :--- | :--- |
| Retorno social por $1 invertido en agua y saneamiento | $4.30 | WHO/UNICEF Joint Monitoring Programme |
| Rango en regiones en desarrollo | $5 – $28 USD | UN-Water GLAAS |

Aplicar esta reasignación presupuestaria en los municipios identificados rompería el ciclo que hoy se sostiene: familias sin drenaje → niños enfermos → gasto hospitalario reactivo → nueva temporada de enfermedades.

**No es crisis de recursos. Es crisis de prioridades.**

---

## 🛠️ Estructura técnica

- **Framework:** Quarto Dashboard (formato `dashboard`)
- **Lenguaje:** Python 3.12
- **Gestión de dependencias:** `uv`
- **Visualización:** Plotly Express + Matplotlib
- **Tipografía:** IBM Plex Serif / IBM Plex Sans
- **Fuentes de datos:** SSA (Morbilidad 2017), INEGI (Censo 2020, ITER), CONEVAL (Pobreza 2020), CONAGUA (RENAMECA)

### Reproducir el dashboard localmente

```bash
git clone https://github.com/[org]/PCABoys-Impacto-Agua-HackODS
cd PCABoys-Impacto-Agua-HackODS
uv sync
cd dashboard
uv run quarto render index.qmd
```

El resultado queda en `docs/index.html`.

---

## 📜 Licencia

Este proyecto se distribuye bajo licencia **Creative Commons Atribución-CompartirIgual 4.0 Internacional** (CC BY-SA 4.0). Los datos fuente mantienen sus licencias originales.

---

## 👤 Equipo PCABoys

- **Carlo Kiliano Ferrera Guadarrama**
- **José Julián Pérez Bustamante**
- **Aldo Sebastián Altamirano Vázquez**

UNAM · Instituto de Investigaciones en Matemáticas Aplicadas y en Sistemas (IIMAS)

---

## 📚 Referencias

1. INEGI — *Censo de Población y Vivienda 2020* — Cuestionario Básico (ITER).
2. CONEVAL — *Medición Multidimensional de la Pobreza 2020*.
3. CONAGUA — *Red Nacional de Medición de Calidad del Agua (RENAMECA)*.
4. Secretaría de Salud (México) — *Anuario de Morbilidad 2017*.
5. WHO/UNICEF — *Joint Monitoring Programme for Water Supply, Sanitation and Hygiene* (JMP).
6. UN-Water — *Informe GLAAS 2014: Inversión en agua y saneamiento*.
7. Organización Mundial de la Salud — *Guidelines for safe recreational water environments*, umbral ≥200 NMP/100mL de coliformes fecales.
