# 💳 Detección de Fraude en Transacciones Financieras con XGBoost, Random Forest y SMOTE

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-orange?logo=googlecolab)
![XGBoost](https://img.shields.io/badge/XGBoost-ML%20Avanzado-green)
![Estado](https://img.shields.io/badge/Estado-Completado-brightgreen)

Sistema de detección de fraude financiero que aplica técnicas avanzadas de Machine Learning para identificar transacciones fraudulentas en un dataset con **alto desbalance de clases** (99.28% normal vs 0.72% fraude).

---

## 📌 Tabla de Contenidos

- [Descripción](#descripción)
- [Objetivo](#objetivo)
- [Dataset](#dataset)
- [Técnicas aplicadas](#técnicas-aplicadas)
- [Tecnologías](#tecnologías)
- [Modelos implementados](#modelos-implementados)
- [Resultados](#resultados)
- [¿Cómo ejecutarlo?](#cómo-ejecutarlo)
- [Aplicación práctica](#aplicación-práctica)
- [Autora](#autora)

---

## 📝 Descripción

Este proyecto forma parte de un portafolio de Inteligencia Artificial aplicada al negocio. A partir de un dataset sintético similar al de fraude real con tarjetas de crédito, se construyeron y compararon modelos supervisados para detectar transacciones fraudulentas, aplicando técnicas avanzadas de balanceo de clases para mejorar la detección de casos minoritarios.

---

## 🎯 Objetivo

Identificar transacciones fraudulentas en un dataset con alto desbalance de clases, aplicando **SMOTE** para balancear los datos y comparando el desempeño de **XGBoost** vs **Random Forest** usando **AUC-ROC** como métrica principal.

---

## 📦 Dataset

| Atributo | Detalle |
|---|---|
| **Tipo** | Dataset sintético generado con `make_classification` (parámetros similares al dataset real de Kaggle) |
| **Total de transacciones** | 284,807 |
| **Transacciones normales** | 282,756 |
| **Transacciones fraudulentas** | 2,051 |
| **Porcentaje de fraude** | 0.72% |
| **Variables** | 29 características (V1–V28 + Amount) |
| **Variable objetivo** | `Class` (0 = Normal, 1 = Fraude) |

---

## 🧠 Técnicas aplicadas

| Técnica | Descripción |
|---|---|
| **SMOTE** | Balanceo de clases desiguales (de 1,641 a 226,204 muestras de fraude en entrenamiento) |
| **XGBoost** | Modelo de gradient boosting avanzado |
| **Random Forest** | Modelo de comparación |
| **AUC-ROC** | Métrica principal para datos desbalanceados |
| **Matriz de confusión** | Análisis de errores del modelo |

---

## 🛠️ Tecnologías utilizadas

| Herramienta | Uso |
|---|---|
| Python 3 | Lenguaje principal |
| Google Colab | Entorno de ejecución |
| XGBoost | Modelo de gradient boosting |
| Scikit-learn | Modelos y métricas de ML |
| Imbalanced-learn (SMOTE) | Balanceo de clases |
| Pandas | Manipulación de datos |
| Matplotlib / Seaborn | Visualización de datos |

---

## 🤖 Modelos implementados

| Modelo | AUC-ROC | Accuracy | Recall (Fraude) | F1-Score (Fraude) |
|---|---|---|---|---|
| Random Forest | 0.5194 | 99% | 4% | 0.07 |
| **XGBoost** | **0.5583** | **77%** | **34%** | **0.02** |

> ✅ El modelo **XGBoost** fue seleccionado como modelo final por su mayor **AUC-ROC** y mejor capacidad para detectar casos de fraude (recall más alto).

> ⚠️ **Nota técnica:** El accuracy del 99% de Random Forest es engañoso en datasets desbalanceados — el modelo simplemente predice "normal" casi siempre. El AUC-ROC es la métrica relevante en este contexto.

---

## 📈 Resultados

### Impacto de SMOTE en el balanceo de clases

| | Antes de SMOTE | Después de SMOTE |
|---|---|---|
| Transacciones normales (train) | 226,204 | 226,204 |
| Transacciones fraudulentas (train) | 1,641 | 226,204 |

### Hallazgos clave

- **XGBoost superó a Random Forest** en la métrica principal (AUC-ROC: 0.5583 vs 0.5194).
- **SMOTE mejoró significativamente** la capacidad del modelo para detectar fraude al balancear las clases desiguales.
- El dataset con 0.72% de fraude representa un reto típico del mundo real en detección de anomalías financieras.

---

## 📂 Contenido del repositorio

```
├── Detección_de_Fraude_en_Transacciones_Financieras_con_XGBoost__Random_Forest_y_SMOTE.ipynb
│                                        # Notebook principal con todo el análisis y código
└── README.md                            # Documentación del proyecto
```

---

## 🚀 ¿Cómo ejecutarlo?

1. Abre el archivo `.ipynb` en Google Colab.
2. Ejecuta las celdas en orden desde el menú **Entorno de ejecución → Ejecutar todo**.
3. El dataset se genera automáticamente con `sklearn.make_classification` — no necesitas descargar nada.
4. ⚠️ **Las celdas de entrenamiento pueden tardar 10–20 minutos** por el volumen del dataset.

---

## 💼 Aplicación práctica

Este sistema puede integrarse en plataformas financieras para:

- **Alertas en tiempo real** sobre transacciones sospechosas.
- **Reducción de falsos negativos** (fraudes no detectados) con técnicas de balanceo.
- **Priorización de revisión manual** de transacciones de alto riesgo.
- Comparación y selección del mejor modelo según el contexto del negocio (precisión vs recall).

---

## 👤 Autora

**Yasmin Beltre**
Customer Success & Operations Specialist | AI Portfolio – INDOTEL/BID/CYMETRIA 2026
📍 Santo Domingo, República Dominicana
🔗 [LinkedIn](https://linkedin.com/in/yasminbeltre)

---

*Proyecto desarrollado como parte del programa de formación en Inteligencia Artificial INDOTEL/BID/CYMETRIA 2026.*
