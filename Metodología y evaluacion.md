# "La clase"

## El profesor imparte

Yo vengo a las clases, en el horario que está previsto, y realizo una serie de ejercicios mediante los cuales muestro los conceptos que se quieren transmitir.

Como este es un ciclo de grado superior, intento que todo sea lo más práctico y lo más aplicado posible.

Yo intento seguir a rajatabla el temario oficial, y lo complementamos en lo que sea necesario.

## El alumno interactúa

El alumno

1. Puede, si asiste a clase, interactuar realizando consultas

2. Fuera del tiempo de la clase, el alumno puede realizar consultas offline (email)

## El trabajo en casa (fuera de horas de clase)

Haced los mismos ejercicios que yo

"A programar se aprende programando"
"Todo lo que aprendes, lo aprendes por repetición"

- Si yo hago un programa, tu haces un programa
- Si yo hago una web, tu haces una web.
- Si yo hago una base de datos, tu haces una base de datos
- ....

En función de vuestra seguridad, o bien repetis "hard", o bien vais adaptando el contenido del ejercicio a vuestros propios intereses.

# Evaluación oficial

Dado que estamos en un ciclo formativo, debéis ser evaluados según los parámetros que establece la normativa

Los contenidos están articulados en
curso -> unidad lectiva -> subunidad lectiva

## Eval basada en subunidades

Encontraréis un ejercicio para realizar por cada subunidad 
Estos ejercicios reflejarán solo el contenido de esa subunidad
Son ejercicios fáciles

## Eval basada en unidades

Encontraréis un ejercicio para realizar al final de cada unidad
Reflejarán el contenido de toda esa unidad
Son ejercicio algo más complejos

## Eval de examen trimestral

Examen que recopila todo lo aprendido en ese trimestre

# Cómo se evalúa

La evaluación de todo el curso en mis seis asignaturas se realiza con una sola rúbrica de evaluación. Hay un SOLO documento de evaluación que os indica cómo responder a las preguntas.

https://github.com/jocarsa/documentos/blob/main/R%C3%BAbrica%20de%20evaluaci%C3%B3n.md

# Ejemplo paso a paso de cómo hacer y entregar una actividad

## Paso 1: Lee el enunciado de la actividad:

Crea un programa en Python llamado "Clasificador de pilotos" que pida al usuario introducir la posición final de un piloto en una carrera de coches (número entero).
Según la posición obtenida, el programa debe mostrar un mensaje diferente:

Si ha quedado en la 1ª posición, mostrar: "¡Eres el campeón de la carrera!"

Si ha quedado en la 2ª o 3ª posición, mostrar: "Subes al podio, gran trabajo."

Si ha quedado entre la 4ª y la 10ª posición, mostrar: "Has puntuado en el campeonato."

En cualquier otra posición, mostrar: "No conseguiste puntos esta vez, sigue entrenando."

## Paso 2: Antes de programar, piensa

que pida al usuario = input

Si ha quedado = if
Si ha quedado = elif
En cualquier otra = else

print resultado

# Paso 3: Recuerda la estructura recomendada de un programa

## docstring
- En primer lugar, arriba del todo, debemos crear un docstring
- Es una descripción del título del programa, el autor, y un breve resumen de lo que hace

## Importaciones
- Importamos librerías necesarias
- Importamos el código que exista en otros archivos

## Variables  globales
- Declaración de variables/parámetros globales
- Crea variables
- Su ámbito será global dentro de todo el programa

## Clases / funciones
- Creamos las clases y las funciones que sean necesarias

## Método o función principal
- Punto de ejecución desde el cual se inicia el programa

# Paso 4: Ahora creamos el programa

```
'''
  Programa clasificador de pilotos
  (c) 2025 Jose Vicente Carratala
  Este programa clasifica a los pilotos de carreras
'''

# Importaciones: Este programa no necesita importaciones


# Variables  globales
posicion_final = ""
mensaje = ""

# Clases / funciones: este programa no necesita clases o funciones

## Método o función principal
# Introducción de datos
posicion_final = input("Introduce la posición en la que has quedado: ")
posicion_final = int(posicion_final) # Tengo que convertir la cadena a numero entero
# Realización de cálculos
if posicion_final == 1:
  mensaje = "¡Eres el campeón de la carrera!"
elif posicion_final == 2 or posicion_final == 3:
  mensaje = "Subes al podio, gran trabajo."
elif posicion_final >=4 and posicion_final <=10:
  mensaje = "Has puntuado en el campeonato."
elif posicion_final >=11:
  mensaje = "No conseguiste puntos esta vez, sigue entrenando."
  
# Impresión de respuestas
print(mensaje)
```

