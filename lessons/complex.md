# Bases de datos NoSQL

![NoSQL](https://francoistoquer.com/img/nosql.png)

---

# Modelo simple -------> Modelo complejos

---

# Columnas

---

### Guardado de tablas
### Paradigma que guarda columnas, no filas
### Generalmente orientadas a la consulta de las tablas

### Columna1: Valor01, Valor03
### Columna2: Valor300, Valor20

---

## Ventajas

### Transición de SQL 
### Enfocado a consultas
### Enfocado a desempeño*
### Modelado similar a relacional

---

## Desventajas

### Complicado modelar múltiples relaciones
### Complicado encontrar balance en duplicidad
### Implementar esquemas semi-fijos
### Mayormente I/O Bound

---

##Proyectos clásicos

### Aplicaciones con múltiples consultas
### Aplicaciones con mayor cantidad de filtros en consultas
### Sistemas de reportes y análisis (Datawarehouse)

---

## Configuraciones comunes

### Replicado
### Cache
### Particionamiento

---

# Modelando Columnas

---

1. Definir entidades
2. Definir consultas
3. Crear tablas por cada consulta
4. Definir métodos de inserción
5. Prototipar consultas

---

## Ejemplo

| id   | versión | status |  participants     |   |
|------|---------|--------|-------------------|---|
| p001 | 1       | active | ["john", "jane"]  |   |

---

## Modelar un administrador de proyectos interno

---

# Administradores

---

### Cassandra
### Hbase
### Accumulo

...

---

# Implementación

---

## [Tutorial de Cassandra]()

---

## Ejercicio

---

# Grafos

---

### Modelado de entidades y relaciones
### Conjunto de claves-valor o documentos
### Enfocado en relaciones de los objetos

### {Key:Value, Key:Value}->{Key:Value, Key:Value}

---

## Ventajas

### Un porcentaje elevado de proyectos son grafos
### Un sólo tipo de modelado
### Múltiples tipos de relaciones
### Elasticidad
### Múltiples usos

---

## Desventajas

### Consultas en grafos complejos
### Aprender lenguajes de consulta
### Cantidad adicional de información al escribir

---

##Proyectos clásicos

### Aplicaciones web
### Redes sociales
### Sistemas de búsquedas complejas
### Reportes y análisis en base a relaciones

---

## Configuraciones comunes

### Transacciones
### Indexado

---

# Modelando Grafos

---

1. Definir entidades/objetos
2. Definir relaciones entre entidades
3. Elegir punto de denormalización/agregados
4. Definir claves-valor
5. Definir acceso e índices
6. Prototipar documentos

---

## Ejemplo

### {id:p001,
### version:1,
### participants:[{name:"John Doe", role:"Developer"}, {name:"Jane Doe", role:"Manager"}],
### status:"active"}

---

## Modelar un administrador de proyectos interno

---

# Administradores

---

### MongoDB
### CouchDB 
### Couchbase
### Amazon DynamoDB
### RethinkDB
### PouchDB

...

---

# Implementación

---

## [Tutorial de MongoDB](https://try.mongodb.org/)

---

## Ejercicio