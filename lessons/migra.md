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
8. Duplicar información
9. Traducir consultas
10. Evaluar resultados

---

## RBDMS -> Cassandra

### CQL
### Modelados similares

---
