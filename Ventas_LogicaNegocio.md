# Ventas

## Listado de Entidades

### clientes **(ED)**

- cliente_id **(PK)**
- nombre
- apellidos
- telefono **(UQ)**
- email **(UQ)**
- direccion
- cp
- ciudad
- pais **(FK)**

### productos **(ED|EC)**

- producto_id **(PK)**
- nombre
- descripcion
- precio
- cantidad <!-- El stock -->

### ventas

- venta-id **(PK)**
- cliente_id **(FK)**
- fecha
- monto

### articulos_x_venta **(EP)**

- articulo_id **(PK)**
- venta_id **(FK)**
- producto_id **(FK)**
- cantidad <!-- Cuantos articulos de ese producto esta comprando el usuario -->

### paises **(EC)**

- pais_id **(PK)**
- nombre
- dominio **(UQ)**

## Relaciones

<!-- Dependiendo de la perspectiva de cual es la entidad que mas te interesa tener el control las relaciones pueden cambiar. -->

1. Un **cliente** tiene **pais** (_1 - 1_ )<!-- Un cliente solo tiene un pais -->
1. Un **cliente** genera **venta** (_1 - M_)
1. Una **venta** tiene **articulo** (_1 - M_)
1. Un **articulo** es un **producto** (_1 - 1_)
