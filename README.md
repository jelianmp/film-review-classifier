# 🎬 Clasificación de Reseñas de Películas con Machine Learning y BERT

Este proyecto tiene como objetivo construir un sistema de clasificación binaria para reseñas de películas (positiva/negativa) utilizando datos de IMDB. Se emplean modelos de aprendizaje automático clásico (Logistic Regression, Random Forest, XGBoost) y un modelo avanzado basado en BERT.

## 📌 Objetivo

Predecir si una reseña es positiva o negativa, maximizando la métrica F1, con un umbral mínimo de 0.85 en el conjunto de prueba.

## ⚙️ Tecnologías usadas

- Python
- pandas, numpy, matplotlib, seaborn
- scikit-learn
- spaCy
- XGBoost
- transformers (BERT)
- Jupyter Notebook

## 🧠 Modelos aplicados

- Regresión Logística (TF-IDF)
- Random Forest (TF-IDF)
- XGBoost (TF-IDF)
- BERT (extractor de embeddings)

## 🔍 Preprocesamiento

- Eliminación de stopwords y signos de puntuación
- Lematización con spaCy
- Vectorización con TF-IDF
- Extracción de embeddings con BERT para una muestra pequeña (por limitaciones de hardware)

## 📊 Resultados

| Modelo             | Accuracy (Test) | F1 Score (Test) |
|--------------------|-----------------|-----------------|
| Regresión Logística | 0.88            | 0.88            |
| Random Forest       | 0.84            | 0.84            |
| XGBoost             | 0.83            | 0.83            |
| BERT (200 muestras) | 0.83            | 0.85            |

Todos los modelos cumplen con el objetivo del proyecto.

## 🧪 Clasificación de Nuevas Reseñas

Se probaron predicciones sobre nuevas reseñas ficticias para comparar el comportamiento de los modelos. Se observa que:

- LR es conservador.
- RF y XGB son permisivos.
- BERT ofrece balance entre precisión y sensibilidad.

## 📁 Estructura del proyecto
film-review-classifier/

├── Proyecto_16.ipynb

├── README.md

├── requirements.txt


⚠️ **Nota sobre los datos:**  
El dataset no está incluido en el repositorio por razones de tamaño, pero todas las transformaciones y pasos están desarrollados completamente en el notebook.

📊 Resultados:

Se logró el objetivo del proyecto, obtener la métrica F1 con un umbral mínimo de 0.85

Los modelos basados en árboles (Random Forest y XGBoost) tienden a ser más permisivos al clasificar reseñas ambiguas o neutras como positivas, mientras que la regresión logística es más conservadora.

BERT mostró un comportamiento más equilibrado, aunque también puede fallar en detectar ciertos matices de lenguaje positivo implícito. En conjunto, usar BERT podría aportar más robustez al clasificador final, especialmente si se integra con otros modelos o se calibra correctamente el umbral de decisión.

✍️ Autor
Jorge Elian Mendoza Pujol

🔗 [LinkedIn](www.linkedin.com/in/jorge-elian-mendoza-pujol-359500283) 
