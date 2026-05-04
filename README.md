# CleanDatasetNetflix

Notebook de limpieza y preparación de datos del dataset público de Netflix usando Python y Pandas.

---

## Descripción

Este proyecto realiza un proceso completo de **limpieza y transformación** del dataset [Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows) disponible en Kaggle. El objetivo es dejar el dataset listo para análisis o modelos de machine learning, tratando valores nulos, duplicados, tipos de datos incorrectos y columnas mal formateadas hace parte del ejercicio roadmap https://roadmap.sh/projects/cleaning-netflix-dataset.

---

##  Estructura del proyecto

```
CleanDatasetNetflix/
│
├── data/
│   ├── netflix_titles.csv          # Dataset original (Kaggle)
│   └── netflix_titles_clean.csv    # Dataset limpio (output)
│
├── netflix_cleaning.ipynb          # Notebook principal
├── .gitignore
└── README.md
```

---

## Proceso de limpieza

El notebook cubre las siguientes etapas:

| Etapa | Descripción |
|---|---|
|  Exploración inicial | Shape, tipos de datos, valores nulos y duplicados |
|  Tratamiento de nulos | Relleno con `"Unknown"`, moda o eliminación según columna |
|  Limpieza de fechas | Conversión de `date_added` a `datetime`, extracción de año y mes |
|  Columna `duration` | Separación en valor numérico y unidad (`min` / `Season`) |
|  Estandarización de texto | Normalización de mayúsculas en `type` y `rating` |
|  Validación de años | Filtrado de `release_year` con valores fuera de rango |
|  Exportación | Guardado del dataset limpio en `data/netflix_titles_clean.csv` |

---
##  Cómo ejecutar el proyecto

**1. Clona el repositorio**
```bash
git clone https://github.com/TuUsuario/CleanDatasetNetflix.git
cd CleanDatasetNetflix
```

**2. Instala las dependencias**
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

**3. Descarga el dataset**

Ve a [Kaggle - Netflix Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows), descarga `netflix_titles.csv` y colócalo en la carpeta `data/`.

**4. Abre el notebook**
```bash
jupyter notebook netflix_cleaning.ipynb
```
O ábrelo directamente desde **VS Code** con la extensión de Jupyter.

---

##  Dataset original

- **Fuente:** [Kaggle - Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **Autor:** Shivam Bansal
- **Registros:** ~8,800 títulos
- **Columnas:** 12 (show_id, type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, description)

---


##  Autor
Cristian Delgado
