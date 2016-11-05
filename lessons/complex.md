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
* Definir subconsultas
3. Crear tablas por cada consulta
4. Definir métodos de inserción (Múltiples tablas)
5. Prototipar consultas

---

## Ejemplo

| id   | versión | status |  participants     |
|------|---------|--------|-------------------|
| p001 | 1       | active | ["john", "jane"]  |

---

## Modelar un administrador de proyectos interno

---

# Administradores

---

### Cassandra
### Hbase
### Accumulo
### BigTable

---

# Implementación

---

## [Tutorial de Cassandra](https://docs.datastax.com/en/cql/3.1/cql/cql_intro_c.html)

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
### Tiempo al escribir datos
### Difícil modelar con texto

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
3. Definir consultas
4. Prototipar grafo

---

## Ejemplo

### {tipo:"proyecto", id:001, version:1, status:"active"}->{tipo"participant", name:"John Doe"}

---

## Modelar un administrador de proyectos interno

---

# Administradores

---

### Neo4J
### Titan 
### Giraph
### Dgraph

### Varias multimodelo

...

---

# Implementación

---

## [Tutorial de Neo4J](https://neo4j.com/developer/get-started/)

---

## Ejercicio