# Ahora rellenamos la rúbrica de evaluación


## 1.-Introducción breve y contextualización - 25% de la nota del ejercicio

En este ejercicio vamos a demostrar la comprensión sobre el uso de las estructuras de control condicional. Este tipo de estructuras nos permiten ejecutar una parte u otra del código fuente según el cumplimiento de una serie de condiciones.

## 2.-Desarrollo detallado y preciso - 25% de la nota del ejercicio

La estructura condicional if contiene los siguientes elementos

Por ejemplo, en este bloque de código:

```
  if condicion:
    codigo
```
Encontramos que:
- if es la palabra reservada a la estructura de control
- condicion es una condición que debe ser evaluada como True para que el codigo se ejecute
- Los dos puntos indican el final de las condiciones y el principio del código a ejecutar
- Y por ultimo, el código, sangrado dentro de la estructura, será el código que se ejecute unicamente si la condición es verdadera

## 3.-Aplicación práctica - 25% de la nota del ejercicio

Para ilustrar de forma más completa un ejemplo de selección, hemos creado este ejercicio que selecciona los ganadores de una carerra de coches:

```
  '''
  Programa clasificador de pilotos
  (c) 2025 Jose Vicente Carratala
  Este programa clasifica a los pilotos de carreras
'''

# Importaciones: Este programa no necesita importaciones


# Variables  globales
posicion_final = ""
mensaje = ""

# Clases / funciones: este programa no necesita clases o funciones

## Método o función principal
# Introducción de datos
posicion_final = input("Introduce la posición en la que has quedado: ")
posicion_final = int(posicion_final) # Tengo que convertir la cadena a numero entero
# Realización de cálculos
if posicion_final == 1:
  mensaje = "¡Eres el campeón de la carrera!"
elif posicion_final == 2 or posicion_final == 3:
  mensaje = "Subes al podio, gran trabajo."
elif posicion_final >=4 and posicion_final <=10:
  mensaje = "Has puntuado en el campeonato."
elif posicion_final >=11:
  mensaje = "No conseguiste puntos esta vez, sigue entrenando."
  
# Impresión de respuestas
print(mensaje)
```

## 4.-Conclusión breve - 25% de la nota del ejercicio
Utilizar estructuras de control va a ser muy útil para poder obtener un control grande sobre aquellos aspectos que necesitemos en nuestros programas, desde el punto de vista de activar o desactivar bloques de código según nos pueda interesar.

# Ultima parte: Elimináis los títulos



En este ejercicio vamos a demostrar la comprensión sobre el uso de las estructuras de control condicional. Este tipo de estructuras nos permiten ejecutar una parte u otra del código fuente según el cumplimiento de una serie de condiciones.



La estructura condicional if contiene los siguientes elementos

Por ejemplo, en este bloque de código:

```
  if condicion:
    codigo
```
Encontramos que:
- if es la palabra reservada a la estructura de control
- condicion es una condición que debe ser evaluada como True para que el codigo se ejecute
- Los dos puntos indican el final de las condiciones y el principio del código a ejecutar
- Y por ultimo, el código, sangrado dentro de la estructura, será el código que se ejecute unicamente si la condición es verdadera


Para ilustrar de forma más completa un ejemplo de selección, hemos creado este ejercicio que selecciona los ganadores de una carerra de coches:

```
  '''
  Programa clasificador de pilotos
  (c) 2025 Jose Vicente Carratala
  Este programa clasifica a los pilotos de carreras
'''

# Importaciones: Este programa no necesita importaciones


# Variables  globales
posicion_final = ""
mensaje = ""

# Clases / funciones: este programa no necesita clases o funciones

## Método o función principal
# Introducción de datos
posicion_final = input("Introduce la posición en la que has quedado: ")
posicion_final = int(posicion_final) # Tengo que convertir la cadena a numero entero
# Realización de cálculos
if posicion_final == 1:
  mensaje = "¡Eres el campeón de la carrera!"
elif posicion_final == 2 or posicion_final == 3:
  mensaje = "Subes al podio, gran trabajo."
elif posicion_final >=4 and posicion_final <=10:
  mensaje = "Has puntuado en el campeonato."
elif posicion_final >=11:
  mensaje = "No conseguiste puntos esta vez, sigue entrenando."
  
# Impresión de respuestas
print(mensaje)
```

Utilizar estructuras de control va a ser muy útil para poder obtener un control grande sobre aquellos aspectos que necesitemos en nuestros programas, desde el punto de vista de activar o desactivar bloques de código según nos pueda interesar.






