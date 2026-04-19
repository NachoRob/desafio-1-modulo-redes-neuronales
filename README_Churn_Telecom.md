# 📊 Predicción de Churn en Telecomunicaciones

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Google Cloud](https://img.shields.io/badge/GoogleCloud-%234285F4.svg?style=for-the-badge&logo=google-cloud&logoColor=white)

Este proyecto desarrolla un sistema de clasificación para predecir la fuga de clientes (**Churn**) en una empresa de telecomunicaciones. El objetivo es transitar desde modelos base con sobreajuste hacia ensambles optimizados capaces de generar valor comercial proactivo.

## 🚀 Stack Tecnológico

* **Lenguaje:** Python 3.x
* **Librerías de ML:** Scikit-Learn, Imbalanced-learn (SMOTE).
* **Análisis de Datos:** Pandas, NumPy.
* **Visualización:** Matplotlib, Seaborn.
* **Entorno:** Jupyter Notebook / Google Colab.

## 📈 Resumen del Desafío

El proyecto se divide en fases de madurez del modelo, abordando problemas comunes como el desbalanceo de clases y el overfitting:

1. **Modelo Base:** Árbol de decisión con métricas iniciales (Accuracy vs Recall).
2. **Optimización Hyper-parámetros:** Uso de `GridSearchCV` para controlar la profundidad del árbol.
3. **Balanceo de Datos:** Implementación de **SMOTE** para mejorar la detección de la clase minoritaria.
4. **Ensambles Heterogéneos:** Implementación manual de un modelo de Bagging con estimadores diversos (LogReg, SVM, Árboles).
5. **Random Forest:** Entrenamiento y evaluación de un bosque aleatorio con métricas **OOB (Out-of-Bag)**.
6. **Modelo Final:** Optimización de Random Forest y análisis de curva **ROC/AUC**.

## 🏆 Resultados Finales

* **AUC-ROC:** 0.91 (Excelente capacidad de discriminación).
* **Recall (Clase 1):** 0.74 (Captura al 74% de los desertores reales).
* **Accuracy Global:** 0.90.

### Atributos Clave (Feature Importance)

El modelo identificó que la fuga está impulsada principalmente por:

1. **ContractRenewal:** El momento del vencimiento es el mayor riesgo.
2. **MonthlyCharge:** Sensibilidad al precio mensual.
3. **DayMins:** Volumen de uso diario.
4. **CustServCalls:** Frustración acumulada por atención al cliente.

## 🛠️ Cómo usar este repositorio

1. Clona el repositorio:

```bash
git clone https://github.com/tu-usuario/churn-telecom-desafio.git
```

2. Instala las dependencias:

```bash
pip install -r requirements.txt
```

3. Ejecuta el notebook principal para ver el flujo completo de entrenamiento y la identificación de los 15 clientes con mayor propensión a la fuga.

Desarrollado con por Ignacio Robles (Nacho) – AI & Cloud Data Engineer.

### Consejos adicionales para tu repo

1. **Requirements.txt:** Incluye `scikit-learn`, `pandas`, `matplotlib`, `seaborn` e `imbalanced-learn`.
2. **Carpeta Data:** Si el dataset es público, súbelo en `/data`. Si es privado, documenta la estructura esperada del CSV.
3. **Gráficos:** La curva ROC (AUC 0.91) es una excelente imagen para incluir en `/images` y referenciarla en el README.

¡Con esto tu repositorio se verá impecable!
