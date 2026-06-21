<div align="center">

<h1>🏠 HomePricePredictor</h1>
<h3>Predicción de Precios de Vivienda con Machine Learning</h3>

<p>
  <img src="https://img.shields.io/badge/Estado-En%20Desarrollo-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Python-3.11-yellow?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/Metodología-Scrum%20%2F%20Ágil-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Gestión-Trello-0052CC?style=for-the-badge&logo=trello" />
</p>

<p><em>Proyecto Integrador Final 
Instituto Nuevos Aires · Tecnicatura Superior en Ciencia de Datos e Inteligencia Artificial</p>

</div>

---

## 📌 Descripción del Proyecto

**HomePricePredictor** es un proyecto simulado de ciencia de datos que busca predecir el precio de venta de viviendas a partir de variables estructurales y contextuales (superficie, cantidad de habitaciones, ubicación, antigüedad, entre otras).

El proyecto reproduce el flujo de trabajo real de un equipo de datos: desde la definición del problema y la limpieza del dataset, hasta el entrenamiento de modelos predictivos y la presentación de resultados a stakeholders no técnicos.

> **Problema central:** ¿Es posible estimar el precio de una vivienda con precisión aceptable, utilizando únicamente sus características físicas y de ubicación?

---

## 🎯 Objetivos

| # | Objetivo |
|---|----------|
| 1 | Construir un modelo de regresión supervisada para predecir precios de inmuebles |
| 2 | Realizar un análisis exploratorio de datos (EDA) para identificar patrones relevantes |
| 3 | Evaluar el modelo con métricas estándar (RMSE, MAE, R²) |
| 4 | Documentar el proceso de manera profesional y reproducible |
| 5 | Aplicar buenas prácticas de ética en el uso de datos |

---

## 🏗️ Estructura del Repositorio

```
HomePricePredictor/
│
├── 📁 data/
│   ├── raw/                  # Datos crudos sin modificar
│   └── processed/            # Datos limpios y transformados
│
├── 📁 notebooks/
│   ├── 01_EDA.ipynb          # Análisis Exploratorio de Datos
│   ├── 02_preprocessing.ipynb # Limpieza y transformación
│   └── 03_modeling.ipynb     # Entrenamiento y evaluación de modelos
│
├── 📁 src/
│   ├── data_processing.py    # Scripts de preprocesamiento
│   └── model.py              # Definición y entrenamiento del modelo
│
├── 📁 reports/
│   ├── informe_etica.md      # Informe de consideraciones éticas
│   └── resultados_sprint.md  # Resumen de avances por sprint
│
├── 📁 docs/
│   └── presentacion_final.pdf
│
├── .gitignore
├── requirements.txt
└── README.md
```

---

## 👤 Rol Simulado

Este proyecto es de modalidad **individual**. En un contexto profesional real, los roles del equipo serían:

| Rol | Responsabilidad |
|-----|----------------|
| **Líder de Proyecto / Scrum Master** | Coordina el sprint, gestiona el backlog en Trello |
| **Data Engineer** | Obtiene, limpia y transforma los datos |
| **Data Scientist** | Construye y valida los modelos predictivos |
| **Data Analyst** | Genera visualizaciones y comunica resultados |
| **Documentador / QA** | Asegura la calidad y documenta el proceso |

---

## 🔄 Metodología Ágil

El proyecto se organizó mediante **Scrum** con ciclos de trabajo semanales (sprints):

```
Sprint 1 — Semana 1
  ✅ Definición del problema
  ✅ Investigación del dataset
  ✅ Configuración del repositorio

Sprint 2 — Semana 2
  ✅ Análisis Exploratorio de Datos (EDA)
  ✅ Limpieza y preprocesamiento
  ✅ Selección de variables

Sprint 3 — Semana 3
  ✅ Entrenamiento del modelo base (Regresión Lineal)
  ✅ Pruebas con modelos avanzados (Random Forest)
  ✅ Evaluación y comparación de métricas

Sprint 4 — Semana 4
  ✅ Documentación final
  ✅ Elaboración del informe ético
  ✅ Preparación de la presentación
```

📋 **Tablero Trello:** [Ver tablero](https://trello.com/b/d1xdMuMV/homepricepredictor)

---

## 🛠️ Tecnologías y Herramientas

<table>
<tr>
  <th>Categoría</th>
  <th>Herramienta</th>
  <th>Uso</th>
</tr>
<tr>
  <td>Lenguaje</td>
  <td>Python 3.11</td>
  <td>Procesamiento, modelado y visualización</td>
</tr>
<tr>
  <td>Análisis de datos</td>
  <td>Pandas, NumPy</td>
  <td>Manipulación y transformación del dataset</td>
</tr>
<tr>
  <td>Visualización</td>
  <td>Matplotlib, Seaborn</td>
  <td>Gráficos del EDA y resultados</td>
</tr>
<tr>
  <td>Machine Learning</td>
  <td>Scikit-learn</td>
  <td>Modelos de regresión y evaluación</td>
</tr>
<tr>
  <td>Gestión del proyecto</td>
  <td>Trello</td>
  <td>Tablero Kanban y seguimiento de tareas</td>
</tr>
<tr>
  <td>Control de versiones</td>
  <td>Git / GitHub</td>
  <td>Repositorio y documentación colaborativa</td>
</tr>
<tr>
  <td>Entorno</td>
  <td>Jupyter Notebook</td>
  <td>Desarrollo iterativo y documentación en código</td>
</tr>
</table>

---

## 📊 Métricas de Éxito

El modelo se considera exitoso si alcanza:

- **R² ≥ 0.80** — el modelo explica al menos el 80% de la varianza en los precios
- **RMSE** — error cuadrático medio dentro de rangos aceptables para el mercado analizado
- **MAE** — error absoluto medio que permita una estimación útil para el usuario final

---

## ⚙️ Cómo Ejecutar el Proyecto

```bash
# 1. Clonar el repositorio
git clone https://github.com/lucasmatias-sanz/HomePricePredictor.git
cd HomePricePredictor

# 2. Instalar dependencias
pip install -r requirements.txt

# 3. Ejecutar los notebooks en orden
jupyter notebook notebooks/01_EDA.ipynb
```

---

## 📄 Licencia

Este proyecto fue desarrollado con fines académicos en el marco de la materia **Aproximación al Campo Laboral** del **Instituto Nuevos Aires**.

---

<div align="center">

**Lucas Matias Sanz**<br/>
Tecnicatura Superior en Ciencia de Datos e Inteligencia Artificial<br/>
Instituto Nuevos Aires · 2026

</div>
