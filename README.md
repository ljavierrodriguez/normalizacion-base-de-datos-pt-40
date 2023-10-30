# Normalizacion

La normalización es un proceso en el diseño de bases de datos que tiene como objetivo eliminar la redundancia y mejorar la integridad de los datos. Se basa en un conjunto de reglas llamadas formas normales. Aquí están las reglas básicas para una buena normalización de una base de datos:

1. **Primera Forma Normal (1FN)**: Cada tabla debe tener una clave primaria única y las columnas deben contener valores atómicos, es decir, valores indivisibles.

2. **Segunda Forma Normal (2FN)**: La tabla debe cumplir con 1FN y, además, todas las columnas no clave deben depender completamente de la clave primaria. Si una columna depende solo de una parte de la clave primaria, se debe dividir en una nueva tabla.

3. **Tercera Forma Normal (3FN)**: La tabla debe cumplir con 2FN y, además, las columnas no clave no deben depender transitivamente de la clave primaria. Esto significa que si una columna depende de otra columna que a su vez depende de la clave primaria, la columna dependiente debe moverse a una nueva tabla.

4. **Forma Normal de Boyce-Codd (BCNF)**: Similar a 3FN, pero se enfoca en garantizar que cada dependencia funcional en la tabla sea una dependencia completa de la clave primaria. Esto evita anomalías como la dependencia parcial.

5. **Cuarta Forma Normal (4FN)**: Se asegura de que no haya dependencias múltiples independientes en la tabla, es decir, que no haya conjuntos de columnas que determinen las mismas dependencias para diferentes conjuntos de valores.

6. **Quinta Forma Normal (5FN)**: También conocida como Proyección Unión, esta forma se centra en la descomposición de las tablas para eliminar las redundancias que pueden surgir debido a las dependencias de unión.

Estas son las formas normales más comunes, pero existen formas más avanzadas como la Sexta Forma Normal (6FN) y otras, que abordan casos de diseño de bases de datos más complejos. Es importante destacar que, si bien la normalización ayuda a reducir la redundancia y mejorar la integridad, un exceso de normalización puede llevar a un rendimiento deficiente en consultas y operaciones. El equilibrio entre la normalización y la optimización del rendimiento es esencial en el diseño de bases de datos.

### Ejemplo

- [Normalizacion de Base de Datos](ejemplos.md)
- [Normalizacion de Base de Datos con Relaciones](ejemplos2.md)
- [Diagrama Entidad Relación](ejemplo3.md)