# Bases de datos NoSQL

![NoSQL](https://francoistoquer.com/img/nosql.png)

---

# ¿Por qué aprender otra forma de guardar datos?
# Y, ¿por qué no?

---

# Temario

---

# [Introducción]()
## SQL vs NoSQL
* CAP
* BASE vs ACID

## Modelando datos
* Problemas comunes

## Modelado de datos NoSQL
* Actividad Modelado de datos NoSQL

---

## [Modelados simples]()
## Clave-Valor
* Modelando Clave-Valor
* Administradores
* Implementación

## Documentos
* Modelando Documentos
* Administradores
* Implementación

---

## [Modelados complejos]()
## Columnas
* Modelando Columnas
* Administradores
* Implementación

## Grafos
* Modelando grafos
* Administradores
* Implementación

---

## [Conclusiones]()
## Bases de datos orientadas a objetos
* Administradores

## Bases de datos inmutables
* Administradores
* Implementación

## SQL + NoSQL + NewSQL
* Evaluar administradores
* Proyectos

---

#SQL vs NoSQL

![CAP](http://181.215.245.136/content/images/extras/cap.png)

---


#SQL vs NoSQL

![BASE](http://181.215.245.136/content/images/extras/acid.png)

---

# Modelo Relacional
## +++Consistencia
## +Disponibilidad
## --Tolerancia a partición

---

# Modelo Relacional
## ¿Cuándo lo usamos?
## ¿Cuándo debemos usarlo?

---

# Modelo X
## ---Consistencia
## Disponibilidad
## +++Tolerancia a partición

---

# Modelo Y
## ++Consistencia
## --Disponibilidad
## ++Tolerancia a partición

---

# Modelando datos

## Escuela
## Clases
## Profesores
## Alumnos

---

# Problemas comunes (Relacional)

## ¿Cómo se implementa una entidad?
## ¿Cómo se implementa una relación de entidades?
## ¿Cómo se implementa un atributo?

---

# Modelando datos

## Escuela
## Clases
## Profesores
## Alumnos
## Horario de Alumno

---

# Problemas comunes (Relacional)
SELECT m1.name, coordinates.lat, coordinates.lon 
FROM mexico m1
  JOIN population
  JOIN coordinates
  JOIN mexico m2
    ON m1.id = population.id
    AND m1.id = coordinates.id
    AND m1.id = m2.ancestor
  WHERE population.population > 10000

---

# Modelando datos

## Escuela
## Clases
## Profesores
## Alumnos
## Horario de Alumno
## Amigos

---

# Problemas comunes (Relacional)

## Jerarquías profundas
## Valores nulos
## Self-Join
## Denormalización

---

###Qué tal si...

#Modelado de datos NoSQL

---

###Escuela patito -> Clase BD -> Prof John Doe -> Alumno01
###Escuela patito -> Clase BD -> Prof John Doe -> Alumno02
###Escuela patito -> Clase Mate -> Prof John Doe -> Alumno03
###Escuela patito -> Clase Mate -> Prof John Doe -> Alumno02

---

###Escuela(Clase(Profesor)(Alumno(s)))

---

###Escuela:
###--"patito"
###--Clase:
###----"BD"
###----Profesor:
###------"John Doe"
###----Alumno:
###------"Alumno01"
###------"Alumno02"

---

#Modelado de datos NoSQL en base a:

##Problema
##Paradigma de desarrollo
##Consultas

---

#Conceptos generales de Modelado

## Denormalización
## Duplicados
## Referencia

---

#Técnicas comunes

## Agregados
## Listas ordenadas
## Índices
## Índices compuestos
## ...

---

#Técnicas de jerarquías

## Listas de adyacencia
## Path materializado
## Conjuntos anidados
## Denormalización/Agregados

---

#Actividad Modelado de datos NoSQL

### Modelar es igual o más importante que implementar

---

## Modelar un administrador de proyectos interno

---

## Modelar proyecto 