# 💳 Detección de Fraude con Tarjetas de Crédito — ML Avanzado

> Proyecto académico desarrollado como parte del curso de Inteligencia Artificial  
> **Autora:** Yasmin Beltre | Customer Success & Operations Specialist  
> [![LinkedIn](https://img.shields.io/badge/LinkedIn-Yasmin%20Beltre-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/yasminbeltre)

---

## 📌 Descripción

Sistema de detección de fraude financiero usando técnicas avanzadas de Machine Learning, incluyendo manejo de datos desbalanceados con SMOTE y comparación de modelos XGBoost vs Random Forest.

---

## 🎯 Objetivo

Identificar transacciones fraudulentas en un dataset con alto desbalance de clases (99.28% normal vs 0.72% fraude), aplicando técnicas avanzadas para mejorar la detección de casos minoritarios.

---

## 🛠️ Tecnologías utilizadas

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-orange?style=flat&logo=googlecolab)
![XGBoost](https://img.shields.io/badge/XGBoost-ML-red?style=flat)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-blue?style=flat)

- **Python 3**
- **Google Colab**
- **XGBoost**
- **Scikit-learn**
- **Imbalanced-learn (SMOTE)**
- **Pandas**
- **Matplotlib**
- **Seaborn**

---

## 🧠 Técnicas aplicadas

| Técnica | Descripción |
|---|---|
| **SMOTE** | Balanceo de clases desiguales |
| **XGBoost** | Modelo de gradient boosting avanzado |
| **Random Forest** | Modelo de comparación |
| **AUC-ROC** | Métrica principal para datos desbalanceados |
| **Matriz de confusión** | Análisis de errores del modelo |

---

## 📈 Resultados

| Métrica | Random Forest | XGBoost |
|---|---|---|
| AUC-ROC | 0.5194 | 0.5583 |
| **Mejor modelo** | | ✅ **XGBoost** |

| Dato | Valor |
|---|---|
| Total transacciones | 284,807 |
| Porcentaje de fraude | 0.72% |
| Técnica de balanceo | SMOTE |

---

## 🔍 Conclusión

XGBoost superó a Random Forest en la detección de fraude. SMOTE mejoró significativamente la capacidad del modelo para identificar transacciones fraudulentas al balancear las clases desiguales.

---

## 🚀 ¿Cómo ejecutarlo?

1. Abre el archivo `.ipynb` en **Google Colab**
2. Ejecuta las celdas en orden
3. El dataset se genera automáticamente
4. ⚠️ Las celdas de entrenamiento tardan **10-20 minutos**

---

## 👩‍💼 Sobre la autora

**Yasmin Beltre** — Customer Success & Operations Specialist con 20+ años optimizando operaciones y procesos. Especializada en CRM Management, Process Optimization y Digital Transformation con foco en AI in Business.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Conectar-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/yasminbeltre)

---

*Proyecto desarrollado como parte del curso de Inteligencia Artificial — 2026*
