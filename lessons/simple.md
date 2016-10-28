# Bases de datos NoSQL

![NoSQL](https://francoistoquer.com/img/nosql.png)

---

# Modelo simple -------> Modelo complejos

---

# Clave-Valor

---

### Es el modelo más simple para una Base de datos
### Paradigma que guarda colecciones de datos
### Múltiples configuraciones y administradores

### Key | Value

---

## Ventajas

### Modelado simple
### Menor tiempo en prototipado de la BD 
### Tiempos de respuesta
### Enfocado a desempeño*
### Mayoría de transacciones: CPU Bound*

Varía en cada administrador, forma de implementar


---

## Desventajas

### Modelar estructuras complejas
### Configurar ajustes para encontrar QAs
### Mayoría de transacciones: CPU Bound*

---

##Proyectos clásicos

### Aplicaciones en tiempo real
### Aplicaciones con cache
### Configuraciones y estados de sistemas
### Partes del sistema con frecuente lectura

---

## Configuraciones comunes

### RAM vs I/O
### Eventaulmente consistente vs transacciones
### Replicado
### BD + Cache

---

# Modelando Clave-Valor

---

1. Definir tipo (string, list*, int, ...)
2. Definir forma de acceso:
 * Llave
 * Llave compuesta
 * Referencia
3. Prototipado de la solución

---

## Ejemplo

### project_id:p001
### project_version:1
### project_participants:["john doe", "jane doe"]
### project_status:"active"

---

## Modelar un administrador de proyectos interno

---

# Administradores

---

### Redis
### Riak
### Memcached
### Hazelcast
### Aerospike
### Amazon SimpleDB
### Oracle NoSQL 
### Tokyo Cabinet

...

---

# Implementación

---

## [Tutorial de Redis](https://try.redis.io/)

---

## Ejercicio

---

# Documentos

---

### Modelado simple de información
### Conjunto de claves-valor
### Paradigma que guarda colecciones de datos generalmente ordenados
### Estandarte del movimiento NoSQL

### {Key:Value, Key:Value}

---

## Ventajas

### Modelado simple
### Guardado en documentos
### Elasticidad en documentos
### Múltiples usos


---

## Desventajas

### Modelar estructuras con múltiples relaciones
### Configurar ajustes para encontrar QAs
### Múltiples técnicas de modelado

---

##Proyectos clásicos

### Aplicaciones web
### Aplicaciones transaccionales
### Búsqueda de documentos por índices
### Aplicaciones con versionamiento

---

## Configuraciones comunes

### Eventaulmente consistente vs transacciones
### Replicado
### Indexado
### Particionamiento

---

# Modelando Documentos

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