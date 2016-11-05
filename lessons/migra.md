# Bases de datos NoSQL

![NoSQL](https://francoistoquer.com/img/nosql.png)

---

#Migración

---

##Por qué NO migrar
* ACID
* Estabilidad de años
* No tengo necesidad de replicar/particionar
* Cantidad de información moderada
* Mis datos nunca cambian

---

##Por qué migrar
* Data -> Big data
* Asincronía
* Desempeño y disponibilidad > Consistencia
* Necesito particionar
* Complejidad en tipos de datos

---

## Ventajas comunes
* Arquitectura menos limitada
* Modelos de datos menos rígidos
* Escalabilidad 
* Mayor Desempeño*
* Forma de programar
* Menores costos

---

## Son comunes las migraciones?
## Quién utiliza NoSQL

---

## Consideraciones
* En qué datos puedo modificar mi consistencia
* Cuándo es conveniente empezar una migración
* Es posible una migración sin downtime?
* Puedo realizar pruebas de desempeño?
* Es posible particionar la migración?

---

## A migrar!
1. Seleccionar la parte a migrar
2. Seleccionar el modelado apropiado
3. Traducir el modelado ER a el modelado elegido
4. Prototipar el modelado elegido
5. Si es posible, prueba de QA del sistema

---

6. Buscar herramientas de migración
7. Buscar herramientas de traducción de consultas
8. Analizar/Traducir consultas
9. Migrar datos (duplicar)
10. Evaluar resultados

---

## RBDMS -> Cassandra

### CQL
### Modelados similares

---

## Ejemplo
### 1 Seleccionando la parte a migrar
estado(id:int, nombre:varchar(25))
municipio(id:int, idEstado:int, nombre:varchar(50))

---
### 2 Seleccionar modelo apropiado
Columnas

---
### 3 Traducir el modelo
estado(id:int, nombre:text)?
municipio(id:int, idEstado:int, nombre:text)?

municipio_query(idEstado:int, nombreEstado:text, idMunicipio:int, nombreMunicipio:text)

---
### 4 Prototipar el modelo
### CQL
CREATE KEYSPACE migration WITH replication = {'class': 'SimpleStrategy', 'replication_factor': '1'};
CREATE TABLE migration.municipio_query (
    idestado int,
    idmunicipio int,
    nombreestado text,
    nombremunicipio text,
    PRIMARY KEY (idestado, idmunicipio)
);

---

### 6 Herramientas de migración
### sqoop

---

### 7 Herramientas de traducción 
### CQL!!!

---

### 8 Analizar/Traducir consultas
select estado.id as idEstado, estado.nombre as nombreEstado, municipio.id as idMunicipio, municipio.nombre as nombreMunicipio from municipio join estado where estado.id = municipio.idEstado;

municipio_query(idEstado:int, nombreEstado:text, idMunicipio:int, nombreMunicipio:text)
select * from municipio_query;
---

### 9 Migrar datos

### csv export
sudo docker exec admin-mysql sh -c 'exec mysql migration -uroot -p"$MYSQL_ROOT_PASSWORD" -B -e "select estado.id as idEstado, estado.nombre as nombreEstado, municipio.id as idMunicipio, municipio.nombre as nombreMunicipio from municipio join estado where estado.id = municipio.idEstado;"' | sed "s/'/\'/;s/\t/\",\"/g;s/^/\"/;s/$/\"/;s/\n//g" > query.csv

### csv import
cat query.csv | cqlsh -e 'use migration; copy municipio_query (idEstado, nombreEstado, idMunicipio, nombreMunicipio) from stdin with header=true ;

---

### 10 Evaluar resultados

### tiempos en memoria y cpu
### tiempos de respuesta
### ... agregar más datos