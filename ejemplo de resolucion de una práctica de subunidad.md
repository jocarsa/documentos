# Ejercicio propuesto

Supongamos que en mi encuesta indiqué que me gusta el cine

La inteligencia artificial me propone el siguiente enunciado:
```
Imagina que eres programador/a de una aplicación de cine que necesita guardar y mostrar información básica de películas.

Declara variables para almacenar la siguiente información de una película:

Título

Año de estreno

Duración en minutos

Puntuación media en una escala del 1 al 10

Utiliza literales y constantes cuando corresponda (por ejemplo, una constante para el año actual).

Haz operaciones con operadores aritméticos para calcular:

Cuántos años han pasado desde su estreno.

Cuántas horas y minutos dura la película (a partir de la duración en minutos).

Muestra en pantalla con print() la ficha técnica de la película en formato:

Título: [título]
Estreno: [año] (hace X años)
Duración: [horas]h [minutos]m
Puntuación: [nota]/10


Opcional: Añade un booleano que indique si la película está recomendada (True/False).
```

# Paso 1: Resolver el problema con código:

Abro un editor de código y resuelvo paso a paso el ejercicio propuesto:

```
'''
    Programa de películas
    (c) 2025 Jose Vicente Carratala
    Este programa gestiona datos de películas
'''

titulo = "La Historia Interminable"
anio_de_estreno = 1984
duracion = 102
puntuacion = 10

tiempo_transcurrido = 2025 - anio_de_estreno
horas = int(duracion/60)
minutos = duracion-60

print("Título: ",titulo)
print("Estreno: ",anio_de_estreno," (hace ",tiempo_transcurrido," años)")
print("Duración: ",horas,"h ",minutos,"m")
print("Puntuación: ",puntuacion,"/10")


```

# Ahora completo la actividad según lo que pide la rúbrica de evaluación

## Introducción breve y contextualización - 25% de la nota del ejercicio

El objetivo de este ejercicio consiste en demostrar el uso básico de los bloques constructivos principales de un programa informático.

Para ello, vamos a crear un ejemplo sencillo de cómo generar desde cero hasta 100 un sencillo programa que gestione la información de una película.


## Desarrollo detallado y preciso - 25% de la nota del ejercicio

Para resolver este ejercicio, vamos a:
- Declarar una serie de variables que contendrán la información
- Crear  operaciones aritméticas con las variables
- Presentar debidamente la información en pantalla

## Aplicación práctica - 25% de la nota del ejercicio

Para ilustrar la creación de un programa informático, presentamos el siguiente ejemplo concreto, en el cual declaramos variables iniciales y procesamos los datos para realizar cálculos:

```
'''
    Programa de películas
    (c) 2025 Jose Vicente Carratala
    Este programa gestiona datos de películas
'''

titulo = "La Historia Interminable"
anio_de_estreno = 1984
duracion = 102
puntuacion = 10

tiempo_transcurrido = 2025 - anio_de_estreno
horas = int(duracion/60)
minutos = duracion-60

print("Título: ",titulo)
print("Estreno: ",anio_de_estreno," (hace ",tiempo_transcurrido," años)")
print("Duración: ",horas,"h ",minutos,"m")
print("Puntuación: ",puntuacion,"/10")


```

## Conclusión breve - 25% de la nota del ejercicio

Con este ejercicio podemos demostrar que es sencillo crear un programa con una estructura base en Python y que no solo funcione correctamente sino que sea legible.

# Ultima parte: unir las partes anteriores en un solo bloque de texto



El objetivo de este ejercicio consiste en demostrar el uso básico de los bloques constructivos principales de un programa informático.

Para ello, vamos a crear un ejemplo sencillo de cómo generar desde cero hasta 100 un sencillo programa que gestione la información de una película.


Para resolver este ejercicio, vamos a:
- Declarar una serie de variables que contendrán la información
- Crear  operaciones aritméticas con las variables
- Presentar debidamente la información en pantalla



Para ilustrar la creación de un programa informático, presentamos el siguiente ejemplo concreto, en el cual declaramos variables iniciales y procesamos los datos para realizar cálculos:

```
'''
    Programa de películas
    (c) 2025 Jose Vicente Carratala
    Este programa gestiona datos de películas
'''

titulo = "La Historia Interminable"
anio_de_estreno = 1984
duracion = 102
puntuacion = 10

tiempo_transcurrido = 2025 - anio_de_estreno
horas = int(duracion/60)
minutos = duracion-60

print("Título: ",titulo)
print("Estreno: ",anio_de_estreno," (hace ",tiempo_transcurrido," años)")
print("Duración: ",horas,"h ",minutos,"m")
print("Puntuación: ",puntuacion,"/10")


```

Con este ejercicio podemos demostrar que es sencillo crear un programa con una estructura base en Python y que no solo funcione correctamente sino que sea legible.

