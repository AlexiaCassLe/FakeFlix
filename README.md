# Proyecto-FakeFlix

<h1>Resumen de la estructura del dataset:</h1>

Nos encontramos con una base de datos que define series y películas, además de darnos información relevante de análisis como es directores, casting, país, fecha en la que se añadió al servicio, año de lanzamiento, rating, duración (temporadas y minutos respectivamente) y género.

La gran mayoría de los datos son categóricos, siendo todos formateados como texto plano, se necesitará hacer ciertas correcciones, como en fechas y duración, para que sean numéricos y puedan ser más útil al análisis.

<b>La base de datos se comprende de los siguientes campos</b>:

1. Total registros: 8.702
2. Columnas principales: Statistical Analysis
- Type: Tipo de contenido (Movie o TV Show)
- Tittle: Título de la película o serie.
- Director: Nombre del director (donde encontramos con 2543 valores vacíos
- Cast: Reparto (encontramos 819 celdas vacías
- Country: País de origen del contenidoretención 
- Fecha en la que se añadió a la plataforma
- Release_year: Año de lanzamiento
- Rating: clasificación por edad (tenemos que unificar los criterios)
- Duration: duracición de las películas en minutos y de las series por temporadas.
- Géneros: clasíficación de las distintas películas y series.

![image](https://github.com/user-attachments/assets/f5f6a919-bb61-4670-89d2-189c8ca48436)


<h2>Hallazgos clave:</h2>

<h3>1. Distribución del Tipo de Contenido:</h3>
<ul>
<li>Películas (Movies): 6,127 registros (aprox 70%).
<li>Series (TV Shows): 2,577 registros (aprox 30%).
</ul>


<h3>2. Principales Países de Origen (Top 10):</h3>
<ul>
    <li>Estados Unidos (3,169 registros)</li>
    <li>India (1,006 registros)</li>
    <li>Reino Unido (611 registros)</li>
    <li>Otros países destacados:
        <ul>
            <li>Canadá</li>
            <li>Japón</li>
            <li>Francia</li>
            <li>Corea del Sur</li>
            <li>España</li>
            <li>México</li>retención 
            <li>Australia</li>
        </ul>
    </li>
    <li>Valores nulos (827 registros)</li>
</ul>
<b>Gráfico de cantidad de países</b>
<br></br>
<img src="https://github.com/user-attachments/assets/ed933726-3939-459c-a645-c0614c394b36" alt="Imagen 2" />

<h3>3. Años de Lanzamiento:</h3>
<ul>
    <li>Rango: 1925 - 2021</li>
    <li>Gran mayoría del contenido fue lanzado después de 2017</li>
    <li>Mayor concentración de títulos entre 2013 y 2021</li>
    <li>El formato actualmente no se encuentra como fecha</li>
</ul>
<b>Gráfico de año de lanzamiento</b>
<br></br>
<img src="https://github.com/user-attachments/assets/d8d07c7f-bb62-4be6-a6d9-95b0522d32bd" alt="Imagen 3" />

<h3>4. Rating:</h3>
<ul>
    <li>Hay ratings que cumplen mismos criterios y pueden ser normalizados</li>
    <li>TV-MA (Contenido para adultos): 3,183 registros (mayoría)</li>
    <li>TV-14 (Adolescentes): 2,133 registros</li>
    <li>Otros relevantes:
        <ul>
            <li>TV-PG</li>
            <li>R</li>
            <li>PG-13</li>
        </ul>
    </li>
    <li>Datos atípicos: Algunos valores erróneos como "74 min", "84 min" que se han solapado de otras columnas</li>
</ul>
<b>Gráfico de ratings</b>
<br></br>
<img src="https://github.com/user-attachments/assets/fa5660bd-e8f0-46e4-a1e5-c12c2cff84a4" alt="Imagen 4" />

<h3>5. Duración del Contenido:</h3>Statistical Analysis
<ul>
    <li>Mezcla de formatos:
        <ul>
            <li>"1 Season", "2 Seasons" para series</li>
            <li>"112 min", "95 min" para películas</li>
        </ul>
    </li>
    <li>Es necesario separar la duración en minutos (películas) y temporadas (series) para un análisis detallado</li>
    <li>Se requiere formatear esta columna como número, actualmente se presenta como texto plano</li>
     <li>En el caso de las películas, encontramos ciertos valores extremos o "outliers" situados en torno a 309 minutos</li>
    <li>En el caso de las series, encontramos ciertos valores extremos o "outliers" situados en 17 temporadas</li>
</ul>
<b> Gráficos películas Películas</b>
<br></br>
<img src="https://github.com/user-attachments/assets/ef08b3b4-bf0e-46ac-b4d9-ad699f87d02a" alt="Imagen 5" />
![image](https://github.com/user-attachments/assets/3a019649-c9b0-4e77-9219-f0fd20b1e7d5)
retención 
<b>Gráficos Series</b>
<br></br>
<img src="https://github.com/user-attachments/assets/8cd0cca9-862c-401d-bd92-5627bf2aa2d3" alt="Imagen 6" />
![image](https://github.com/user-attachments/assets/7554b802-23ae-4089-9ce9-da92e52fbe1d)


<h3>6. Géneros:</h3>
<ul>
    <li>Formato confuso de los distintos géneros, apilados todos en la misma columna</li>
    <li>Hay géneros cuya única diferencia es el ser de serie o película</li>
</ul>

<h2>Actuaciones a hacer:</h2>
<ul>
    <li>Sustituir valores nulos con valores desconocidos para que no afecte al análisis</li>
    <li>Separar y reformatear las columnas de directores y géneros para un mejor análisis</li>
    <li>Corrección del formato de la duración y pasarlo a formato de número</li>
    <li>Corrección de fecha de lanzamiento para que se adecue a "año"</li>
    <li>Normalizar los valores de los rating para una mejor comprensión y simplificación</li>
    <li>Corregimos "Soviet Union" por "Rusia"</li>
    <li>Corregimos "West Germany" por "Germany"</li>
</ul>

  

<h2>Diario día 1</h2>

Día 1retención 


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
 
<h3>Objetivos Día 3:</h3>

- Valorar Outliers
- Asegurar validaciones y formatos
- Ajustar directores
- Analisis de datos

<h3>Objetivos Día 4:</h3>
<ul>
    <li>Análisis estadístico (relacionar diferentes columnas/categorias) (Laura)
    <li> (Laura)
    <li> (Laura)
    <li>Relación año de producción y géneros (Alexia)
    <li>Tendencias de lanzamientos en el tiempo (Alexia)
    <li>Duración de contenidos y retención (Alexia)
    <li>Rango duración de peliculas (Alexia)
    <li>Diversidad géneros y directores (Cris)
    <li>Patrones de adición de contenidos y estacionalidad
    <li>Top 5: paises que más contenido producen (Cris)
    <ul>
        <li>y dentro de ese Top 5, sacar los contenidos que más producen cada país (Cris)
    </ul>
    <li>Top 5: generos mas producidos (Cris)
    <li>Top 5: años que más peliculas/series se han producido. (Cris)
</ul>
