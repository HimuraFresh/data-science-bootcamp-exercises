# data-science-bootcamp-exercises

Prácticas resueltas de un bootcamp de Data Science (480h): Python, SQL, análisis de datos, Machine Learning y Deep Learning.

Este repositorio recoge las **prácticas obligatorias** de cada unidad del bootcamp, reorganizadas por módulo temático. No incluye la teoría, los workouts ni los ejercicios de clase: solo el trabajo evaluable resuelto, para que sea fácil ver qué se hizo en cada tema.

## Estructura

Cada módulo contiene sus unidades numeradas en orden cronológico, y cada unidad una carpeta `practica-obligatoria/` con el notebook resuelto y los recursos que necesita para ejecutarse (datasets en `data/`, imágenes en `img/`, utilidades como `bootcampviztools.py`):

```
modulo/
└── unidad/
    └── practica-obligatoria/
        ├── practica-obligatoria-<tema>.ipynb
        └── data/ · img/ · *.py (si la práctica los usa)
```

Convención de nombres: minúsculas y guiones (`kebab-case`), sin la numeración administrativa del bootcamp. Los archivos de datos y las imágenes conservan su nombre original para no romper las rutas relativas de los notebooks.

## Contenido

### 01-programacion-basica
Fundamentos de Python: Markdown y herramientas de trabajo, sintaxis básica, flujo de control (bucles y condicionales, con ejercicios extra), colecciones y funciones, módulos y programación orientada a objetos.

### 02-herramientas-avanzadas
NumPy (vectores, matrices, arrays, agregaciones) y Pandas (Series, DataFrames, selección, filtrado, nulos, duplicados, groupby), en dos niveles cada uno.

### 03-data-analysis
El ciclo de análisis de datos completo: procesos ETL, lectura y procesado de ficheros (CSV, Excel, XML, JSON), bases de datos con SQL (SQLite), obtención de datos externos vía web scraping y APIs (TMDb), estadística descriptiva univariante y multivariante, y visualización con Matplotlib y Seaborn.

### 04-machine-learning
Estadística inferencial e introducción al ML, seguido de aprendizaje supervisado (regresión lineal y regularización, regresión logística, árboles de decisión, ensembles con bagging y boosting, otros modelos y un repaso general) y no supervisado (clustering con K-Means y DBSCAN, reducción de dimensionalidad con PCA y selección de características).

### 05-deep-learning
Introducción al deep learning y a Keras, redes convolucionales (CNN) con un dataset de ~5.000 imágenes de perros y gatos incluido en el repo, y transfer learning con fine tuning.

## Cómo ejecutar los notebooks

Las prácticas están pensadas para ejecutarse desde su propia carpeta (usan rutas relativas tipo `./data/`). Las librerías principales utilizadas a lo largo del repo son: `numpy`, `pandas`, `matplotlib`, `seaborn`, `scipy`, `scikit-learn`, `tensorflow`/`keras`, `requests`, `beautifulsoup4` y `sqlite3` (incluida en Python).

Notas puntuales:

- La práctica de web scraping y APIs (`03-data-analysis/04-...`) requiere una API key gratuita de [TMDb](https://www.themoviedb.org/) para ejecutar las llamadas; el notebook indica dónde ponerla y ofrece como alternativa los JSON ya descargados en `data/`.
- La práctica de CNN (`05-deep-learning/03-...`) entrena con las imágenes de su carpeta `data/` (~120 MB), por lo que la primera clonación del repo tarda un poco más.
- Varias prácticas usan `bootcampviztools.py`, un módulo de funciones de visualización proporcionado por el bootcamp, que se incluye junto al notebook que lo necesita.
