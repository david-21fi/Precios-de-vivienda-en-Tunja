# Proyecto de Recolección de Datos de Precios de Viviendas en Tunja

## Descripción
Este proyecto se centra en la recolección de datos de precios de viviendas en la ciudad de Tunja mediante técnicas de Web Scraping. Utiliza Python y varias de sus librerías para automatizar la recolección, limpieza y transformación de los datos. El objetivo es crear un conjunto de datos que pueda ser utilizado para análisis y modelos predictivos.


## Fuente de Datos
Los datos se han extraído de varias páginas web de anuncios de venta de viviendas. Aquí se mencionan algunas de las fuentes utilizadas:
- [Puntopropiedad](https://www.puntopropiedad.com)
- [metrocudrado](https://www.metrocuadrado.com)
- [Casas.trivit](https://casas.trovit.com.co/)

## Proceso ETL
### Extracción
La extracción de datos se realizó utilizando la técnica de Web Scraping con Python y las siguientes librerías:
- `requests`: para hacer las solicitudes HTTP a las páginas web.
- `BeautifulSoup`: para parsear y extraer información de las páginas web HTML.
- `Selenium`: para interactuar con páginas dinámicas que requieren JavaScript.

### Transformación
Los datos extraídos se procesaron y limpiaron utilizando las siguientes librerías:
- `pandas`: para manipulación y limpieza de datos.
- `numpy`: para operaciones numéricas.
- `re`: para manejo de expresiones regulares y limpieza de texto.

### Carga
Los datos transformados se guardaron en archivos CSV para su posterior análisis:
- `pandas`: para exportar los datos a formato CSV.
## Características del Conjunto de Datos
El conjunto de datos obtenido incluye las siguientes características (columnas):

| Columna            | Descripción                                              | Tipo de Datos |
|--------------------|----------------------------------------------------------|---------------|
| `latitud`          | codenada geografica en grados                            | flotante      |
| `longitud`          | codenada geografica en grados                           | flotante      |
| `titulo`           | Título del anuncio                                       | Cadena de texto|
| `precio`           | Precio de la vivienda                                    | Flotante      |
| `ubicacion`        | Ubicación de la vivienda (barrio, ciudad)                | Cadena de texto|
| `area`             | Área de la vivienda en metros cuadrados                  | Flotante      |
| `num_habitaciones` | Número de habitaciones                                   | Entero        |
| `num_banos`        | Número de baños                                          | Entero        |
| `url`              | URL del anuncio                                          | Cadena de texto|

### Ejemplo de Registro
Aquí tienes un ejemplo de un registro del conjunto de datos:

| id  | titulo                       | precio | ubicacion          | area  | num_habitaciones | num_banos | latitud   | longitud   | url                          |
|-----|------------------------------|--------|--------------------|-------|------------------|-----------|-----------|------------|------------------------------|
| 1   | Casa en venta en Tunja       | 250000 | Centro             | 120.5 | 3                | 2         | 5.5444    | -73.3579   | [Ver Anuncio](https://...)    |
| 2   | Apartamento en Tunja         | 180000 | Barrio Norte       | 80.0  | 2                | 1         |  5.5476   | -73.3528   | [Ver Anuncio](https://...)    |

## Instalación
Sigue estos pasos para configurar el proyecto en tu máquina local:

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/nombre-del-repositorio.git
   cd nombre-del-repositorio
