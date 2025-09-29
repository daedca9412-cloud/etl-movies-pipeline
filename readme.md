📊 ETL Pipeline para Análisis de Ratings de Películas

Este proyecto implementa un Pipeline ETL (Extract, Transform, Load) en Python para procesar y analizar datos de películas y calificaciones.

Incluye:

Extracción de datos desde archivos CSV (movies.csv y ratings.csv).

Transformación y limpieza de datos (tipos de datos, duplicados, nulos, rangos válidos).

Carga simulada en archivos CSV de warehouse (completa, incremental o upsert).

Análisis exploratorio con visualizaciones (histogramas, distribuciones, correlaciones, tendencias).

Monitoreo mediante logging.

## 📂 Dataset

Este proyecto utiliza el dataset **MovieLens** para las pruebas de ETL.

- Fuente: [MovieLens Dataset (GroupLens)](https://www.kaggle.com/datasets/grouplens/movielens-20m-dataset)  
- Archivos requeridos:
  - `movies.csv`
  - `ratings.csv`

### Cómo preparar los datos
1. Descarga los archivos desde el enlace oficial.
2. Colócalos en la carpeta raíz del proyecto (junto al código).
3. Asegúrate de mantener los nombres de archivo tal como aparecen en el código:
   - `movie.csv`
   - `rating.csv`


⚙️ Requisitos

Python 3.8+

Librerías necesarias:

pip install pandas matplotlib seaborn

📂 Estructura del proyecto
etl-movies-pipeline/
│── etl_pipeline.py        # Código principal del pipeline
│── movies.csv             # Dataset de películas
│── ratings.csv            # Dataset de calificaciones
│── requirements.txt       # Dependencias del proyecto
│── README.md              # Este archivo

🚀 Ejecución

Clonar este repositorio:

git clone https://github.com/tu_usuario/etl-movies-pipeline.git
cd etl-movies-pipeline


Instalar dependencias:

pip install -r requirements.txt


Ejecutar el pipeline:

python etl_pipeline.py

📊 Ejemplo de salida

Al correr el pipeline se muestran logs y métricas:

Iniciando Pipeline ETL
Hora de inicio: 2025-09-28 22:15:01
==================================================
RESUMEN DEL PIPELINE ETL
==================================================
Estado: EXITOSO
Duración: 3.24 segundos
Registros extraídos: 105339
Registros procesados y cargados: 105200
Tasa de filtrado: 0.1%


Además, se generan gráficos de:

Distribución de ratings

Top 10 películas más calificadas

Ratings por año

Matriz de correlación

Promedio de ratings por año

🔧 Funciones principales

extraer_datos_csv() → lee archivos CSV.

union() → une datasets en un campo común.

Transformacion() → limpieza, conversión y validación de datos.

carga_de_datos() → simula cargas (full, incremental, upsert).

graficos() → visualizaciones EDA.

etl() → orquestador completo del pipeline.

💡 Mejoras futuras

Conexión a bases de datos reales (SQL/NoSQL).

Integrar orquestadores (Airflow, Prefect).

Automatización con Docker.

Despliegue en la nube (AWS, GCP, Azure).

👨‍💻 Autor

Proyecto desarrollado por Daniel Castiblanco, como práctica de ETL y análisis de datos aplicado a ingeniería electrónica y ciencia de datos.
