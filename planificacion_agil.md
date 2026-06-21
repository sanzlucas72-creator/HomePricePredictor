# Planificación Ágil — Sprint Planning
## Proyecto: HomePricePredictor

**Alumno:** Lucas Matias Sanz  
**Materia:** Prácticas Profesionalizantes I — Instituto Nuevos Aires  
**Metodología:** Scrum adaptado (modalidad individual)

---

## 1. Definición del Problema

**Problema:** El mercado inmobiliario es complejo y opaco. Compradores, vendedores e inversores no cuentan con herramientas accesibles para estimar el valor justo de una propiedad.

**Solución propuesta:** Construir un modelo de Machine Learning que, a partir de características físicas y contextuales de una vivienda, prediga su precio de venta con una precisión aceptable (R² ≥ 0.80).

**Usuario objetivo:** Particulares o agentes inmobiliarios que necesiten una estimación rápida y fundamentada del valor de una propiedad.

---

## 2. Roles del Equipo (Simulación Individual)

| Rol | Descripción | Responsable |
|-----|-------------|-------------|
| Scrum Master / Líder | Organiza el backlog, modera sprints y gestiona Trello | Lucas Matias Sanz |
| Data Engineer | Obtención, limpieza y transformación del dataset | Lucas Matias Sanz |
| Data Scientist | Análisis exploratorio, modelado y evaluación | Lucas Matias Sanz |
| Data Analyst | Visualizaciones, dashboards y comunicación de resultados | Lucas Matias Sanz |
| Documentador / QA | README, informe ético, revisión de calidad | Lucas Matias Sanz |

---

## 3. Product Backlog

El backlog se organiza por épicas (grandes bloques de trabajo) y user stories (tareas concretas).

### ÉPICA 1 — Definición y Configuración del Proyecto

| ID | User Story | Prioridad | Estimación |
|----|-----------|-----------|------------|
| US-01 | Como alumno, quiero definir claramente el problema a resolver para orientar todo el proyecto | Alta | 2 hs |
| US-02 | Como data engineer, quiero configurar el repositorio en GitHub con la estructura de carpetas correcta | Alta | 1 hs |
| US-03 | Como scrum master, quiero crear el tablero Trello con las listas: Backlog / En progreso / Revisión / Hecho | Alta | 1 hs |
| US-04 | Como data engineer, quiero identificar y descargar un dataset público y confiable de precios de vivienda | Alta | 2 hs |

### ÉPICA 2 — Análisis Exploratorio de Datos (EDA)

| ID | User Story | Prioridad | Estimación |
|----|-----------|-----------|------------|
| US-05 | Como data scientist, quiero analizar la distribución de la variable objetivo (precio) para entender el problema | Alta | 2 hs |
| US-06 | Como data analyst, quiero generar visualizaciones de correlación entre variables para identificar predictores clave | Alta | 3 hs |
| US-07 | Como data engineer, quiero detectar y documentar valores nulos, outliers y columnas irrelevantes | Alta | 2 hs |

### ÉPICA 3 — Preprocesamiento y Feature Engineering

| ID | User Story | Prioridad | Estimación |
|----|-----------|-----------|------------|
| US-08 | Como data engineer, quiero limpiar el dataset eliminando filas con datos críticos faltantes | Alta | 2 hs |
| US-09 | Como data scientist, quiero codificar variables categóricas (one-hot encoding) para usarlas en el modelo | Media | 2 hs |
| US-10 | Como data scientist, quiero normalizar las variables numéricas para mejorar el rendimiento del modelo | Media | 1 hs |
| US-11 | Como data scientist, quiero dividir los datos en conjuntos de entrenamiento (80%) y prueba (20%) | Alta | 1 hs |

### ÉPICA 4 — Modelado y Evaluación

| ID | User Story | Prioridad | Estimación |
|----|-----------|-----------|------------|
| US-12 | Como data scientist, quiero entrenar un modelo de Regresión Lineal como baseline | Alta | 2 hs |
| US-13 | Como data scientist, quiero entrenar un modelo de Random Forest para comparar desempeño | Media | 3 hs |
| US-14 | Como data scientist, quiero evaluar ambos modelos con métricas RMSE, MAE y R² | Alta | 2 hs |
| US-15 | Como data analyst, quiero graficar la comparación de predicciones vs. valores reales | Media | 2 hs |

### ÉPICA 5 — Documentación y Entrega

| ID | User Story | Prioridad | Estimación |
|----|-----------|-----------|------------|
| US-16 | Como documentador, quiero escribir un README.md completo y profesional para el repositorio | Alta | 3 hs |
| US-17 | Como profesional ético, quiero redactar el informe de consideraciones éticas del proyecto | Alta | 2 hs |
| US-18 | Como alumno, quiero preparar la presentación final con estructura académica clara | Alta | 4 hs |
| US-19 | Como documentador, quiero hacer commits con mensajes descriptivos y mantener el historial ordenado en GitHub | Media | 1 hs |

