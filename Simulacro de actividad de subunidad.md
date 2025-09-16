# Recibís un enunciado

Ejercicio propuesto (estructuras condicionales - tema: plantas):

Crea un programa en JavaScript que, dado un número que representa la altura de una planta en centímetros, muestre un mensaje en pantalla indicando en qué etapa de crecimiento se encuentra:

Si la planta mide menos de 10 cm → mostrar "La planta es un brote".

Si mide entre 10 y 30 cm → mostrar "La planta es joven".

Si mide entre 30 y 100 cm → mostrar "La planta está en su etapa adulta".

Si mide más de 100 cm → mostrar "La planta es un árbol grande".

# Analizo antes el problema

-variable de altura_planta
-if menor que 10 dice la planta es un brote
-if mayor que 10 y menor que 30 la planta es joven
-if mayor que 30 y menor que 100 la planta es adulta
-en caso contrario, la planta es un arbol grande

# Código del ejercicio

```
<script>
  /* 
    Programa calculadora de plantas
    v0.1 Jose Vicente Carratala
    Este programa clasifica a las plantas según su altura
  */
  
  // En este caso no hay librerías que importar
  
  // Declaro variables del programa
  var altura_planta;
  var etapa_crecimiento;
  
  // Aqui vendrían las funciones o clases
  
  // Método principal
  
    // Introduzco datos
    altura_planta = prompt("Dime la altura de la planta");
    // Realizo cálculos
    if(altura_planta < 10){
      etapa_crecimiento = "La planta es un brote";
    }else if(altura_planta >= 10 && altura_planta < 30){
      etapa_crecimiento = "La planta es un brote";
    }else if(altura_planta >= 30 && altura_planta < 100){
      etapa_crecimiento = "La planta está en su etapa adulta";
    }else{
      etapa_crecimiento = "La planta es un árbol grande";
    }
    // Ofrezco resultados
    document.write(etapa_crecimiento);
    
</script>
```

# Rúbrica de evaluación

## 1.-Introducción breve y contextualización - 25% de la nota del ejercicio

Gracias a las estructuras de control condicional, podemos elegir los bloques de código que ejecutamos en función de la validación de una expresión.

Esto nos permte un mayor control sobre la ejecución de los programas que creamos.

## 2.-Desarrollo detallado y preciso - 25% de la nota del ejercicio

El comienzo de una estructura de control condicional se ejecuta utilizando la palabra reservada if

A continuación, entre paréntesis, debemos introducir la condición a validar

Por último, entre llaves introducimos el código que se ejecutara solo en el caso de que la expresión resulte ser verdadera.

Por ejemplo

```
if(edad > 30){
  document.write('Ya no eres eres joven')
}
```

También existe una clausula llamada else que podemos ejecutar para atrapar aquellos casos que sean falsos.

Lo podemos ver en el siguiente ejemplo:

```
if(edad > 30){
  document.write('Ya no eres eres joven')
}
else{
  document.write('Sí que eres joven')
}
```

(seguiría explicando por ejemplo el caso else if)

## 3.-Aplicación práctica - 25% de la nota del ejercicio

Para mostrar este concepto de forma consistente, a continuación se presenta un ejercicio completo, que le pide al usuario introducir una altura de una planta, y clasifica a la planta en base al uso de estructuras condicionales

```
<script>
  /* 
    Programa calculadora de plantas
    v0.1 Jose Vicente Carratala
    Este programa clasifica a las plantas según su altura
  */
  
  // En este caso no hay librerías que importar
  
  // Declaro variables del programa
  var altura_planta;
  var etapa_crecimiento;
  
  // Aqui vendrían las funciones o clases
  
  // Método principal
  
    // Introduzco datos
    altura_planta = prompt("Dime la altura de la planta");
    // Realizo cálculos
    if(altura_planta < 10){
      etapa_crecimiento = "La planta es un brote";
    }else if(altura_planta >= 10 && altura_planta < 30){
      etapa_crecimiento = "La planta es un brote";
    }else if(altura_planta >= 30 && altura_planta < 100){
      etapa_crecimiento = "La planta está en su etapa adulta";
    }else{
      etapa_crecimiento = "La planta es un árbol grande";
    }
    // Ofrezco resultados
    document.write(etapa_crecimiento);
    
</script>
```


## 4.-Conclusión breve - 25% de la nota del ejercicio

Las estructuras de control nos ofrecen un nivel superior de ajuste sobre cómo se ejecutan nuestros programas.

Para utilizar estructuras de control debemos antes haber comprendido cómo utilizar variables u operadores de comparación, así como salidas y entradas.

# Limpiar el código:



Gracias a las estructuras de control condicional, podemos elegir los bloques de código que ejecutamos en función de la validación de una expresión.

Esto nos permte un mayor control sobre la ejecución de los programas que creamos.



El comienzo de una estructura de control condicional se ejecuta utilizando la palabra reservada if

A continuación, entre paréntesis, debemos introducir la condición a validar

Por último, entre llaves introducimos el código que se ejecutara solo en el caso de que la expresión resulte ser verdadera.

Por ejemplo

```
if(edad > 30){
  document.write('Ya no eres eres joven')
}
```

También existe una clausula llamada else que podemos ejecutar para atrapar aquellos casos que sean falsos.

Lo podemos ver en el siguiente ejemplo:

```
if(edad > 30){
  document.write('Ya no eres eres joven')
}
else{
  document.write('Sí que eres joven')
}
```

(seguiría explicando por ejemplo el caso else if)



Para mostrar este concepto de forma consistente, a continuación se presenta un ejercicio completo, que le pide al usuario introducir una altura de una planta, y clasifica a la planta en base al uso de estructuras condicionales

```
<script>
  /* 
    Programa calculadora de plantas
    v0.1 Jose Vicente Carratala
    Este programa clasifica a las plantas según su altura
  */
  
  // En este caso no hay librerías que importar
  
  // Declaro variables del programa
  var altura_planta;
  var etapa_crecimiento;
  
  // Aqui vendrían las funciones o clases
  
  // Método principal
  
    // Introduzco datos
    altura_planta = prompt("Dime la altura de la planta");
    // Realizo cálculos
    if(altura_planta < 10){
      etapa_crecimiento = "La planta es un brote";
    }else if(altura_planta >= 10 && altura_planta < 30){
      etapa_crecimiento = "La planta es un brote";
    }else if(altura_planta >= 30 && altura_planta < 100){
      etapa_crecimiento = "La planta está en su etapa adulta";
    }else{
      etapa_crecimiento = "La planta es un árbol grande";
    }
    // Ofrezco resultados
    document.write(etapa_crecimiento);
    
</script>
```


Las estructuras de control nos ofrecen un nivel superior de ajuste sobre cómo se ejecutan nuestros programas.

Para utilizar estructuras de control debemos antes haber comprendido cómo utilizar variables u operadores de comparación, así como salidas y entradas.


