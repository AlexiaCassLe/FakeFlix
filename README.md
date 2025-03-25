# Proyecto-FakeFlix

<h1>Resumen de la estructura del dataset:</h1>

Nos encontramos con una base de datos que define series y películas, además de darnos información relevante de análisis como es directores, casting, país, fecha en la que se añadió al servicio, año de lanzamiento, rating, duración (temporadas y minutos respectivamente) y género.

La gran mayoría de los datos son categóricos, siendo todos formateados como texto plano, se necesitará hacer ciertas correcciones, como en fechas y duración, para que sean numéricos y puedan ser más útil al análisis.

<b>La base de datos se comprende de los siguientes campos</b>:

1. Total registros: 8.702
2. Columnas principales: 
- Type: Tipo de contenido (Movie o TV Show)
- Tittle: Título de la película o serie.
- Director: Nombre del director (donde encontramos con 2543 valores vacíos
- Cast: Reparto (encontramos 819 celdas vacías
- Country: - : Fecha en la que se añadió a la plataforma
- Release_year: Año de lanzamiento
- Rating: clasificación por edad (tenemos que unificar los criterios)
- Duration: duracición de las películas en minutos y de las series por temporadas.
- Géneros: clasíficación de las distintas películsa y series.

![image](https://github.com/user-attachments/assets/f5f6a919-bb61-4670-89d2-189c8ca48436)


<h2>Hallazgos clave:</h2>

<h3>1. Distribución del Tipo de Contenido:</h3>
- Películas (Movies): 6,127 registros (aprox 70%).
- Series (TV Shows): 2,577 registros (aprox 30%).


<h3>2. Principales Países de Origen (Top 10):</h3>
- Actualizar ciertos nombres de de paises a la representación actual: West Germany, Soviet Union
- Normalizar nombres de paises para que coincidan (corregir comas, espacios y mayusculas): Reino Unido, Estados Unidos y Polonia
- Estados Unidos (3,169)
- India (1,006 registros).
- Reino Unido (611 registros).
- Otros países destacados: Canadá, Japón, Francia, Corea del Sur, España, México, Australia.
- Valores nulos (827 registros)

![image](https://github.com/user-attachments/assets/ed933726-3939-459c-a645-c0614c394b36)



<h3>3. Años de Lanzamiento:</h3>
- Rango: 1925 - 2021.
- Gran mayoría del contenido fue lanzado después de 2017.
- Mayor concentración de títulos entre 2013 y 2021.
- El formato actualmente no se encuentra como fecha.


<h3>4. Rating:</h3>
- Hay ratings que cumplen mismos criterios y pueden ser normalizados.
- TV-MA (Contenido para adultos): 3,183 registros (mayoría).
- TV-14 (Adolescentes): 2,133 registros.
- Otros relevantes: TV-PG, R, PG-13.
- Datos atípicos: Algunos valores erróneos como "74 min", "84 min" que se han solapado de otras columnas.

![image](https://github.com/user-attachments/assets/481221f7-f0ad-4682-86b1-046e80164755)

<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRmsBYxHWj-LlizbZVMtwX5rZ4i4BCNX_kO2KNbACnO2o5wIz4drKbDx7wnjkhTKT5kRdOx-XrtWsp7/pubchart?oid=331851997&amp;format=interactive"></iframe>

<h3>5. Duración del Contenido (Muestra Aleatoria):</h3>
- Mezcla de formatos: "1 Season", "2 Seasons" para series y "112 min", "95 min" para películas.
- Es necesario separar la duración en minutos (películas) y temporadas (series) para un análisis detallado.
- Se requiere formatear esta columna como número, actualmente se presenta como texto plano


<h3>6. Géneros Más Frecuentes (Top 10)</h3>
- Formato confuso de los distintos géneros,apilados todos en la misma columna
- Hay géneros cuya única diferencia es el ser de serie o película.

<h2>Actuaciones a hacer:</h2>

- Sustituir valores nulos con valores desconocidos para que no afecte al análisis
- Separar y reformatear las columnas de directos y géneros para un mejor análisis.
- Correcion del formato de la duración y pasarlo a formato de número
- Corección de fecha de lanzamiento para que se adecue a "año"
- Normalizar los valores de los rating para una mejor comprensión y simplificación
- Corregimos Soviet Union por Rusia
- Corregimos West Germany por Germany.

  

<h2>Diario día 1</h2>

Día 1


- Creación de las tareas iniciales
- Definición de objetivos
- Exploración de la base de datos
- Revisión y análisis descriptivo de los datos.
- Eliminamos duplicados
- Organización de la columna de géneros (en progreso)
- Formateamos la tabla para mostrar las celdas sin valores.
- Revisamos formatos de columnas (fechas, números, texto)
- Visualizamos la viabilidad de eliminar datos irrelevantes
- Definimos actuaciones frente a celdas vacias

<h3>Objetivos Día 2:</h3>

- Finalizar Data Profiling
   - Definir formato de los ratings.
   - Dar valor a las celdas vacias
   - Continuar con la separación de géneros.
   - Ver relaciones.
- Comenzar Data Cleaning
  - Sustituir valores nulos
  - Cambiar formatos
  - Sustituir paises por países actuales
