# u67: Actividad: Desafío Pokemon 
## Objetivo

Implementar un programa que utilice funciones, y colecciones para el cálculo del ataque efectivo de un pokemon frente a otro y determinar el ganador del ataque.

## Descripción

Los datos de los pokemons están almacenados en el archivo de nombre `POKEDEX.txt`, cada línea de este archivo contiene el registro de un pokemon con los siguientes atributos:  identificador (code), nombre del pokemon (pokemon), tipo de pokemon (type), y nivel de ataque (atak). El archivo también contiene una cabecera.
```
CODE|POKEMON|TYPE|ATK
001|Bulbasaur|Grass|49
002|Ivysaur|Grass|62
003|Venusaur|Grass|100
004|Charmander|Fire|52
005|Charmeleon|Fire|64
006|Charizard|Fire|104
```

El archivo de nombre `TIPOSPOKEMONS.txt` contiene todos los tipos de pokemons y cómo afecta su ataque sobre otro tipo. Cada línea representa los siguientes 4 atributos:

    1. tipo de pokemon (type),
    2. listado de tipos en los que un ataque se duplica (lista super),
    3. listado de tipos en los que un ataque se disminuye por la mitad (lista half), y
    4. listado de tipos en los que un ataque se anula (lista zero)

Ejemplo del archivo de texto
```
DARK TYPE|GHOST/PSYCHIC|DARK/FIGHTING/STEEL|
DRAGON TYPE|DRAGON|STEEL|FAIRY
NORMAL TYPE||ROCK/STEEL|GHOST
```

Como se observa en el ejemplo, cada atributo está separado por la barra (|) y cada tipo de pokemon están separados por el slash (/). 

En el archivo de ejemplo, la primera línea define que un pokemon tipo `DARK` que duplica su ataque frente a pokemones tipo `GHOST`, `PSYCHICK`, y que disminuye su ataque por lo mitad frente a pokemones tipo `DARK`, `FIGHTING` y `STEEL`. El cuarto atributo está vacío, por lo que no hay otros tipos con los que su ataque se haga cero.

## Instrucciones

Usted debe realizar las siguientes tareas: 

1.- Implementar la función `cargarPokedex(nombreArchivo)`,  que retorna un diccionario con los datos de los pokemones con la siguiente estructura: use como clave el atributo code, como valor una lista de 3 elementos, nombre del pokemon, tipo y ataque. 
Ejemplo: 
```
{ 1:['Bulbasaur','Grass',49], 2:['Ivysaur','Grass',62],...,8:['Wartortle', 'Water',63] } 
```   
2.- Implementar la función `cargarTipos(nombreArchivo)`, que retorna un diccionario con los tipos de pokemones con la siguiente estructura: como clave el tipo de pokemon y como valor una lista que contiene tres listas, la primera la lista super, la segunda la lista half,  y la tercera lista zero. Ejemplo: para los tipos `DARK`, `DRAGON` y `NORMAL` del archivo el diccionario tendría la siguiente estructura: 
```
{'DARK': [['GHOST', 'PSYCHIC'], ['DARK', 'FIGHTING', 'STEEL'],[]], 
'DRAGON': [['DRAGON'], ['STEEL'], ['FAIRY']],
'NORMAL': [[], ['ROCK','STEEL'], ['GHOST']], ... }
```
3.- Implementar una función `seleccionarPokemones(pokedex)`, que recibe un diccionario como el creado por la función `cargarPokedex` y retorna 2 códigos diferentes de pokemones seleccionados al azar en una tupla. 

4.- Implementar una función `batallaPokemon(idpok1, idpok2, pokedex, dicTiposPok)`, que determina el vencedor de una batalla pokemon, según las reglas descritas en los atributos del archivo `tipospokemones.txt`. Donde pokedex es un diccionario como el que devuelve la función 1 y `dicTiposPok` un diccionario como el que devuelve la función 2. La función retorna el id del vencedor o `0` si hay un empate.

A continuación un ejemplo de la llamada a esta función: 
```
batallaPokemon(1,8,pokedex,dicTiposPokemon)
```
Ejemplo de la salida por pantalla que se realiza en la llamada a esta función.
```
Pokemon con codigo 1: [Bulbasaur,Grass,49] con tipo GRASS
Enfrenta a:
Pokemon con codigo 8: [Wartortle,Water,63] con tipo WATER
```
Como WATER (tipo del oponente) se encuentra en la lista SUPER de GRASS, el ataque de Bulbasaur se multiplica por 2.

```
Ataque efectivo de Bulbasaur = 49 * 2 = 98
```
Para calcular el ataque de 
'WATER': [['FIRE', 'GROUND', 'ROCK'], ['DRAGON', 'GRASS', 'WATER'], ['']]
Grass (tipo del oponente) se encuentra en la lista HALF, por lo tanto el ataque de Bulbasaur se multiplica por 0.5
Ataque = 63 * 0.5 = 31.5

98 >31.5 -> Vencedor: 1 – Bulbasaur
Entregables
Subir el archivo .py que incluya lo solicitado en el taller. 
