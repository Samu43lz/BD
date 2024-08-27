# carreras

<!-- Las entidades las ponemos en plural y los atributos en singular.
    Además si hay espacios debemos reemplazarlos con un guión medio -->

## Listado de Entidades

### carreras **(ED)** <!--  Entidad de Datos -->

- carrera_id **(PK)**
- carrera_nombre
- tipo_carrera **(FK)**
- fecha
- tiempo
- mejor_tiempo
- altitud
- lugar
- pais **(FK)**
- foto

### tipos_carreras **(EC)** <!-- Entidad Catalogo -->

- tipo_carrera_id **(PK)**
- descripcion
- distancia

### Paises **(EC)** <!-- Entidad Catalogo -->

- pais_id **(PK)**
- nombre

## Glosario

- **PK** _Primary Key_
- **FK** _Foreign Key_
- **UQ** _Unique Attribute_
- **ED** Entidad de Datos
- **EP** Entidad Pivote
- **EC** Entidad Catálogo

## Relaciones

1. Una **carrera** _Pertenece_ a un tipo de carrera. (1 a 1)
1. Una **carrera** se _corre_ en un pais. (1 a 1)
