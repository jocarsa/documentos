# Guía para entregar las actividades correctamente

## Recibís el enunciado del ejercicio (previsiblemente adaptado a vuestro perfil)
Ejemplo:
-Crea un programa en JavaScript que represente el marcador de un partido de fútbol.
-Declara tres variables: una para los goles del equipo local, otra para los goles del equipo visitante y otra para el total de goles.
-Asigna a las variables de los equipos un número cualquiera de goles.
-Calcula el total de goles sumando los dos valores.
-Muestra por pantalla con document.write los goles de cada equipo y el total del partido.

## En primer lugar os vais al IDE que queráis, y resolvéis el ejercicio (y que funcione)

```
<script>
	/*
		Programa marcadores de futbol
		(c) 2025 Jose Vicente Carratala
		Este programa calcula el total de goles metidos en un partido
	*/

	var goles_equipo_local = 3;
	var goles_equipo_visitante = 2;
	var goles_totales = goles_equipo_local + goles_equipo_visitante;

	document.write("El equipo local ha marcado ",goles_equipo_local," goles<br>");
	document.write("El equipo visitante ha marcado ",goles_equipo_visitante," goles<br>");
	document.write("El total de goles marcados en el partido es de ",goles_totales ," goles<br>");
	
	
</script>
```
