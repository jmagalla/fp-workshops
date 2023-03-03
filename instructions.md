# Juego de disparos 

## Objetivo

Implementar un programa para simular un juego de disparos de tiro al blanco.
Descripción


Hay un solo jugador y este cuenta con 30 disparos. El jugador debe realizar los disparos con el objetivo de matar a 6 patos. Cada pato tiene un número de vidas distintas, de manera que, si el jugador acierta a un pato, su número de vidas disminuye. 

1. Genere una lista de 6 números aleatorios diferentes entre 1 y 6, que representará a los 6 patos y su número de vidas. Por ejemplo, para la lista `[3, 5, 4, 2, 1, 6]`, el pato número 1 tiene 3 vidas, el pato número 2 tiene 5 vidas, el pato 3 tiene 4, y así sucesivamente.

2. El jugador deberá ingresar por teclado la posición del pato al que va a disparar. Si el pato tiene un número de vidas mayor a 0, el número de vida para ese pato se disminuye, caso contrario se pierde un disparo. Si el número de vidas de un pato llega a cero se habrá eliminado un pato.

3. En cada disparo, el programa debe mostrarle al jugador cuántos tiros le restan y cuántos patos, y el total de vidas de los patos.

El juego termina cuando el jugador ya no tenga más disparos o cuando haya eliminado todos los patos. 

Al final del juego, el programa debe mostrar cuántos patos eliminó en total.
Validaciones 
Se debe validar que el jugador ingrese una posición válida.
Entregables
Subir 1 archivo .py que incluya lo solicitado en el taller
