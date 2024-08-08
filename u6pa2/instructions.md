Aquí tienes la versión del ejercicio donde los estudiantes cargarán los datos desde archivos de texto utilizando `np.loadtxt`:

# u6pa2: Análisis de Rendimiento de Pilotos de F1

Dada los siguientes archivos:

- **points_pilots.txt**: Un archivo de texto que contiene la matriz de puntos de los pilotos de F1 a lo largo de 5 años. Cada fila representa los puntos de un piloto en los años 2020, 2021, 2022, 2023 y 2024, separados por espacios.

  Ejemplo de contenido de `puntos.txt`:
  ```
  413 413 347 381 363 408 381 358 318 240
  454 395 214 278 249 168 204 191 49 22
  ```

- **pilotos2024.txt**: Un archivo de texto que contiene los nombres de los pilotos
  Revisar el contenido de `pilotos.txt`:
  
- **years.txt**: Un archivo de texto que contiene los años, separados por espacios.

  Ejemplo de contenido de `anios.txt`:
  ```
  2020 2021 2022 2023 2024
  ```

## Instrucciones:

1. **Cargar los datos desde archivos:**
   Escribe un programa principal que realice lo siguiente:
   
   - Cargue la matriz de puntos desde el archivo `puntos.txt` en un array de NumPy.
   - Cargue los nombres de los pilotos desde el archivo `pilotos.txt` en un array de NumPy.
   - Cargue los años desde el archivo `anios.txt` en un array de NumPy.

2. **Preguntas a responder:**

   Después de cargar los datos, responde a las siguientes preguntas utilizando los arrays cargados:

   - **Piloto con más puntos en total:**
     Escribe un código que muestre el nombre del piloto que ha acumulado más puntos en total a lo largo de los 5 años.

   - **Piloto con más puntos en los últimos 3 años (2022-2024):**
     Escribe un código que muestre el nombre del piloto que ha acumulado más puntos en los últimos 3 años.

   - **Pilotos que disminuyen su rendimiento del año 2023 al 2024:**
     Escribe un código que muestre los nombres de los pilotos cuyo puntaje disminuyó del año 2023 al 2024.

   - **Años en los que Hamilton es mejor que Verstappen:**
     Escribe un código que muestre los años en los que Lewis Hamilton tuvo más puntos que Max Verstappen.

   - **Top 3 pilotos en un año específico:**
     Solicita al usuario que ingrese un año y muestra los 3 pilotos con más puntos en ese año, en orden descendente, con sus puntajes. Un piloto por línea junto con su puntaje.

Asegura que los datos se carguen antes de responder las preguntas, lo que también es un buen ejercicio de estructura de programa para tus estudiantes.