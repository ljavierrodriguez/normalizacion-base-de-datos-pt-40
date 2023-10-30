# Ejemplo: 

Aquí tienes un ejemplo simplificado de cómo se podría aplicar la normalización a una base de datos hipotética utilizando diferentes formas normales. En este ejemplo, consideraremos una base de datos de pedidos de clientes.

Supongamos que tenemos una tabla inicial que almacena información sobre pedidos de clientes, donde cada fila representa un pedido y tiene las siguientes columnas: `Id Pedido`, `Cliente`, `Dirección`, `Producto`, `Cantidad`, `Precio Unitario`.

**Tabla Original (sin normalización):**

| Número de Pedido | Cliente | Dirección         | Producto | Cantidad | Precio Unitario |
|------------------|---------|-------------------|----------|----------|-----------------|
| 1                | Juan    | Calle A, Ciudad   | Producto1| 5        | $10             |
| 2                | María   | Calle B, Ciudad   | Producto2| 3        | $15             |
| 3                | Juan    | Calle A, Ciudad   | Producto1| 2        | $10             |

Ahora, vamos a aplicar la normalización a través de diferentes formas normales:

**Primera Forma Normal (1FN):**

Separamos los datos repetidos y convertimos la información en filas únicas. Agregamos una clave primaria única para cada fila.

| Número de Cliente | Cliente | Dirección        |
|-------------------|---------|------------------|
| 1                 | Juan    | Calle A, Ciudad  |
| 2                 | María   | Calle B, Ciudad  |
| 3                 | Juan    | Calle A, Ciudad  |

| Número de Pedido | Producto | Cantidad | Precio Unitario |
|------------------|----------|----------|-----------------|
| 1                | Producto1| 5        | $10             |
| 2                | Producto2| 3        | $15             |
| 3                | Producto1| 2        | $10             |

**Segunda Forma Normal (2FN):**

Identificamos las dependencias parciales y creamos nuevas tablas para eliminarlas.

Tabla Pedidos:

| Número de Pedido | Cliente | Dirección        |
|------------------|---------|------------------|
| 1                | Juan    | Calle A, Ciudad |
| 2                | María   | Calle B, Ciudad |
| 3                | Juan    | Calle A, Ciudad |

Tabla Productos:

| Número de Pedido | Producto | Cantidad | Precio Unitario |
|------------------|----------|----------|-----------------|
| 1                | Producto1| 5        | $10             |
| 2                | Producto2| 3        | $15             |
| 3                | Producto1| 2        | $10             |

**Tercera Forma Normal (3FN):**

Identificamos las dependencias transitivas y creamos nuevas tablas para eliminarlas.

Tabla Pedidos:

| Número de Pedido | Cliente |
|------------------|---------|
| 1                | Juan    |
| 2                | María   |
| 3                | Juan    |

Tabla Clientes:

| Cliente | Dirección        |
|---------|------------------|
| Juan    | Calle A, Ciudad |
| María   | Calle B, Ciudad |

Tabla Productos:

| Número de Pedido | Producto | Cantidad | Precio Unitario |
|------------------|----------|----------|-----------------|
| 1                | Producto1| 5        | $10             |
| 2                | Producto2| 3        | $15             |
| 3                | Producto1| 2        | $10             |

Este es un ejemplo simplificado para ilustrar cómo se aplican las formas normales en la normalización de una base de datos. En situaciones más complejas, es posible que se requiera una normalización más profunda y el diseño podría involucrar más tablas y relaciones.