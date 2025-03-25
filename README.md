# Proyecto-FakeFlix

Resumen de la estructura del dataset:

Nos encontramos con una base de datos que define series y películas, además de darnos información relevante de análisis como es directores, casting, país, fecha en la que se añadió al servicio, año de lanzamiento, rating, duración (temporadas y minutos respectivamente) y género.

La gran mayoría de los datos son categóricos, siendo todos formateados como texto plano, se necesitará hacer ciertas correcciones, como en fechas y duración, para que sean numéricos y puedan ser más útil al análisis.

La base de datos se comprende de los siguientes campos:

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
- Géneros: clasíficaciónd e las distintas películsa y series.

Hallazgos clave:

1. Distribución del Tipo de Contenido: -
- Películas (Movies): 6,127 registros (aprox 70%).
- Series (TV Shows): 2,577 registros (aprox 30%).


2. Principales Países de Origen (Top 10):
- Estados Unidos (3,168 registros, 36%).
- India (1,007 registros).
- Reino Unido (609 registros).
- Otros países destacados: Canadá, Japón, Francia, Corea del Sur, España, México, Australia.
- Valores nulos



3. Años de Lanzamiento: -
- Rango: 1925 - 2021.
- Gran mayoría del contenido fue lanzado después de 2017.
- Mayor concentración de títulos entre 2013 y 2021.
- El formato actualmente no se encuentra como fecha.


4. Rating:
- Hay ratings que cumplen mismos criterios y pueden ser normalizados.
- TV-MA (Contenido para adultos): 3,183 registros (mayoría).
- TV-14 (Adolescentes): 2,133 registros.
- Otros relevantes: TV-PG, R, PG-13.
- Datos atípicos: Algunos valores erróneos como "74 min", "84 min" que se han solapado de otras columnas.

5. Duración del Contenido (Muestra Aleatoria):
- Mezcla de formatos: "1 Season", "2 Seasons" para series y "112 min", "95 min" para películas.
- Es necesario separar la duración en minutos (películas) y temporadas (series) para un análisis detallado.
- Se requiere formatear esta columna como número, actualmente se presenta como texto plano


6. Géneros Más Frecuentes (Top 10):
- Formato confuso de los distintos géneros,apilados todos en la misma columna
- Hay géneros cuya única diferencia es el ser de serie o película.

Actuaciones a hacer:
- Sustituir valores nulos con valores desconocidos para que no afecte al análisis
- Separar y reformatear las columnas de directos y géneros para un mejor análisis.
- Correcion del formato de la duración y pasarlo a formato de número
- Corección de fecha de lanzamiento para que se adecue a "año"
- Normalizar los valores de los rating para una mejor comprensión y simplificación

  



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

Objetivos Día 2:
- Finalizar Data Profiling
   - Definir formato de los ratings.
   - Dar valor a las celdas vacias
   - Continuar con la separación de géneros.
   - Ver relaciones.
