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

La metodología empleada en este trabajo sigue un flujo típico de aprendizaje supervisado con énfasis en explicabilidad (XAI), estructurado para garantizar tanto el desempeño predictivo del modelo como la comprensión de sus decisiones.

### Exploración de datos
Se realizó una inspección inicial para verificar su estructura, tipos de datos y variable objetivo. Posteriormente, se llevó a cabo un análisis exploratorio de datos (EDA), incluyendo visualizaciones de la distribución de la variable *Purchased* y el comportamiento de las variables *Age* y *EstimatedSalary*, tanto de forma general como segmentada por clase.

### Preprocesamiento
Como parte del preprocesamiento, la variable categórica *Gender* fue codificada en formato binario (0/1). No se aplicó escalado de variables, ya que el modelo seleccionado (Random Forest) no lo requiere y mantener las variables en su escala original favorece la interpretabilidad de las técnicas de explicabilidad utilizadas.

### División de los datos
El conjunto de datos fue dividido en subconjuntos de entrenamiento y prueba utilizando una partición estratificada, con el objetivo de preservar la proporción de clases en ambos conjuntos. Se empleó una división del 75 % para entrenamiento y 25 % para prueba (test_size = 0.25), permitiendo evaluar el desempeño del modelo sobre datos no utilizados durante el proceso de entrenamiento.

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

En el notebook principal del repositorio (`Deber_Grupal_S4.ipynb`) se presentan los resultados obtenidos a partir del entrenamiento del modelo y la aplicación de técnicas de explicabilidad. En particular, se destacan los siguientes aspectos:

- Desempeño adecuado del modelo Random Forest, con métricas que evidencian una capacidad consistente para diferenciar entre las clases *Compra* y *No compra*.
- Identificación de las variables **Age** y **EstimatedSalary** como las de mayor influencia en las decisiones del modelo, tanto a nivel global como local, mediante técnicas SHAP.
- Explicaciones locales coherentes de predicciones individuales, obtenidas con SHAP y LIME, que permiten comprender cómo distintas variables contribuyen a cada decisión.
- Análisis reflexivo sobre la transparencia del modelo, la presencia de posibles sesgos y los riesgos éticos asociados a su implementación.

Las visualizaciones y explicaciones que respaldan estos resultados se muestran directamente en el notebook.

---

## 📁 Estructura del repositorio
```text
grupal_S4/
├── data/          # Dataset utilizado
│   └── Social_Network_Ads.csv
├── notebooks/     # Notebook principal del análisis
│   └── Deber_Grupal_S4.ipynb
└── README.md
```
---

## 🎥 Presentación técnica

Enlace a la presentación técnica donde se explica el problema abordado, la metodología aplicada, las técnicas de explicabilidad utilizadas, el análisis comparativo y las conclusiones finales:

👉 **ENLACE AL VIDEO:**  
[https://ENLACE_DEL_VIDEO](https://drive.google.com/file/d/177CxaCwWil_pvzZc916c1hXr0mueXaQt/view?usp=drive_link)
