# Informe de Consideraciones Éticas
## Proyecto: HomePricePredictor — Predicción de Precios de Vivienda

**Alumno:** Lucas Matias Sanz  
**Materia:** Prácticas Profesionalizantes I  
**Institución:** Instituto Nuevos Aires  
**Fecha:** Junio 2025

---

## 1. Introducción

El desarrollo de modelos de Machine Learning conlleva responsabilidades que van más allá del desempeño técnico. En el proyecto **HomePricePredictor**, se trabajó con datos relacionados a características de viviendas y sus precios de mercado. Aunque aparentemente neutros, estos datos pueden contener sesgos estructurales que, si no se abordan con criterio ético, pueden generar predicciones injustas o discriminatorias.

Este informe analiza las principales implicancias éticas del proyecto, siguiendo los principios estudiados en la materia: **equidad, transparencia, privacidad y responsabilidad**.

---

## 2. Principios Éticos Aplicados

### 2.1 Equidad y No Discriminación

Uno de los riesgos más importantes en la predicción de precios inmobiliarios es la **perpetuación de sesgos históricos**. Los datos de precios de vivienda pueden reflejar décadas de discriminación estructural en el mercado inmobiliario: barrios históricamente devaluados por razones socioeconómicas o demográficas pueden generar predicciones que refuercen esas inequidades.

**Medidas adoptadas:**
- Se evitó incluir variables de ubicación geográfica de forma directa sin contextualización.
- Se revisó la distribución de errores del modelo por segmentos de precio para detectar si el modelo favorece ciertos rangos en detrimento de otros.
- Se reconoce que el modelo **no debe usarse como herramienta de tasación oficial** sin revisión humana experta.

### 2.2 Transparencia y Explicabilidad

Un modelo que no puede explicarse genera desconfianza y dificulta la detección de errores. En este proyecto se priorizó la **explicabilidad del modelo** por sobre la complejidad técnica.

**Medidas adoptadas:**
- Se optó por comenzar con un modelo de Regresión Lineal, cuyo razonamiento es fácilmente interpretable.
- Se utilizaron gráficos de importancia de variables (feature importance) para comunicar qué factores influyen más en la predicción.
- Los notebooks están documentados paso a paso, de modo que cualquier persona con conocimientos básicos pueda seguir el proceso.

### 2.3 Privacidad y Seguridad de los Datos

Los datos inmobiliarios pueden contener información sensible de personas físicas: dueños de propiedades, compradores, inquilinos. El uso irresponsable de estos datos puede violar la privacidad individual.

**Medidas adoptadas:**
- El dataset utilizado es de **fuente pública y anonimizada** (no contiene nombres, DNI ni datos de contacto).
- No se almacenaron datos sensibles en el repositorio público de GitHub.
- Se incluyó un `.gitignore` adecuado para evitar la publicación accidental de datos crudos.

### 2.4 Responsabilidad Profesional

Como futuro profesional en Ciencia de Datos, es fundamental asumir la responsabilidad sobre los outputs del modelo. Un error en la estimación de precio puede tener consecuencias reales sobre decisiones financieras de personas.

**Compromiso asumido:**
- El modelo se presenta como una **herramienta de apoyo a la decisión**, no como un oráculo infalible.
- Se documentan explícitamente las limitaciones del modelo: rango de datos en que fue entrenado, variables no consideradas (estado de la propiedad, tendencia del mercado, etc.).
- Se recomienda siempre complementar la predicción con la evaluación de un profesional del sector.

---

## 3. Limitaciones Éticas Identificadas

| Limitación | Descripción | Mitigación propuesta |
|------------|-------------|----------------------|
| Sesgo de datos históricos | El dataset puede reflejar desigualdades del mercado | Análisis crítico de distribución y residuos por segmento |
| Falta de contexto socioeconómico | El modelo no considera factores macroeconómicos | Documentar explícitamente las variables excluidas |
| Riesgo de sobreconfianza | Un R² alto puede generar uso irresponsable | Comunicar siempre el intervalo de confianza de la predicción |
| Datos desactualizados | El mercado inmobiliario varía con el tiempo | Establecer una frecuencia de re-entrenamiento del modelo |

---

## 4. Reflexión Personal

A lo largo del desarrollo de este proyecto, comprendí que la ética en la Ciencia de Datos no es una etapa final del proceso, sino una dimensión transversal que debe estar presente desde la elección del problema hasta la comunicación de los resultados.

Como técnico en formación, me comprometo a:
- Cuestionar siempre el origen y representatividad de los datos que utilizo.
- Documentar las decisiones técnicas con honestidad, incluyendo las limitaciones.
- Priorizar el impacto humano del modelo por encima de la métrica de desempeño.
- Comunicar con claridad a los stakeholders qué puede y qué no puede hacer el modelo.

---

## 5. Referencias

- Clases del curso "Aproximación al Campo Laboral" — MSc. Ángel Daniel Fuentes S.
- Principios de IA responsable — Clase 4: Actores Clave y Ética en la Era Digital.
- Jobin, A. et al. (2019). *The global landscape of AI ethics guidelines*. Nature Machine Intelligence.
