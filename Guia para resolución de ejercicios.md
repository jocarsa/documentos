
Ejemplo:

Un posible enunciado para el ejercicio:
- Un establo tiene varias cuadras y cada cuadra puede albergar 3 caballos.
- El usuario introduce el número total de caballos que quiere guardar.
- El programa debe calcular cuántas cuadras completas necesita, redondeando hacia arriba aunque la última no se llene.

# Resolución del ejercicio:
Paso 1:
Resolvéis el ejercicio en cuanto a código en el lenguaje que sea.
Ejemplo de ejercicio resuelto:

```
''' 
    Calculadora de cuadras
    v0.1 (c) 2025 Jose Vicente Carratalá
    Programa que calcula número de cuadras a partir de los caballos
'''

import math as matematicas

# Datos de inicio
caballos = 0
cuadras = 0
caballos_por_cuadra = 0

# Entrada de información
caballos_por_cuadra = int(input("Introduce el número de caballos por cuadra: "))
caballos = int(input("Introduce el número de caballos: "))

# Realización de cálculos
cuadras = caballos / caballos_por_cuadra
redondeoalza = matematicas.ceil(cuadras)

# Salida de resultados
print("Si tienes",caballos,"caballos")
print("Y te caben tres caballos por cuadra")
print("En ese caso necesitas",redondeoalza,"cuadras")


```

# Introducción del ejercicio según la rúbrica de evaluación:

## Introducción breve y contextualización - 25% de la nota del ejercicio
Vamos a realizar una demostración del uso de la librería matemática para realizar un redondeo al alza. La librería matemática sirve para tener acceso a realizar operaciones más avanzadas de las que permite el núcleo de Python.

## Desarrollo detallado y preciso - 25% de la nota del ejercicio
En Python, encontramos una librería llamada math, que tiene una serie de propiedades y métodos. Para usar esta librería, en primer lugar debemos importarla dentro de un programa, por ejemplo de esta forma:
```
import math
```

Hay que notar que es una buena práctica en Python trabajar con espacios de nombres (namespaces), por lo tanto sería más recomendable importar de esta forma:

```
import math as matematicas
```

Un pequeño ejemplo de uso de la librería sería este:

```
import math as matematicas
print(matematicas.pi)
```
El ejemplo anterior muestra el valor de la variable PI

## Aplicación práctica - 25% de la nota del ejercicio

A continuación se muestra un ejemplo de código completo en el que se ilustra el uso de la librería matemática

```
''' 
    Calculadora de cuadras
    v0.1 (c) 2025 Jose Vicente Carratalá
    Programa que calcula número de cuadras a partir de los caballos
'''

import math as matematicas

# Datos de inicio
caballos = 0
cuadras = 0
caballos_por_cuadra = 0

# Entrada de información
caballos_por_cuadra = int(input("Introduce el número de caballos por cuadra: "))
caballos = int(input("Introduce el número de caballos: "))

# Realización de cálculos
cuadras = caballos / caballos_por_cuadra
redondeoalza = matematicas.ceil(cuadras)

# Salida de resultados
print("Si tienes",caballos,"caballos")
print("Y te caben tres caballos por cuadra")
print("En ese caso necesitas",redondeoalza,"cuadras")


```

*Notas:*

Hay que tener cuidado en Python cuando introducimos un valor con input, porque por defecto se convierte en cadena de caracteres - usaremos conversión de tipo para evitar el error.

Hay que tener en cuenta que debemos cerrar tantos paréntesis como hayamos abierto

## Conclusión breve - 25% de la nota del ejercicio

Como hemos visto, la librería matemática nos va a ayudar a realizar operaciones complejas de forma sencilla y predecible.

Más adelante, podremos comprobar la utilidad de la librería matemática en programas más grandes.

# Entrega completa del ejercicio:

Por lo tanto, lo que entregaréis en la aplicación de subida, será lo siguiente (la suma de los cuatro apartados:

---
Vamos a realizar una demostración del uso de la librería matemática para realizar un redondeo al alza. La librería matemática sirve para tener acceso a realizar operaciones más avanzadas de las que permite el núcleo de Python.

En Python, encontramos una librería llamada math, que tiene una serie de propiedades y métodos. Para usar esta librería, en primer lugar debemos importarla dentro de un programa, por ejemplo de esta forma:
```
import math
```

Hay que notar que es una buena práctica en Python trabajar con espacios de nombres (namespaces), por lo tanto sería más recomendable importar de esta forma:

```
import math as matematicas
```

Un pequeño ejemplo de uso de la librería sería este:

```
import math as matematicas
print(matematicas.pi)
```
El ejemplo anterior muestra el valor de la variable PI

A continuación se muestra un ejemplo de código completo en el que se ilustra el uso de la librería matemática

```
''' 
    Calculadora de cuadras
    v0.1 (c) 2025 Jose Vicente Carratalá
    Programa que calcula número de cuadras a partir de los caballos
'''

import math as matematicas

# Datos de inicio
caballos = 0
cuadras = 0
caballos_por_cuadra = 0

# Entrada de información
caballos_por_cuadra = int(input("Introduce el número de caballos por cuadra: "))
caballos = int(input("Introduce el número de caballos: "))

# Realización de cálculos
cuadras = caballos / caballos_por_cuadra
redondeoalza = matematicas.ceil(cuadras)

# Salida de resultados
print("Si tienes",caballos,"caballos")
print("Y te caben tres caballos por cuadra")
print("En ese caso necesitas",redondeoalza,"cuadras")


```

*Notas:*

Hay que tener cuidado en Python cuando introducimos un valor con input, porque por defecto se convierte en cadena de caracteres - usaremos conversión de tipo para evitar el error.

Hay que tener en cuenta que debemos cerrar tantos paréntesis como hayamos abierto

Como hemos visto, la librería matemática nos va a ayudar a realizar operaciones complejas de forma sencilla y predecible.

Más adelante, podremos comprobar la utilidad de la librería matemática en programas más grandes.


---



