Aquí tienes un ejemplo de normalización de una base de datos con relaciones utilizando diferentes formas normales. En este caso, consideraremos una base de datos de una biblioteca que almacena información sobre libros, autores y préstamos.

**Tabla Original (sin normalización):**

| ID Libro | Título           | Autor          | Año Publicación | ID Usuario | Nombre Usuario | Fecha Préstamo |
|----------|------------------|----------------|-----------------|------------|----------------|----------------|
| 1        | Libro1           | Autor1         | 2000            | 101        | Juan           | 2023-07-15     |
| 2        | Libro2           | Autor2         | 2005            | 102        | María          | 2023-07-18     |
| 1        | Libro1           | Autor1         | 2000            | 103        | Carlos         | 2023-07-20     |

Vamos a aplicar la normalización a través de diferentes formas normales:

**Primera Forma Normal (1FN):**

Separamos los datos repetidos y convertimos la información en filas únicas. Agregamos una clave primaria única para cada fila.

Tabla Libros:

| ID Libro | Título           | Autor          | Año Publicación |
|----------|------------------|----------------|-----------------|
| 1        | Libro1           | Autor1         | 2000            |
| 2        | Libro2           | Autor2         | 2005            |

Tabla Usuarios:

| ID Usuario | Nombre Usuario |
|------------|----------------|
| 101        | Juan           |
| 102        | María          |
| 103        | Carlos         |

Tabla Préstamos:

| ID Préstamo | ID Libro | ID Usuario | Fecha Préstamo |
|-------------|----------|------------|----------------|
| 1           | 1        | 101        | 2023-07-15     |
| 2           | 2        | 102        | 2023-07-18     |
| 3           | 1        | 103        | 2023-07-20     |

**Segunda Forma Normal (2FN):**

Identificamos las dependencias parciales y creamos nuevas tablas para eliminarlas.

Tabla Libros:

| ID Libro | Título           | Autor          | Año Publicación |
|----------|------------------|----------------|-----------------|
| 1        | Libro1           | Autor1         | 2000            |
| 2        | Libro2           | Autor2         | 2005            |

Tabla Autores:

| Autor    | ID Libro |
|----------|----------|
| Autor1   | 1        |
| Autor2   | 2        |

Tabla Usuarios:

| ID Usuario | Nombre Usuario |
|------------|----------------|
| 101        | Juan           |
| 102        | María          |
| 103        | Carlos         |

Tabla Préstamos:

| ID Préstamo | ID Libro | ID Usuario | Fecha Préstamo |
|-------------|----------|------------|----------------|
| 1           | 1        | 101        | 2023-07-15     |
| 2           | 2        | 102        | 2023-07-18     |
| 3           | 1        | 103        | 2023-07-20     |

**Tercera Forma Normal (3FN):**

Identificamos las dependencias transitivas y creamos nuevas tablas para eliminarlas.

Tabla Libros:

| ID Libro | Título           | Año Publicación |
|----------|------------------|-----------------|
| 1        | Libro1           | 2000            |
| 2        | Libro2           | 2005            |

Tabla Autores:

| Autor    |
|----------|
| Autor1   |
| Autor2   |

Tabla Libros_Autores:

| ID Libro | Autor    |
|----------|----------|
| 1        | Autor1   |
| 2        | Autor2   |

Tabla Usuarios:

| ID Usuario | Nombre Usuario |
|------------|----------------|
| 101        | Juan           |
| 102        | María          |
| 103        | Carlos         |

Tabla Préstamos:

| ID Préstamo | ID Libro | ID Usuario | Fecha Préstamo |
|-------------|----------|------------|----------------|
| 1           | 1        | 101        | 2023-07-15     |
| 2           | 2        | 102        | 2023-07-18     |
| 3           | 1        | 103        | 2023-07-20     |

En este ejemplo, hemos aplicado la normalización en tres formas normales distintas, lo que ha dado como resultado una estructura más organizada y sin redundancias en las tablas, mejorando la integridad de los datos y facilitando la gestión de la base de datos.