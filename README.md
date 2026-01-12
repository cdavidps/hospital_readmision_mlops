# Clinical Readmission Risk Predictor (CRRP)

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Cloud-Ready: Codespaces](https://img.shields.io/badge/Cloud--Ready-Codespaces-brightgreen.svg)](https://github.com/features/codespaces)

## 🏥 Contexto de Negocio

Las readmisiones hospitalarias antes de los 30 días son un indicador crítico de la calidad del cuidado de la salud. Solo en EE. UU., estas representan un costo de más de **$25 mil millones anuales**. 

Este proyecto desarrolla un sistema predictivo para identificar pacientes diabéticos con alto riesgo de readmisión. El valor estratégico de esta solución radica en:
1. **Optimización de Recursos:** Identificar proactivamente a pacientes que requieren planes de alta intensivos.
2. **Mejora de Resultados Clínicos:** Reducir complicaciones post-hospitalarias.
3. **Reducción de Costos:** Minimizar penalizaciones financieras por tasas elevadas de readmisión.

## 🚀 Objetivos del Proyecto

* **Predicción de Riesgo:** Clasificar pacientes con riesgo de readmisión en <30 días utilizando datos clínicos históricos.
* **Explicabilidad (XAI):** Proporcionar transparencia al personal médico sobre los factores que impulsan cada predicción mediante **SHAP values**.
* **Diseño Modular:** Arquitectura de software basada en principios de ingeniería para facilitar el mantenimiento y despliegue (MLOps ready).

## 🏗️ Arquitectura del Sistema

El proyecto implementa un ciclo de vida de Machine Learning profesional:



* **Data Ingestion:** Manejo de datos médicos complejos y tratamiento profesional de valores ausentes (Missing Data Strategy).
* **Feature Engineering:** Agrupación avanzada de diagnósticos (ICD-9 Mapping) y análisis de estabilidad de medicación.
* **Modelado:** Implementación de Gradient Boosting (XGBoost) con manejo de desbalance de clases.
* **Interpretación:** Capa de explicabilidad local para apoyo a la toma de decisiones clínicas.

## 📂 Estructura del Repositorio

```text
├── .devcontainer/     # Configuración de entorno en la nube (Codespaces)
├── data/               # Versionamiento de datasets (Raw vs Processed)
├── src/                # Código fuente modular
│   ├── data_loader.py  # Pipeline de limpieza y ETL
│   ├── features.py     # Ingeniería de atributos clínicos (ICD-9 mapping)
│   ├── train.py        # Pipeline de entrenamiento y evaluación
│   └── interpret.py    # Lógica de explicabilidad con SHAP
├── notebooks/          # Experimentación y EDA detallado
├── tests/              # Pruebas unitarias para validación de datos
├── requirements.txt    # Gestión estricta de dependencias
└── README.md
```
## 📊 Dataset

Se utiliza el UCI Diabetes 130-US Hospitals Dataset, que contiene 10 años de atención clínica en 130 hospitales.

* Muestra: +100,000 encuentros.
* Atributos: 50 variables (demografía, diagnósticos, resultados de laboratorio y 24 medicamentos).

## 🔧 Instrucciones para Ejecución

1. Haz un Fork de este repositorio.
2. En tu fork, haz clic en el botón verde Code.
3. Selecciona la pestaña Codespaces y haz clic en Create codespace on main.
4. El entorno instalará automáticamente todas las dependencias y configurará Python.

