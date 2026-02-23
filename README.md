# EXPLICABILIDAD DE MODELOS PREDICTIVOS CON RANDOM FOREST
Análisis con SHAP y LIME sobre el dataset Social Network Ads
# Objetivo
Entrenar un modelo supervisado de clasificación basado en Random Forest para predecir la variable Purchased, y aplicar técnicas de explicabilidad (SHAP y LIME) con el fin de comprender cómo las variables influyen en las decisiones del modelo, así como reflexionar sobre la transparencia, los riesgos éticos y las implicaciones sociales de su posible implementación.

---

## 📊 Dataset
Se utilizó el conjunto de datos **Social Network Ads**, el cual contiene información demográfica y económica de usuarios:

- Gender  
- Age  
- EstimatedSalary  
- Purchased (variable objetivo)

El dataset se encuentra disponible en la carpeta `data/`.

---

## 🧠 Metodología

La metodología empleada en este trabajo se basa directamente en las acciones desarrolladas en el notebook de Google Colab, siguiendo un flujo típico de aprendizaje supervisado con énfasis en explicabilidad (XAI).

### Exploración de datos
Se realizó una inspección inicial para verificar su estructura, tipos de datos y variable objetivo. Posteriormente, se llevó a cabo un análisis exploratorio de datos (EDA), incluyendo visualizaciones de la distribución de la variable *Purchased* y el comportamiento de las variables *Age* y *EstimatedSalary*, tanto de forma general como segmentada por clase.

### Preprocesamiento
Como parte del preprocesamiento, la variable categórica *Gender* fue codificada en formato binario (0/1). No se aplicó escalado de variables, ya que el modelo seleccionado (Random Forest) no lo requiere y mantener las variables en su escala original favorece la interpretabilidad de las técnicas de explicabilidad utilizadas.

### División de los datos
El conjunto de datos fue dividido en subconjuntos de entrenamiento y prueba utilizando una partición estratificada, con el objetivo de preservar la proporción de clases en ambos conjuntos.

### Entrenamiento del modelo
Se entrenó un modelo **Random Forest Classifier** para un problema de clasificación binaria, utilizando hiperparámetros básicos y sin realizar procesos de ajuste complejo (tuning), priorizando la claridad metodológica y la interpretabilidad del modelo.

### Evaluación del modelo
El desempeño del modelo fue evaluado mediante métricas estándar, incluyendo accuracy, matriz de confusión y reporte de clasificación (precision, recall y F1-score), con el fin de verificar su capacidad predictiva antes de aplicar técnicas de explicabilidad.

### Técnicas de explicabilidad (XAI)
Para analizar cómo el modelo toma decisiones, se aplicaron técnicas de inteligencia artificial explicable. En primer lugar, se utilizó **SHAP** para obtener explicaciones globales (importancia de variables) y locales (predicciones individuales). Posteriormente, se empleó **LIME** para generar explicaciones locales adicionales y contrastar los resultados obtenidos con SHAP.

### Análisis ético
Finalmente, a partir de las explicaciones generadas, se realizó un análisis reflexivo sobre la transparencia del modelo, la influencia de variables sensibles y los posibles riesgos éticos y sociales asociados a su implementación.

---

## 📈 Resultados principales
El modelo Random Forest obtuvo un **accuracy aproximado del 91 %** sobre el conjunto de prueba, mostrando un desempeño equilibrado entre las clases *Compra* y *No compra*. 

Los análisis de explicabilidad evidencian que las variables **Age** y **EstimatedSalary** son las que ejercen mayor influencia en las decisiones del modelo, tanto a nivel global como local. En contraste, la variable **Gender** presenta un impacto reducido, lo que disminuye el riesgo de sesgos directos asociados a esta característica sensible.

Las explicaciones locales obtenidas mediante SHAP y LIME muestran coherencia en la interpretación de decisiones individuales, reforzando la confianza en el comportamiento del modelo.

---

## 📁 Estructura del repositorio
```text
grupal_S4/
├── data/          # Dataset utilizado
│   └── Social_Network_Ads.csv
├── notebooks/     # Notebook principal del análisis
│   └── Deber_Grupal_S4.ipynb
├── figures/       # Gráficos y visualizaciones XAI
│   ├── eda_purchased_distribution.png
│   ├── shap_global_summary.png
│   ├── shap_global_bar.png
│   ├── shap_local_compra.png
│   ├── shap_local_no_compra.png
│   ├── lime_local_compra.png
│   └── lime_local_no_compra.png
└── README.md
```
---

## 🎥 Presentación técnica

Enlace a la presentación técnica donde se explica el problema abordado, la metodología aplicada, las técnicas de explicabilidad utilizadas, el análisis comparativo y las conclusiones finales:

👉 **ENLACE AL VIDEO:**  
https://ENLACE_DEL_VIDEO
