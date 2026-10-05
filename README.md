# Telecom-analysis
Análisis de una empresa de Telecomunicaciones  para identificar patrones de uso, detectar comportamientos atípicos y comprender qué segmentos de clientes muestran necesidades diferenciadas, con el fin de optimizar la oferta comercial y mejorar la experiencia del usuario.
# 📊 Proyecto 6: Análisis del Comportamiento de Clientes — ConnectaTel

## 📝 Descripción del Proyecto
Este proyecto analiza el comportamiento de uso real de los servicios móviles (llamadas y mensajes) de los clientes de **ConnectaTel**, una empresa de telecomunicaciones con presencia en México y Colombia. 

El objetivo principal es identificar patrones de consumo por segmentos demográficos (edad, ciudad, tipo de plan), detectar comportamientos atípicos u outliers, y generar hallazgos estratégicos que permitan optimizar la oferta comercial y mejorar la retención de usuarios.

---

## 🎯 Preguntas del Negocio
- ¿Qué segmentos de clientes muestran un mayor o menor volumen de uso en llamadas y mensajes?
- ¿Qué usuarios presentan valores atípicos (*outliers*) que sugieran un uso inusual o un posible error de registro?
- ¿Cómo varía el comportamiento de consumo según la edad y el plan contratado (*Básico* vs. *Premium*)?
- ¿Qué recomendaciones comerciales orientadas al diseño de planes y la experiencia del usuario se extraen de los datos?

---

## 🛠️ Herramientas y Librerías
- **Entorno de desarrollo:** Jupyter Notebook / JupyterLab
- **Lenguaje:** Python 3.x
- **Librerías principales:**
  - `pandas`: Manejo, limpieza e integración de datos.
  - `numpy`: Operaciones numéricas y vectoriales.
  - `matplotlib` & `seaborn`: Visualización de datos, histogramas y diagramas de caja (*boxplots*).

---

## 🗂️ Datasets Utilizados
El análisis se fundamenta en tres fuentes de datos complementarias:

1. **`plans.csv`**: Catálogo de planes ofrecidos por la empresa (precios mensuales, cuotas de minutos/GB/mensajes e importes por exceso de consumo).
2. **`users_latam.csv`**: Información demográfica y contractual de los clientes (`user_id`, edad, ciudad, fecha de registro, plan actual y fecha de cancelación/churn).
3. **`usage.csv`**: Registro detallado de la actividad de los usuarios (tipo de servicio: llamada o mensaje, duración en minutos y longitud en caracteres).

---

## 🔄 Flujo de Trabajo (Plan de Acción)

| Paso | Fase | Descripción / Acción |
| :--- | :--- | :--- |
| **1** | **Carga y Exploración** | Inspección inicial con `.head()`, `.shape` e `.info()` para comprender la estructura y tipos de variables. |
| **2** | **Calidad de Datos** | Conteo e identificación de valores nulos (`.isna()`), datos faltantes y detección de *sentinels* (ej. `?`, `-999`). |
| **3** | **Limpieza y Formato** | Estandarización de fechas a tipo `datetime`, imputación/marcado de inconsistencias e ignorado razonado de nulos esperados. |
| **4** | **Estadística Descriptiva** | Cálculo de métricas clave (media, mediana, desviación estándar, percentiles) para variables numéricas e intervalos. |
| **5** | **Análisis Visual y Outliers** | Identificación de sesgos y datos atípicos utilizando el rango intercuartílico (**IQR**) apoyado en histogramas y *boxplots*. |
| **6** | **Segmentación de Usuarios** | Creación de grupos demográficos (por rangos de edad, país y plan) y análisis de sus proporciones mediante `countplots`. |
| **7** | **Insights Ejecutivos** | Síntesis de conclusiones clave y propuestas de valor orientadas al diseño de mejores ofertas y retención de clientes. |

---

## 🚀 Cómo Reproducir este Proyecto

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/tu_usuario/connectatel-analysis.git](https://github.com/tu_usuario/connectatel-analysis.git)
   cd connectatel-analysis
