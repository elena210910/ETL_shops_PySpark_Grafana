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

## *Pasos de realizacion*.🚀

### Instalación de Docker y Docker Compose

1. **Instalación de Docker**: - Descarga e instala  [Dockerfile](https://github.com/elena210910/ETL_shops_PySpark_Grafana/blob/main/Docker/Dockerfile).
2. **Instalación de Docker Compose**: - Descarga e instala [Docker Compose](https://github.com/elena210910/ETL_shops_PySpark_Grafana/blob/main/Docker/docker-compose).



### DAG

EL script que define un [DAG](https://github.com/elena210910/ETL_shops_PySpark_Grafana/blob/main/Dag) en Apache Airflow con siete tareas diferentes: 
generar datos, procesar datos, limpiar datos, cargar en PostgreSQL, cargar en ClickHouse,
realizar operaciones analíticas. Las tareas están 
configuradas para ejecutarse en un orden específico usando operadores de Python.

## Conexión a la base de datos

"IMPORTANTE: [Conéctate a la base de datos](https://github.com/elena210910/ETL_shops_PySpark_Grafana/blob/main/admin.PNG) a través de ADMIN en la interfaz de AIRFLOW.
Las contraseñas y otros detalles están especificados en el archivo docker-compose

## Ejecutamos nuestro DAG en Airflow


**Podemos ver cómo nuestras tareas se completaron con éxito!**



![](https://github.com/elena210910/ETL_shops_PySpark_Grafana/blob/main/dag_succes.PNG)



### Y ahora, veamos los resultados..

1. Ejemplo de datos generados - [sales_data.csv](https://github.com/elena210910/ETL_shops_PySpark_Grafana/blob/main/ej_csv.PNG)
   
2. Los datos cargados en [PostgreSQL](https://github.com/elena210910/ETL_shops_PySpark_Grafana/blob/main/postgres.PNG) (en un total son dos tablas).
   
3. CLickHouse - Atreves de una consulta simple de SQL (SELECT *
                                                       FROM aggregated_sales_data asd 
                                                       ORDER BY product_id 
                                                       LIMIT 10)
   podemos observar q datos han sido [cargados](https://github.com/elena210910/ETL_shops_PySpark_Grafana/blob/main/click_tab.PNG).

4. Visualicemos los datos obtenidos en [GRAFANA](https://github.com/elena210910/ETL_shops_PySpark_Grafana/blob/main/chart_grafana.PNG).
   Conectémonos a la tabla en ClickHouse - Veamos en qué región están los compradores más activos 🚀


