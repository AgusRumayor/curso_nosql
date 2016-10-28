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

## Configuraciones 

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

---
