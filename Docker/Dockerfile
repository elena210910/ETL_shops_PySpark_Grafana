# Imagen base para Airflow
FROM apache/airflow:2.9.2

USER root

# Instalaccion а OpenJDK 17
RUN apt-get update && apt-get install -y openjdk-17-jdk && apt-get clean

# Creación de la carpeta para drivers y descarga del driver PostgreSQL
RUN mkdir -p /opt/airflow/jars && \
    curl -o /opt/airflow/jars/postgresql-42.2.23.jar https://jdbc.postgresql.org/download/postgresql-42.2.23.jar

USER airflow

# Instalación de paquetes adicionales
RUN pip install apache-airflow-providers-apache-spark matplotlib seaborn clickhouse_driver pyspark psycopg2-binary
