# Procesamiento de Lenguaje Natural I

## Repositorio para la entrega de trabajos prácticos

Este repositorio contiene las soluciones a los distintos desafíos propuestos en la materia **Procesamiento de Lenguaje Natural I** del posgrado en Inteligencia Artificial del LSE de la FIUBA.

---

### 📘 Descripción breve del Desafío 1

El primer desafío consistió en aplicar técnicas fundamentales de PLN sobre el dataset **20 Newsgroups**, incluyendo:

- Vectorización de textos con TF-IDF.
- Cálculo de similaridad coseno entre documentos.
- Clasificación de textos con modelos de Naive Bayes (`MultinomialNB` y `ComplementNB`), ajustando hiperparámetros del vectorizador para maximizar el F1-score macro.
- Exploración semántica mediante la comparación entre palabras utilizando una matriz término-documento transpuesta.

---

### ⚙️ Requisitos para correr la solución

Para ejecutar correctamente el código del desafío, se requiere tener instalado:

- Python 3.8 o superior
- Jupyter Notebook o entorno compatible
- `scikit-learn`
- `numpy`
- `scipy`
- `optuna`