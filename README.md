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

---

### 📙 Descripción breve del Desafío 2

En el segundo desafío se abordó la generación de representaciones vectoriales de palabras mediante **Word2Vec**, utilizando un corpus literario compuesto por archivos PDF.

Las actividades principales incluyeron:

- Procesamiento automático de múltiples archivos PDF desde la carpeta `textos/` para construir un corpus unificado.
- Entrenamiento de un modelo Word2Vec con `Gensim`, configurado con Skip-gram y parámetros ajustados para corpus de baja escala.
- Evaluación cualitativa de la calidad de los embeddings mediante:
  - Similitud entre palabras.
  - Operaciones vectoriales tipo analogía.
  - Visualización del espacio vectorial en 2D y 3D mediante t-SNE.
- El desarrollo completo se encuentra en el archivo `Gensim.ipynb`.

---

### ⚙️ Requisitos para correr la solución

- Python 3.11.9  
- Jupyter Notebook o entorno compatible  
- `gensim`  
- `pypdf`  
- `plotly`  
- `scikit-learn` (≥ 1.2 para compatibilidad con t-SNE multithreaded)  
- Carpeta `textos/` con archivos `.pdf` ubicada en el mismo nivel que el archivo `Gensim.ipynb`

---

### 📗 Descripción breve del Desafío 3

El tercer desafío abordó la **modelización de secuencias de texto** mediante distintas arquitecturas de redes neuronales recurrentes. Se utilizó un corpus literario unificado, obtenido a partir de múltiples archivos PDF, para entrenar modelos que pudieran predecir caracteres futuros en una secuencia, con el objetivo de generar texto de manera autónoma.

Las actividades principales incluyeron:

- Limpieza, normalización y tokenización a nivel caracter del corpus completo.
- Codificación del texto y construcción del vocabulario.
- Implementación de un dataset para generar pares de entrada y salida supervisada.
- Implementación y entrenamiento de un modelo secuencial en Keras que comienza con una capa de embeddings para representar caracteres como vectores densos, seguido por tres bloques recurrentes en cascada: SimpleRNN, LSTM y GRU, y una capa densa con activación softmax para la predicción del próximo carácter.
- Evaluación de los modelos con la métrica de perplejidad sobre el conjunto de validación.
- Generación de texto a partir de los modelos entrenados para evaluar la coherencia y fluidez.

El desarrollo completo se encuentra en el archivo `Desafío 3.ipynb`.

---

### ⚙️ Requisitos para correr la solución

- Python 3.11.9  
- Jupyter Notebook o entorno compatible  
- `tensorflow`  
- `pypdf`  
- `numpy`  
- `matplotlib`  
- Carpeta `textos/` con archivos `.pdf` ubicada en el mismo nivel que el archivo `Desafío 3.ipynb`