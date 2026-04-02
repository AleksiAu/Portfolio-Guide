# 📚 Aleksi's Portfolio Guide

Welcome to my data portfolio! Here I document my projects in energy data analytics and power systems.

## 🧑‍💻 About Me

I'm an MSc (Tech) in Electrical Engineering with a minor in Data Analytics, currently working as a Design Engineer at a distribution network company in Finland. My work focuses on building data-driven tools to support grid planning, investment prioritization, and load analysis. I'm experienced in processing large-scale smart meter data with Python and DuckDB, building geospatial visualizations, and applying statistical and ML methods to real energy system problems.

My Master's thesis developed a data-based methodology for long-term distribution and medium-voltage network development planning.

---

## 📂 Projects

### ⚡ 2D Grid Flow Desktop
**Code:** [grid-flow-desktop](https://github.com/AleksiAu/grid-flow-desktop)

| | |
|---|---|
| **Objective** | Build an interactive desktop tool for visualising and editing DC power flow in distribution and transmission networks |
| **Description** | PySide6 desktop application with IEC-inspired node symbols (generator, substation, consumer, connection point), live DC nodal B-θ solver, and optional PyPSA LPF engine. Supports drag-and-drop editing, separator toggling, connection-point capacity dispatch, and JSON save/load. Modular package architecture separates data model, solver, graphics, and UI layers. |
| **Key question** | *How do topology changes and load shifts propagate as power flows across the network?* |
| **Tools** | Python, PySide6, NumPy, Pandas, PyPSA (optional) |
| **Results** | Fully interactive editor with real-time power flow updates. Architecture refactored to use Qt signals instead of back-references, enabling clean separation between the graphics layer and application logic. |

---

### 🗺️ Spatial Grid Analysis
**Code:** [spatial-grid-analysis](https://github.com/AleksiAu/spatial-grid-analysis)

| | |
|---|---|
| **Objective** | Map electricity demand spatially to support network planning and investment prioritization |
| **Description** | Aggregated customer-level consumption data into a 1 km × 1 km grid, classified areas into profile types (urban, residential, industrial), visualized asset age, and built animated time-slider maps showing how consumption evolves |
| **Key question** | *Where is demand concentrated, how has it changed, and where are the oldest assets?* |
| **Tools** | Python, DuckDB, GeoPandas, Shapely, Folium, pyproj |
| **Results** | Identified industrial zones, dense urban demand, and low-load rural areas. Provided communicable basis for investment discussions with stakeholders |

---

### 🌡️ Load–Weather Analysis
**Code:** [load-weather-analysis](https://github.com/AleksiAu/load-weather-analysis)

| | |
|---|---|
| **Objective** | Quantify weather sensitivity and separate structural demand trends from temperature-driven variability |
| **Description** | Built regression models (P = a + b·T) for MV and LV customer groups, constructed temperature-corrected load time series using month×hour normal temperatures, analyzed seasonal daily profiles, and performed December cold-weather energy comparisons |
| **Key question** | *How sensitive is our load to temperature, and what are the real demand trends when we remove weather noise?* |
| **Tools** | Python, DuckDB, Pandas, Matplotlib, Seaborn, SciPy |
| **Key findings** | LV network shows ~1.5 MW/°C heating sensitivity. Temperature correction reduces year-to-year noise by ~30%. Winter daily profiles peak at 7–9 AM and 17–19 PM. Cold Decembers drive 25%+ higher demand. |

---

### 🤖 Load Forecasting with LSTM
**Code:** [load-forecasting-ml](https://github.com/AleksiAu/load-forecasting-ml)

| | |
|---|---|
| **Objective** | Predict hourly network load using deep learning with historical consumption and weather data |
| **Description** | End-to-end ML pipeline: DuckDB extracts 15+ behavioral features per customer in a single SQL query, LSTM neural network trained on 7-day lookback windows with cyclical time encodings and calendar features, evaluated against persistence baseline |
| **Key question** | *Can we forecast hourly load accurately enough to support operational planning?* |
| **Tools** | Python, TensorFlow/Keras, DuckDB, Plotly, Pandas |
| **Results** | LSTM outperforms persistence baseline across RMSE, MAE, and MAPE. Cold-weather subset analysis reveals where the model struggles most. |

---

### 🔌 Connection Sizing Analysis
**Code:** *(methodology documented in portfolio)*

| | |
|---|---|
| **Objective** | Assess how connection sizing aligns with actual usage across customer groups |
| **Description** | Linked connection capacity data with measured peak load, calculated utilization rates, and identified patterns of over- and under-sizing |
| **Key question** | *Are customer connections appropriately sized for their real demand?* |
| **Tools** | Python, Pandas, Matplotlib |
| **Key findings** | ~66% of connections use less than half their capacity. ~5% exceed nominal capacity. Results inform tariff discussions and planning assumptions. |

---



## 🛠️ Skills

| Category | Details |
|----------|---------|
| **Languages & querying** | Python (Pandas, NumPy, SciPy), SQL, DuckDB |
| **Visualization** | Matplotlib, Seaborn, Plotly, Power BI, Folium |
| **Geospatial** | GeoPandas, Shapely, Folium, pyproj |
| **Machine learning** | TensorFlow/Keras, scikit-learn |
| **Domain tools** | Trimble NIS & DMS, SCADA, PVSyst |
| **Power systems** | Load flow analysis, reliability indices (SAIDI/SAIFI/CAIDI), voltage drop studies, reactive power management |
| **Other** | Git, Excel, Jupyter, reproducible analysis pipelines |

---

## 📜 Education & Certifications

| | |
|---|---|
| **MSc (Tech)** | Electrical and Electronics Engineering — LUT University (2020–2025) |
| **Major** | Electrical Networks and Markets |
| **Minor** | Data Analytics |
| **Thesis** | Development Plan for Nivos Verkot Oy's Distribution and High-Voltage Network |
| **Exchange** | Ghent University, Belgium (2024) |

---

## 📫 Contact

If you'd like to discuss my work, potential roles, or collaboration — feel free to reach out!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/aleksiauramo) [![Email](https://img.shields.io/badge/EA4335?style=flat&logo=gmail&logoColor=white)](mailto:aleksi.auramo@gmail.com)
