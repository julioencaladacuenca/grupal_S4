# Grupal_S4 – Explicabilidad de Modelos Predictivos (XAI)

Repositorio correspondiente a la actividad **S4**, cuyo objetivo es entrenar un modelo predictivo supervisado y aplicar técnicas de explicabilidad para analizar cómo el modelo toma decisiones, así como reflexionar sobre aspectos éticos, sociales y de transparencia en sistemas de inteligencia artificial.

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
El desarrollo de la actividad siguió las siguientes etapas:

1. Análisis exploratorio de datos (EDA)
2. Evaluación de la calidad de los datos
3. Preprocesamiento de variables
4. Entrenamiento de un modelo predictivo supervisado
5. Evaluación del desempeño del modelo
6. Aplicación de técnicas de explicabilidad (XAI)
7. Análisis ético y reflexivo de los resultados obtenidos

Toda la metodología y el análisis se documentan en el notebook principal del repositorio.

---

## 🤖 Modelo predictivo
- **Tipo de problema:** Clasificación binaria  
- **Modelo utilizado:** Random Forest Classifier  
- **Variable objetivo:** Purchased  

El modelo fue evaluado mediante métricas estándar, incluyendo accuracy, matriz de confusión, precision, recall y F1-score, con el fin de verificar su desempeño antes de aplicar técnicas de explicabilidad.

---

## 📈 Resultados principales
El modelo Random Forest obtuvo un **accuracy aproximado del 91 %** sobre el conjunto de prueba, mostrando un desempeño equilibrado entre las clases *Compra* y *No compra*. 

A partir de las técnicas de explicabilidad aplicadas, se identificó que las variables **Age** y **EstimatedSalary** son las que ejercen mayor influencia en las decisiones del modelo, tanto a nivel global como local. En contraste, la variable **Gender** presenta un impacto reducido, lo que disminuye el riesgo de sesgos directos asociados a esta característica sensible.

Los análisis locales realizados con SHAP y LIME muestran coherencia en las explicaciones individuales, reforzando la confianza en la interpretación del comportamiento del modelo.

---

## 🔍 Técnicas de explicabilidad aplicadas (XAI)
Para analizar la toma de decisiones del modelo, se aplicaron las siguientes técnicas de explicabilidad:

- **SHAP**
  - Explicabilidad global (importancia de variables)
  - Explicabilidad local (predicciones individuales)
- **LIME**
  - Explicaciones locales para casos concretos

Estas técnicas permitieron identificar las variables más influyentes, comparar explicaciones entre métodos y analizar decisiones individuales del modelo. Las visualizaciones generadas se encuentran en la carpeta `figures/`.

---

## ⚖️ Transparencia, sesgos y análisis ético
A partir de las técnicas de explicabilidad, se analizó la transparencia del modelo, la influencia de variables sensibles, los posibles riesgos éticos y sociales de su implementación, así como la importancia de incorporar explicabilidad en sistemas predictivos utilizados en contextos reales. Estas reflexiones se desarrollan dentro del notebook principal.

---

## 📁 Estructura del repositorio
```text
grupal_S4/
├── data/          # Dataset utilizado
│   └── Social_Network_Ads.csv
├── notebooks/     # Notebook principal del análisis
│   └── S4_Explicabilidad_RandomForest_SHAP_LIME.ipynb
├── figures/       # Gráficos y visualizaciones XAI (exportados del notebook)
│   ├── eda_purchased_distribution.png
│   ├── shap_global_summary.png
│   ├── shap_global_bar.png
│   ├── shap_local_compra.png
│   ├── shap_local_no_compra.png
│   ├── lime_local_compra.png
│   └── lime_local_no_compra.png
├── video/         # Enlace a la presentación técnica
│   └── enlace_video.txt
└── README.md
