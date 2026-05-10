# Instrucciones para descargar el dataset

Por motivos de optimización y buenas prácticas en el control de versiones, los archivos de datos originales (`.csv`) no se suben a este repositorio de GitHub. 

Para poder ejecutar los notebooks de la carpeta `/notebooks`, es necesario descargar los microdatos y colocarlos en esta misma carpeta `/data`.

## Origen de los Datos
El proyecto utiliza los microdatos de la **Encuesta de Inserción Laboral de Titulados Universitarios (EILU) 2019**, concretamente la cohorte de egresados de Máster.

1. Descarga el archivo `EILU_MAST_2019.csv` proporcionado en el campus virtual de la asignatura (o directamente desde la web del Instituto Nacional de Estadística - INE).
2. Guarda el archivo exactamente con ese nombre dentro de esta carpeta `/data`.
3. Al ejecutar el primer notebook (`01_EDA.ipynb`), se generará automáticamente en esta misma ubicación un nuevo archivo llamado `EILU_MAST_2019_limpio.csv` que servirá de base para las fases posteriores de Machine Learning.