# Enunciado:

Ejercicio: Clasificación de jugadores de baloncesto por edad

Escribe un programa en Python que pida al usuario la edad de un jugador de baloncesto y muestre por pantalla la categoría en la que debe jugar.

Las categorías son las siguientes (puedes ajustarlas si lo deseas):

Menores de 8 años → Pre-mini

De 8 a 11 años → Mini

De 12 a 15 años → Infantil

De 16 a 17 años → Cadete

De 18 a 20 años → Junior

21 años o más → Senior

Además, si el jugador tiene más de 40 años, el programa debe mostrar un mensaje adicional indicando que es “Veterano con experiencia en la cancha”.

# Escribir pseudocódigo

- Pide al usuario la edad
- Si la edad es menor de 8, pre-mini
- Si la edad va de 8 a 11, mini
- Si la edad va de 12 a 15, infantil
- Si la edad va de 16 a 17, cadete
- Si la edad va de 18 a 20, junior
- Si la edad va de 21 a más, senior
- Si la edad es mayor que 40, veterano
- Muestra la categoria

# Empezamos a meter "palabritas"

- Pide al usuario la edad (esto lo voy a solucionar con input)
- Si la edad es menor de 8, pre-mini (esto lo voy a solucionar con if)
- Si la edad va de 8 a 11, mini (esto lo voy a solucionar con if)
- Si la edad va de 12 a 15, infantil (esto lo voy a solucionar con if)
- Si la edad va de 16 a 17, cadete (esto lo voy a solucionar con if)
- Si la edad va de 18 a 20, junior (esto lo voy a solucionar con if)
- Si la edad va de 21 a más, senior (esto lo voy a solucionar con if)
- Si la edad es mayor que 40, veterano (esto lo voy a solucionar con if)
- Muestra la categoria (esto lo voy a solucionar con print)

# Bloques fundamentales y código fuente

```
# Docstring
''' 
  Programa clasificador de baloncesto
  v0.1 Jose Vicente Carratala
  Este programa clasifica categorías por edades
'''

# Importaciones
# Este programa no requiere importaciones

# Declaración de variables globales
# Inicializamos las variables con valores vacíos

edad = 0
categoria = ""

# Funciones/clases
# En este programa no hay funciones o clases

# Función principal

edad = input("Introduce tu edad: ")
edad = int(edad) # Convierto la edad en un entero
if edad < 8:
  categoria = "pre-mini"
elif edad >= 8 and edad <= 11:
  categoria = "mini"
elif edad >= 12 and edad <=15:
  categoria = "infantil"
elif edad >= 16 and edad <=17:
  categoria = "cadete"
elif edad >= 18 and edad <=20:
  categoria = "junior"
else:
  categoria = "senior"
  
print("Tu edad es de",edad,"años y tu categoría es: ",categoria)  

if edad > 40:
  print("Veterano con experiencia en la cancha")
  
```

# Rúbrica de evaluación

## 1.-Introducción breve y contextualización

Las estructuras de control de selección nos permiten ejecutar diferentes bloques de código de forma condicional, es decir, la ejecución de esos bloques está supeditada a la validación de una expresión.

Nos sirve para elegir qué partes de un programa se activan y cuales permanecen sin ejecutarse.

## 2.-Desarrollo detallado y preciso

Cuando introducimos una condicion, utilizamos, en primer lugar, la cláusula if (si condicional)

Escribiremos de la siguiente forma:

```
if condicion:
  codigo a ejecutar
```
El código solo se ejecutará si la validación de la condición resulta ser cierta

Además tenemos la posibilidad de ejecutar código en el caso falso, mediante la claúsula else

Ejemplo:
```
if condicion:
  codigo que se ejecuta en el caso verdadero
else:
  codigo que se ejecuta en el caso falso
```

(explicar también elif)

## 3.-Aplicación práctica

Para ilustrar mejor este concepto, a continuación se muestra un ejercicio en el que en primer lugar se le pide la edad al usuario, y se le clasifica, en categorías de baloncesto, según su edad

```
# Docstring
''' 
  Programa clasificador de baloncesto
  v0.1 Jose Vicente Carratala
  Este programa clasifica categorías por edades
'''

# Importaciones
# Este programa no requiere importaciones

# Declaración de variables globales
# Inicializamos las variables con valores vacíos

edad = 0
categoria = ""

# Funciones/clases
# En este programa no hay funciones o clases

# Función principal

edad = input("Introduce tu edad: ")
edad = int(edad) # Convierto la edad en un entero
if edad < 8:
  categoria = "pre-mini"
elif edad >= 8 and edad <= 11:
  categoria = "mini"
elif edad >= 12 and edad <=15:
  categoria = "infantil"
elif edad >= 16 and edad <=17:
  categoria = "cadete"
elif edad >= 18 and edad <=20:
  categoria = "junior"
else:
  categoria = "senior"
  
print("Tu edad es de",edad,"años y tu categoría es: ",categoria)  

if edad > 40:
  print("Veterano con experiencia en la cancha")
  
  
  
  
  

```

## 4.-Conclusión breve

Como hemos podido ver, las instrucciones condicionales ponen en manos del programador el poder de no ejecutar todo el codigo de forma lineal, sino de poder controlar qué partes se ejecutan y cuándo lo hacen

# Lo que se entrega al final:


Las estructuras de control de selección nos permiten ejecutar diferentes bloques de código de forma condicional, es decir, la ejecución de esos bloques está supeditada a la validación de una expresión.

Nos sirve para elegir qué partes de un programa se activan y cuales permanecen sin ejecutarse.

Cuando introducimos una condicion, utilizamos, en primer lugar, la cláusula if (si condicional)

Escribiremos de la siguiente forma:

```
if condicion:
  codigo a ejecutar
```
El código solo se ejecutará si la validación de la condición resulta ser cierta

Además tenemos la posibilidad de ejecutar código en el caso falso, mediante la claúsula else

Ejemplo:
```
if condicion:
  codigo que se ejecuta en el caso verdadero
else:
  codigo que se ejecuta en el caso falso
```

(explicar también elif)


Para ilustrar mejor este concepto, a continuación se muestra un ejercicio en el que en primer lugar se le pide la edad al usuario, y se le clasifica, en categorías de baloncesto, según su edad

```
# Docstring
''' 
  Programa clasificador de baloncesto
  v0.1 Jose Vicente Carratala
  Este programa clasifica categorías por edades
'''

# Importaciones
# Este programa no requiere importaciones

# Declaración de variables globales
# Inicializamos las variables con valores vacíos

edad = 0
categoria = ""

# Funciones/clases
# En este programa no hay funciones o clases

# Función principal

edad = input("Introduce tu edad: ")
edad = int(edad) # Convierto la edad en un entero
if edad < 8:
  categoria = "pre-mini"
elif edad >= 8 and edad <= 11:
  categoria = "mini"
elif edad >= 12 and edad <=15:
  categoria = "infantil"
elif edad >= 16 and edad <=17:
  categoria = "cadete"
elif edad >= 18 and edad <=20:
  categoria = "junior"
else:
  categoria = "senior"
  
print("Tu edad es de",edad,"años y tu categoría es: ",categoria)  

if edad > 40:
  print("Veterano con experiencia en la cancha")
  
  
  
  
  

```

Como hemos podido ver, las instrucciones condicionales ponen en manos del programador el poder de no ejecutar todo el codigo de forma lineal, sino de poder controlar qué partes se ejecutan y cuándo lo hacen