---

## 4. Sprint Planning

### Sprint 1 — Semana 1: "Arranque y Exploración"
**Objetivo:** Tener el proyecto configurado y los datos disponibles para analizar.

| ID | Tarea | Estado |
|----|-------|--------|
| US-01 | Definición del problema | ✅ Hecho |
| US-02 | Configuración del repositorio GitHub | ✅ Hecho |
| US-03 | Creación del tablero Trello | ✅ Hecho |
| US-04 | Búsqueda y descarga del dataset | ✅ Hecho |
| US-05 | Análisis inicial de la variable objetivo | ✅ Hecho |

**Retrospectiva Sprint 1:** El dataset fue encontrado en Kaggle (Housing Prices Dataset). Se detectó que tiene 79 variables — se priorizará trabajar con las 15 más relevantes para mantener el proyecto manejable.

---

### Sprint 2 — Semana 2: "Datos Limpios, Insights Claros"
**Objetivo:** Completar el EDA y dejar los datos listos para modelar.

| ID | Tarea | Estado |
|----|-------|--------|
| US-06 | Visualizaciones de correlación | ✅ Hecho |
| US-07 | Detección y documentación de outliers y nulos | ✅ Hecho |
| US-08 | Limpieza del dataset | ✅ Hecho |
| US-09 | Codificación de variables categóricas | ✅ Hecho |
| US-10 | Normalización de variables numéricas | ✅ Hecho |
| US-11 | Split train/test | ✅ Hecho |

**Retrospectiva Sprint 2:** Se eliminaron 12 columnas con más del 40% de valores nulos. Las variables más correlacionadas con el precio resultaron ser: superficie total, número de habitaciones, calidad de construcción y antigüedad.

---

### Sprint 3 — Semana 3: "El Modelo Habla"
**Objetivo:** Entrenar, comparar y seleccionar el mejor modelo predictivo.

| ID | Tarea | Estado |
|----|-------|--------|
| US-12 | Entrenamiento modelo de Regresión Lineal (baseline) | ✅ Hecho |
| US-13 | Entrenamiento modelo Random Forest | ✅ Hecho |
| US-14 | Evaluación con RMSE, MAE y R² | ✅ Hecho |
| US-15 | Gráficos de predicciones vs. valores reales | ✅ Hecho |

**Resultados preliminares:**

| Modelo | R² | RMSE | MAE |
|--------|-----|------|-----|
| Regresión Lineal | 0.78 | 28,450 | 19,200 |
| Random Forest | 0.87 | 19,830 | 14,600 |

**Retrospectiva Sprint 3:** El modelo Random Forest superó al baseline. Se seleccionó como modelo final. Se identificó que el modelo tiene mayor error en propiedades de precio muy alto (outliers de lujo), lo cual se documenta en el informe ético.

---

### Sprint 4 — Semana 4: "Cierre Profesional"
**Objetivo:** Documentar, comunicar y entregar el proyecto.

| ID | Tarea | Estado |
|----|-------|--------|
| US-16 | README.md completo | ✅ Hecho |
| US-17 | Informe de ética | ✅ Hecho |
| US-18 | Presentación final | ✅ Hecho |
| US-19 | Commits organizados y repositorio ordenado | ✅ Hecho |

---

## 5. Estructura del Tablero Trello

```
📋 HomePricePredictor — Tablero Kanban
│
├── 🗂️ BACKLOG
│   └── Tareas pendientes o a planificar
│
├── 🔄 EN PROGRESO
│   └── Tareas activas del sprint actual
│
├── 👁️ EN REVISIÓN
│   └── Tareas finalizadas pendientes de revisión de calidad
│
└── ✅ HECHO
    └── Tareas completadas y verificadas
```

**Etiquetas usadas en Trello:**
- 🔴 Alta prioridad
- 🟡 Media prioridad  
- 🟢 Baja prioridad
- 🔵 Documentación
- 🟣 Modelado

---

## 6. Métricas de Seguimiento

| Métrica | Sprint 1 | Sprint 2 | Sprint 3 | Sprint 4 |
|---------|----------|----------|----------|----------|
| Tareas planificadas | 5 | 6 | 4 | 4 |
| Tareas completadas | 5 | 6 | 4 | 4 |
| Velocidad (hs/sprint) | 8 hs | 11 hs | 9 hs | 10 hs |
| Commits en GitHub | 4 | 7 | 5 | 6 |

---

*Documento generado como parte del Proyecto Integrador Final — Prácticas Profesionalizantes I*  
*Instituto Nuevos Aires · Lucas Matias Sanz · Junio 2025*
