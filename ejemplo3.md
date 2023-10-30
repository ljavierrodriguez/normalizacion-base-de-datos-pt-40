Aquí tienes un ejemplo simplificado de un diagrama entidad-relación (DER) para un sistema de gestión de una biblioteca. El DER representa las entidades, atributos y relaciones entre ellas en un formato gráfico.

En este caso, consideraremos tres entidades principales: `Libro`, `Autor` y `Usuario`, junto con una relación `Préstamo` entre los usuarios y los libros prestados.

```
                +------------------+
                |      Autor       |
                +------------------+
                | ID (PK)          |
                | Nombre           |
                | Nacionalidad     |
                +------------------+
                       |          
                       | 1      
                       |          
                +------------------+
                |      Libro       |
                +------------------+
                | ID (PK)          |
                | Título           |
                | Año Publicación  |
                +------------------+
                | Autor (FK)       |
                +------------------+
                       |         
                       | N
                       |         
                +------------------+
                |     Préstamo     |
                +------------------+
                | ID (PK)          |
                | Fecha Préstamo   |
                +------------------+
                | Libro (FK)       |
                | Usuario (FK)     |
                +------------------+
                       |         
                       | N
                       |         
                +------------------+
                |     Usuario      |
                +------------------+
                | ID (PK)          |
                | Nombre           |
                | Dirección        |
                +------------------+
```

En este diagrama:

- `Autor` y `Libro` son entidades independientes con sus propios atributos.
- `Préstamo` es una entidad que representa la relación entre `Libro` y `Usuario`, ya que un usuario puede tomar prestados uno o varios libros, y un libro puede ser prestado a varios usuarios.
- `Préstamo` tiene claves foráneas (`Libro (FK)` y `Usuario (FK)`) que hacen referencia a las claves primarias de `Libro` y `Usuario`, respectivamente.

Recuerda que este es un ejemplo simple y que los sistemas de bases de datos del mundo real pueden ser más complejos, involucrando más entidades y relaciones. Un diagrama entidad-relación es una herramienta útil para visualizar la estructura y las conexiones en una base de datos antes de su implementación.