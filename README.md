# ❤️ Análisis Exploratorio de Enfermedad Cardíaca  
### Unificación, limpieza y exploración de datos clínicos

## 📌 Descripción del proyecto

Este proyecto consiste en un **análisis exploratorio de datos (EDA)** aplicado a un conjunto de datos de **diagnóstico de enfermedad cardíaca**, el cual originalmente se encontraba dividido en **tres datasets distintos**, cada uno en **formatos diferentes**.

El objetivo principal del proyecto es:

- Importar, limpiar y unificar los datasets originales  
- Estandarizar y codificar las variables  
- Exportar un dataset final en formato **Parquet**  
- Realizar un análisis exploratorio para identificar patrones y tendencias  
- Obtener nociones iniciales sobre la relevancia de las variables mediante *Random Forest*

Este proyecto forma parte de mi formación como **estudiante de Ingeniería en Sistemas**, con interés en **Análisis de Datos y Ciencia de Datos**.

---

## 🗂️ Fuentes de datos

El dataset corresponde al clásico **Heart Disease Database**, proveniente de las siguientes instituciones médicas:

1. **Cleveland Clinic Foundation**  
   - Formato original: `.data / .csv`

2. **Hungarian Institute of Cardiology (Budapest)**  
   - Formato original: `.xlsx`

3. **V.A. Medical Center, Long Beach (CA)**  
   - Formato original: `.pdf`

El dataset original incluía **4 regiones y 76 variables**.  
Para este proyecto se trabajó con:

- 3 regiones  
- 14 variables clínicas relevantes  
- 797 registros en total  

---

## 🔄 Importación, limpieza y unificación de datos

Notebook principal: **`importar_datos2.ipynb`**

En esta etapa del proyecto se realizó:

- Importación de datos desde múltiples formatos (Excel, PDF y texto plano)  
- Renombrado y homologación de columnas  
- Reemplazo de valores `"?"` por valores nulos (`NaN`)  
- Verificación y corrección de tipos de datos  
- Conversión de variables categóricas  
- Unificación de los tres datasets en uno solo  
- Exportación del dataset final en formato **Parquet**

---

## 📊 Análisis Exploratorio de Datos

Notebook: **`visualizacion.ipynb`**

El análisis exploratorio incluye:

### 🔍 Descripción de variables
- Definición clínica y técnica de cada variable  
- Tipo de dato y codificación utilizada  

### 📈 Análisis univariado
- Distribuciones de variables como:
  - Edad  
  - Presión arterial  
  - Colesterol  
  - Frecuencia cardíaca máxima  

### 📉 Análisis multivariado
- Comparaciones por diagnóstico de enfermedad cardíaca  
- Visualizaciones segmentadas por sexo y región  
- Mapa de calor de correlaciones (variables numéricas y booleanas)

### 🌲 Random Forest (enfoque exploratorio)
- Uso de un `RandomForestClassifier`  
- Codificación de variables categóricas mediante `OneHotEncoder`  
- Análisis de importancia de variables  

> **Nota:** El dataset se encuentra desbalanceado. El modelo se utiliza únicamente con fines exploratorios para obtener nociones, no como modelo predictivo final.

---

## 🧠 Variables principales

Algunas de las variables incluidas en el análisis son:

- `age` — Edad del paciente  
- `sex` — Sexo  
- `chest_pain_type` — Tipo de dolor torácico  
- `resting_blood_pressure` — Presión arterial en reposo  
- `serum_cholestoral` — Colesterol sérico  
- `maximum_heart_rate` — Frecuencia cardíaca máxima  
- `ST_depression` — Depresión del segmento ST  
- `number_major_vessels` — Número de vasos principales  
- `thal` — Resultado de gammagrafía cardíaca  
- `diagnosis_heart_disease` — Variable objetivo  

---

## 🛠️ Tecnologías utilizadas

- Python 3  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- PyArrow  
- pdfplumber  

---

## 🚧 Estado del proyecto

🟡 **En desarrollo**

Posibles mejoras y extensiones futuras:

- Tratamiento avanzado de valores faltantes  
- Balanceo de clases  
- Feature engineering  
- Modelos predictivos  
- Validación cruzada  

---

## 👨‍💻 Autor

Estudiante de **Ingeniería en Sistemas**  
Intereses principales:

- Análisis de Datos  
- Ciencia de Datos  
- Machine Learning  

Este proyecto forma parte de mi portafolio académico y personal.

---

## ⭐ Comentarios finales

Este proyecto busca aplicar técnicas reales de limpieza, unificación y análisis exploratorio sobre datos clínicos reales, enfrentando problemas comunes como múltiples formatos de origen, valores faltantes y datasets desbalanceados.
