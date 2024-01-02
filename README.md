# ETL Identificación de Empresas para Inversión 
## Proyecto en desarrollo, fecha estimada 25/11/2023

## Descripción
Búsqueda de empresas estadounidenses recién constituidas y no muy conocidas con el potencial de ofrecer inversiones exitosas a largo plazo. 

La misión de nuestro equipo de científicos de datos es proveer un conjunto de datos limpio y estructurado con las 10 empresas principales que cumplan con criterios financieros y técnicos específicos para facilitar la toma de decisiones de inversión.

## Criterios de Selección
Para calificar como una de las top 10 empresas, las compañías deben cumplir con los siguientes requisitos:

- Ser empresas fundadas después del año 2000.
- Haber pagado dividendos en algún momento en los últimos años.
- Tener actualmente un Price To Earnings Ratio (PER) menor a 30.
- Poseer actualmente un beneficio por acción (EPS, Earnings Per Share) positivo.

Si hay más de 10 empresas que cumplen estos criterios, utilizaremos un criterio de ordenación adicional para seleccionar las más prometedoras.

## Indicadores Relevantes
Además de los criterios mencionados, seleccionaremos indicadores fundamentales y técnicos adicionales que proporcionen información valiosa para el equipo de inversión. Estos podrían incluir:

- Crecimiento de ingresos año tras año.
- Margen de beneficio neto.
- Volumen de acciones negociadas.
- Variabilidad en el precio de la acción.

## Proceso de ETL
El proceso de ETL se llevará a cabo en dos etapas principales:

### 1. Extracción y Limpieza
Recogeremos datos de diversas fuentes financieras (realizamos "web scaping" de algunas fuentes financieras fiables), combinaremos la información relevante y realizaremos las tareas de limpieza necesarias.

### 2. Análisis y Selección
Realizaremos análisis en la base de datos para extraer el top 10 de empresas basándonos en los criterios establecidos. Luego, filtraremos y extraeremos la información e indicadores fundamentales/técnicos que sean necesarios y suficientes para el equipo de inversión.

## Salida de Datos
La tabla de salida con las top 10 empresas y sus indicadores relevantes se escribirá en formato parquet, listo para su análisis e interpretación por parte del equipo de inversión de la UAX.

## Herramientas y Tecnologías
- SQL (para gestión de bases de datos)
- Python/R (para limpieza y análisis de datos)
- Parquet (para escritura de la tabla de salida)
- Diversas APIs y fuentes de datos financieros

## Contribución
Este proyecto está abierto a contribuciones de estudiantes y profesionales interesados en la ciencia de datos y la inversión financiera. Para contribuir, por favor siga las directrices de contribución que se detallan en este documento.

## Contacto
Para más información o consultas sobre el proyecto, por favor contacte al líder del equipo de inversión de la UAX a través de [correo electrónico / formulario de contacto].

---

Este archivo README proporciona una visión general del proyecto de inversión para el equipo de la UAX. Es importante asegurarse de que todas las herramientas y procesos estén adecuadamente documentados para que los colaboradores puedan seguir fácilmente los pasos necesarios. Además, cualquier cambio en los criterios de selección o en las fuentes de datos debe reflejarse actualizando este documento.
