# Workshop 1: Strings, Lists and Functions 

## Ejercicio 1

Escriba una función de nombre `mezclar(cad1, cad2)` que recibe dos palabras. La función debe mezclar las dos palabras de la siguiente manera:

  1. Elegir un caracter al azar en la palabra 1
  2. A partir del caracter elegido recortar hasta el final de la palabra 
  3. Hacer lo mismo para la palabra 2
  4. Concatene ambas palabras recortadas y retornar esta como la mezcla.

A continuación un ejemplo de lo que retornaría la función, si se elige al azar la `e` de la primera palabra y luego la `d` de la segunda.
```
mezcla("maletas", "pesadisimo") -> "etasdisimo"
```

## Ejercicio 2
Escriba una función de nombre `max_pal(lista)` que recibe una lista de 3 cadenas y retorna la cadena con la longitud más larga. 

### Instrucciones

1. Cree una lista con las longitudes de cada cadena
2. Use max para obtener la longitud más larga
3. Considere ambas listas como listas paralelas, y con la posición de la longitud más larga, obtener la cadenas más larga
4. Retornar la cadenas más larga

No use condicionales, no use lazos, el programa debe ser escrito usando solo funciones de listas. 

```
max_pal(["espol", "milenium", "trono"]) -> milenium
max_pal(["pera", "banana", "escalofrio"]) -> escalofrio
```

