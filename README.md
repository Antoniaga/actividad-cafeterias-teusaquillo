# Análisis de cafeterías en Teusaquillo

Proyecto desarrollado para la asignatura Herramientas de Computación en la Nube de la Maestría en Analítica Aplicada.

## Objetivo

Construir un flujo de datos en la nube a partir de la API de Foursquare para analizar la distribución de cafeterías en la localidad de Teusaquillo, Bogotá.

## Arquitectura

Foursquare API → Python/Pandas → Amazon S3 Raw Zone → Amazon EC2 → Parquet + DuckDB → Amazon S3 Zona Optimizada

## Datos

Se utilizaron las categorías oficiales de Foursquare:

- Coffee Shop
- Café

Los resultados fueron depurados y validados geográficamente mediante el polígono oficial de la localidad de Teusaquillo.

## Resultados principales

- 46 establecimientos finales
- 23 Coffee Shop
- 21 Café
- 2 establecimientos híbridos validados
- 37,7% de las celdas de análisis presentan al menos una cafetería
- Máximo de 4 cafeterías por celda de 500 m

## Seguridad

Las credenciales se gestionan mediante variables de entorno y el archivo `.env` no se incluye en el repositorio.

## Tecnologías utilizadas

- Python
- Pandas
- GeoPandas
- Foursquare Places API
- Amazon S3
- Amazon EC2
- Boto3
- Apache Parquet
- DuckDB
- Matplotlib