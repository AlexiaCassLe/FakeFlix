# Proyecto-FakeFlix

Resumen de la estructura del dataset:

1. Total registros: 8.709
2. Columnas principales: 
- Type: Tipo de contenido (Movie o TV Show)
- Tittle: Título de la película o serie.
- Director: Nombre del director (donde encontramos con 2543 valores vacíos, 
- Cast: Reparto (encontramos 819 celdas vacías, donde pondremos Unknown)
- Country: - : Fecha en la que se añadió a la plataforma
- Release_year: Año de lanzamiento
- Rating: clasificación por edad (tenemos que unificar los criterios)
- Duration: duracición de las películas en minutos y de las series por temporadas.


Hallazgos clave:

1. Distribución del Tipo de Contenido:
- Películas (Movies): 6,131 registros (aprox 70%).
- Series (TV Shows): 2,578 registros (aprox 30%).


2. Principales Países de Origen (Top 10):
- Estados Unidos (3,168 registros, 36%).
- India (1,007 registros).
- Reino Unido (609 registros).
- Otros países destacados: Canadá, Japón, Francia, Corea del Sur, España, México, Australia.


3. Años de Lanzamiento:
- Rango: 1925 - 2021.
- Media: Año 2014.
- 50% del contenido fue lanzado después de 2017.
- Mayor concentración de títulos entre 2013 y 2021.


4. Clasificaciones por Edad (Rating):
- TV-MA (Contenido para adultos): 3,183 registros (mayoría).
- TV-14 (Adolescentes): 2,133 registros.
- Otros relevantes: TV-PG, R, PG-13.
- Datos atípicos: Algunos valores erróneos como "74 min", "84 min".



5. Géneros Más Frecuentes (Top 10):
- Películas Internacionales (2,752 registros).
- Dramas (2,427 registros).
- Comedias (1,674 registros).
- Otras categorías importantes: Documentales, Acción & Aventura, Películas Independientes.


6. Duración del Contenido (Muestra Aleatoria):
- Mezcla de formatos: "1 Season", "2 Seasons" para series y "112 min", "95 min" para películas.
- Es necesario separar la duración en minutos (películas) y temporadas (series) para un análisis detallado.

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
