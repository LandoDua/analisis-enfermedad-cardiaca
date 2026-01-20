# Data Schema: Heart Disease Dataset

Este esquema define las variables para procesamiento por IA. Cada entrada incluye el nombre exacto de la columna en el DataFrame, su significado clínico y su espacio de estados.

---

### Descripción de Atributos

- **COLUMN: city**
  - Type: Categorical (Nominal)
  - Domain: `['Cleveland', 'Budapest', 'Long Beach']`
  - Description: Geographic location of the data collection site.

- **COLUMN: ID_patient**
  - Type: Numerical (ID)
  - Description: Unique patient identifier within each geographic region. Should be excluded from predictive modeling.

- **COLUMN: age**
  - Type: Numerical (Integer)
  - Unit: Years
  - Description: Age of the patient.

- **COLUMN: sex**
  - Type: Categorical (Binary)
  - Domain: `['female', 'male']`
  - Description: Biological sex of the patient.

- **COLUMN: chest_pain_type**
  - Type: Categorical (Ordinal)
  - Mapping: `{1: typical_angina, 2: atypical_angina, 3: non_anginal_pain, 4: asymptomatic}`
  - Description: Heart-related chest pain classification.

- **COLUMN: resting_blood_pressure**
  - Type: Numerical (Integer)
  - Unit: mmHg
  - Description: Resting systolic blood pressure upon hospital admission.

- **COLUMN: serum_cholestoral**
  - Type: Numerical (Integer)
  - Unit: mg/dl
  - Description: Serum cholestoral level.

- **COLUMN: fasting_blood_sugar**
  - Type: Boolean (Binary)
  - Mapping: `{1: > 120 mg/dl, 0: <= 120 mg/dl}`
  - Description: Fasting blood sugar level relative to the 120 mg/dl threshold.

- **COLUMN: resting_EEG**
  - Type: Categorical (Nominal)
  - Mapping: `{0: normal, 1: ST-T_wave_abnormality, 2: left_ventricular_hypertrophy}`
  - Description: Electrocardiographic results at rest.

- **COLUMN: maximum_heart_rate**
  - Type: Numerical (Integer)
  - Unit: bpm
  - Description: Highest heart rate achieved during exercise stress test.

- **COLUMN: exercise_induced_angina**
  - Type: Boolean (Binary)
  - Mapping: `{1: yes, 0: no}`
  - Description: Presence of chest pain induced by physical exertion.

- **COLUMN: ST_depression**
  - Type: Numerical (Float)
  - Unit: mm
  - Description: ST segment depression induced by exercise relative to rest (Oldpeak). Indicator of myocardial ischemia.

- **COLUMN: slope_ST**
  - Type: Categorical (Ordinal)
  - Mapping: `{1: upsloping, 2: flat, 3: downsloping}`
  - Description: Slope of the peak exercise ST segment.

- **COLUMN: number_major_vessels**
  - Type: Numerical (Ordinal)
  - Domain: `[0, 1, 2, 3]`
  - Description: Number of major vessels colored by fluoroscopy.

- **COLUMN: thal**
  - Type: Categorical (Nominal)
  - Mapping: `{3: normal, 6: fixed_defect, 7: reversible_defect}`
  - Description: Thallium stress test results.

---

### Variable Objetivo (Target)

- **COLUMN: diagnosis_heart_disease**
  - Type: Categorical (Binary/Multiclass)
  - Mapping: `{0: < 50% narrowing (healthy), 1: > 50% narrowing (disease)}`
  - Note: Values 2, 3, and 4 in original sources indicate increasing severity of vessel narrowing.
