# Recibo un enunciado de actividad

```
Actividad: Objetos deportivos en JavaScript

Vas a practicar el uso de objetos ya existentes en JavaScript aplicados al deporte:

Usa el objeto Date para obtener la fecha y hora actuales de un partido y muéstralas por consola.

Usa el objeto Math para:

Calcular una puntuación aleatoria de un jugador (por ejemplo, entre 0 y 10 puntos).


Muestra en consola frases como:

"El partido comenzó el día ... a las ..."

"El jugador ha conseguido X puntos."
```

# Análisis

Analizo lo que pide el ejercicio y planeo el esquema del programa según el siguiente patron:

1. Docstring
2. Importacion de librerías o archivos
3. Variables globales
4. Funciones/clases
5. Función principal

# Realizo el código del ejercicio

```
<script>
  /*
    Programa objetos deportivos
    v0.1 Jose Vicente Carratala
    Programa que usa la librería de fechas y la librería matemática
  */

  var fecha;
  var puntuacion;

  fecha = new Date("2025-09-13 21:00:00");
  console.log(fecha);
  puntuacion = Math.random();
  console.log(puntuacion*10)
  
  console.log("El partido comenzó el día",fecha.getFullYear(),fecha.getMonth()+1,fecha.getDate()," a las ",fecha.getHours(),fecha.getMinutes(),fecha.getSeconds());
  console.log("El jugador ha conseguido",puntuacion*10,"puntos")
</script>
```

# Consulto la rúbrica de evaluación y voy rellenando poco a poco

## 1.-Introducción breve y contextualización - 25% de la nota del ejercicio

En este ejercicio vamos a desarrollar un ejemplo de instanciación de objetos. Los objetos son contenedores de funcionalidades que nos permiten automatizar una gran cantidad de tareas gracias a código ya preparado.

En el contexto de la programación informática los objetos preconstruidos me ayudan a ser más productivo porque no tengo que programar yo todo lo que ya está programado en el objeto.

## 2.-Desarrollo detallado y preciso - 25% de la nota del ejercicio

Las clases son plantillas que permiten ser instanciadas en forma de objetos. 

Cuando realizamos una instancia, creamos una nueva copia de la clase dentro de un identificador.

Por ejemplo, si queremos crear una instancia del objeto date, haremos algo como:

```
var fecha = new Date("2025-09-13 21:00:00");
```

## 3.-Aplicación práctica - 25% de la nota del ejercicio

Para demostrar claramente este concepto, a continuación podemos encontrar un programa informático completo que trabaja con el concepto de instancias:

```
<script>
  /*
    Programa objetos deportivos
    v0.1 Jose Vicente Carratala
    Programa que usa la librería de fechas y la librería matemática
  */

  var fecha;
  var puntuacion;

  fecha = new Date("2025-09-13 21:00:00");
  console.log(fecha);
  puntuacion = Math.random();
  console.log(puntuacion*10)
  
  console.log("El partido comenzó el día",fecha.getFullYear(),fecha.getMonth()+1,fecha.getDate()," a las ",fecha.getHours(),fecha.getMinutes(),fecha.getSeconds());
  console.log("El jugador ha conseguido",puntuacion*10,"puntos")
</script>
```

## 4.-Conclusión breve - 25% de la nota del ejercicio

Trabajar con instancias de objetos es sencillo y conveniente, puesto que nos ahorran tener que crear manualmente nuestros propios objetos.

De todas formas, más adelante veremos cómo crear nuestras propias clases y objetos para tener más control.

# Contenido final del ejercicio que entregas:

Es lo mismo que en la unidad anterior, pero  uniendo los bloques y quitando los títulos

---

En este ejercicio vamos a desarrollar un ejemplo de instanciación de objetos. Los objetos son contenedores de funcionalidades que nos permiten automatizar una gran cantidad de tareas gracias a código ya preparado.

En el contexto de la programación informática los objetos preconstruidos me ayudan a ser más productivo porque no tengo que programar yo todo lo que ya está programado en el objeto.

Las clases son plantillas que permiten ser instanciadas en forma de objetos. 

Cuando realizamos una instancia, creamos una nueva copia de la clase dentro de un identificador.

Por ejemplo, si queremos crear una instancia del objeto date, haremos algo como:

```
var fecha = new Date("2025-09-13 21:00:00");
```

Para demostrar claramente este concepto, a continuación podemos encontrar un programa informático completo que trabaja con el concepto de instancias:

```
<script>
  /*
    Programa objetos deportivos
    v0.1 Jose Vicente Carratala
    Programa que usa la librería de fechas y la librería matemática
  */

  var fecha;
  var puntuacion;

  fecha = new Date("2025-09-13 21:00:00");
  console.log(fecha);
  puntuacion = Math.random();
  console.log(puntuacion*10)
  
  console.log("El partido comenzó el día",fecha.getFullYear(),fecha.getMonth()+1,fecha.getDate()," a las ",fecha.getHours(),fecha.getMinutes(),fecha.getSeconds());
  console.log("El jugador ha conseguido",puntuacion*10,"puntos")
</script>
```

Trabajar con instancias de objetos es sencillo y conveniente, puesto que nos ahorran tener que crear manualmente nuestros propios objetos.

De todas formas, más adelante veremos cómo crear nuestras propias clases y objetos para tener más control.

---
