# ETL_shops_PySpark_Grafana

## Descripción de la tarea
Trabajo en una empresa que gestiona una gran tienda en línea.
Mi tarea es crear una canalización automatizada (Pipeline) para el procesamiento 
y análisis de datos de ventas.

## Stack tecnológico
- **PostgreSQL**: para almacenamiento de datos.
- **ClickHouse**: para operaciones analíticas.
- **Apache Airflow**: para orquestación de tareas.
- **PySpark**: para procesamiento de datos.
- **Grafana**: para visualización de datos finales.

Dado que los datos reales son parte confidencial de la empresa, 
generaré datos realistas de ventas. Luego, cargaré esos datos en una tabla de PostgreSQL, 
y después los procesaré, limpiaré, cargaré en bases de datos y realizaré operaciones analíticas.

## Pasos de realizacion.

### Instalación de Docker y Docker Compose

1. **Instalación de Docker**: - Descarga e instala  [Dockerfile](https://github.com/elena210910/ETL_shops_PySpark_Grafana/blob/main/Docker/Dockerfile).
2. **Instalación de Docker Compose**: - Descarga e instala [Docker Compose](https://github.com/elena210910/ETL_shops_PySpark_Grafana/blob/main/Docker/docker-compose).


### DAG

EL script que define un [DAG](https://github.com/elena210910/ETL_shops_PySpark_Grafana/blob/main/Dag) en Apache Airflow con siete tareas diferentes: 
generar datos, procesar datos, limpiar datos, cargar en PostgreSQL, cargar en ClickHouse,
realizar operaciones analíticas. Las tareas están 
configuradas para ejecutarse en un orden específico usando operadores de Python.

