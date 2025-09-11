
Ejemplo:

Un posible enunciado para el ejercicio:
- Un establo tiene varias cuadras y cada cuadra puede albergar 3 caballos.
- El usuario introduce el número total de caballos que quiere guardar.
- El programa debe calcular cuántas cuadras completas necesita, redondeando hacia arriba aunque la última no se llene.

Resolución del ejercicio:
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

