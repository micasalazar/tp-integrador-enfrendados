# tp-integrador-enfrendados

Enfrendados es un juego de dados de dos jugadores en el que interviene el azar y las matemáticas.
El objetivo general del juego es sumar la mayor cantidad de puntos en un total de tres rondas. La suma de puntaje depende de diferentes situaciones que se pueden dar en el juego y que más adelante se explicarán.
El juego se juega con seis dados de seis caras por cada jugador más dos dados de doce caras que lanzan los jugadores entre ronda y ronda. Una imagen de cómo podría iniciar una partida es la siguiente:


Al comenzar un juego y por única vez deben tirar cada uno un dado. Quien obtenga el valor mayor comienza la partida. En caso de empate se debe repetir la tirada hasta que alguno obtenga el mayor dado.
Luego comienza la partida y el jugador 1 (el primero en tirar) lanza los dos dados de doce caras. Luego de tirar éstos dados deberá tirar los dados de seis caras que tenga en su poder (al comenzar la partida serán seis dados pero luego puede variar). Los dados que cada jugador tiene en su poder los llamaremos dados stock. Y habrá dados stock para el jugador 1 y dados stock para el jugador 2.

Luego de hacer ambos lanzamientos es momento de confiar en el azar y en las destrezas matemáticas ya que los puntajes ocurren de la siguiente manera:

Primero, deberá sumar ambas caras de los dados de doce caras. Esto dará un valor numérico entre 2 y 24. Este resultado de la suma lo llamaremos número objetivo.
Luego deberá seleccionar, del lanzamiento de sus dados stock, los que desee para que al sumar todas sus caras iguale el valor del número objetivo. A la suma de los dados seleccionados por el jugador luego del lanzamiento lo llamaremos suma seleccionada y a los dados seleccionados para ser sumados los llamaremos dados elegidos.

Si ocurre que la suma seleccionada por el jugador es igual al número objetivo entonces se logra una tirada exitosa y ocurren las siguientes situaciones:
El puntaje de esa ronda para el jugador es igual a la suma seleccionada multiplicado por la cantidad de dados elegidos y se suma al total general que viene acumulando en las demás rondas.
El jugador se resta la cantidad de dados elegidos de sus dados stock y se los envía al contrincante aumentando la cantidad de dados stock de este último.

Si además ocurre que el jugador que realiza la tirada exitosa se queda sin dados. Gana automáticamente la partida acumulando diez mil puntos a lo que venía acumulando.

Por el contrario, si en el lanzamiento de la ronda no logra una tirada exitosa. Es decir, no puede realizar ninguna suma correcta entre su lanzamiento de dados stock y el número objetivo. Entonces es el contrario el que le enviará un dado de sus dados stock sólo si tiene una cantidad mayor a uno de dados. De lo contrario no habrá penalidad por no lograr una tirada exitosa.

Luego, será turno del siguiente jugador que deberá tirar con la cantidad de dados stock correspondiente.

La ronda finalizará cuando ambos hayan terminado de hacer su lanzamiento y se procederá a la siguiente ronda hasta que se realicen tres rondas o bien que alguno gane por quedarse sin dados.

Veamos un ejemplo de una tirada de un jugador en una ronda:

Aquí podemos observar que la suma objetivo es 12. Y que el stock de dados del jugador es de 5 dados. El jugador debe sumar las caras de los dados que desee y que sumen entre todos 12. Puede optar por:

Alternativa A: 
Dado1 + Dado2 + Dado3 → 3 + 4 + 5 → 12
ó
Alternativa B:
Dado4 + Dado5 → 6 + 6 → 12

En cualquiera de los dos casos su lanzamiento pasaría a ser una tirada exitosa. Pero, la Alternativa A es más conveniente porque le sumaría 12x3 → 36 puntos y además le enviaría 3 dados al stock de dados del contrincante.
En cambio, la Alternativa B le sumaría 12x2 → 24 puntos y le enviaría 2 dados al stock de dados del contrincante.


Veamos otro ejemplo de tirada de un jugador en una ronda:

Aquí el jugador no tiene muchas alternativas. Ha ocurrido que su lanzamiento no sólo es una tirada exitosa sino que también lo dejará sin dados en su stock de dados. Por lo tanto, automáticamente ganará la partida sumando diez mil puntos a lo que venía acumulando anteriormente.

Siempre puede ocurrir que el jugador luego de un lanzamiento no se de cuenta que tiene una tirada exitosa y, por lo tanto, a pesar de que pueda sumar puntos y enviarle dados al contrincante no lo haga. Esto es una situación del juego y es equivalente a que el jugador no haya obtenido una tirada exitosa. Es decir, debe recibir un dado en castigo con las reglas que se explicaron anteriormente.

El ganador del juego es aquel jugador que se quede sin dados o bien que transcurridas las tres rondas sumó más puntos. Si transcurriendo las rondas, se logra exactamente la misma cantidad de puntos. El partido queda empatado.

Actividad
Se pide desarrollar en C/C++ el juego haciendo uso de un proyecto de Aplicación de Consola.

El juego debe contar con un menú principal con las siguientes opciones:
    _______   ____________  _______   ______  ___ 	____  ____  _____
   / ____/ | / / ____/ __ \/ ____/ | / / __ \/   |  / __ \/ __ \/ ___/
  / __/ /  |/ / /_  / /_/ / __/ /  |/ / / / / /| | / / / / / / /\__ \
 / /___/ /|  / __/ / _, _/ /___/ /|  / /_/ / ___ |/ /_/ / /_/ /___/ /
/_____/_/ |_/_/   /_/ |_/_____/_/ |_/_____/_/  |_/_____/\____//____/


1 - JUGAR
2 - ESTADÍSTICAS
3 - CRÉDITOS
---------------------
0 - SALIR


La opción jugar, debe permitir iniciar un nuevo juego de Enfrendados. Antes de comenzar el juego debe solicitar a los jugadores el nombre.
Luego, el juego debe mostrar la información necesaria para que los usuarios puedan jugarlo. Esto, como mínimo, debe ser: el número de ronda actual, el nombre del jugador que está tirando, la tirada de dados del jugador actual, la tirada de dados objetivo (dados de 12 caras) del jugador actual, el puntaje acumulado de ambos jugadores y la cantidad de dados del stock de cada jugador.
Luego de realizar la tirada de los dados objetivo. Debe mostrar uno al lado de otro los dados del lanzamiento y calcular y mostrar la suma objetivo.
Luego de realizar la tirada de los dados del stock del jugador. Debe mostrar uno al lado de otro los dados del lanzamiento y preguntarle al usuario qué número de dados desea seleccionar. Al ir seleccionando cada dado, debe automáticamente sumarlos y compararlos con la suma objetivo. En el momento que ambas sumas sean iguales, finaliza la ronda.
El juego no contemplará la posibilidad de que el usuario se equivoque. Dado seleccionado es un dado sumado. No existe la posibilidad de deshacer la selección de un dado. Si por alguna razón el jugador no puede lograr una suma que le otorgue una tirada exitosa. Puede ingresar un número de dado 0 para que finalice una ronda como no exitosa.
Cuando finaliza una ronda y antes de continuar con el lanzamiento del contrincante (si corresponde), debe mostrarse una pantalla que explique lo sucedido. 


Esto es:
Si es una tirada exitosa indicarlo además de mostrar cuál era la suma objetivo, mostrar las caras de los dados elegidos y la suma total de puntos e indicar cuántos dados se le envían al contrincante.
Si no es una tirada exitosa indicarlo además de mostrar cuántos dados recibe de su contrincante (puede ser uno o cero).
También debe contemplar que el jugador haya logrado una tirada exitosa que además finalice el juego. Entonces debe indicarlo particularmente y terminar la partida.

La opción estadísticas, debe mostrar el nombre del jugador que haya obtenido el mayor puntaje y dicho puntaje.

La opción créditos, debe mostrar los apellidos, nombres y legajos de los integrantes del equipo. Así como también el nombre del equipo.

La opción salir, debe salir del juego previa confirmación del usuario.

Créditos
Íconos obtenidos de Freepik y logo hecho en Logo Maker.
Juego inventado por Angel Simón. Levemente inspirado en el juego Mafia.
Anexo

Vocabulario

Término
Descripción
Dados stock
Son los dados de seis caras que tiene cada jugador. Se usan en cada ronda y su cantidad puede cambiar durante el juego.
Dados objetivo
Son dos dados de doce caras que se tiran al inicio de cada turno y definen el número objetivo. Son comunes para ambos jugadores.
Número objetivo
Es la suma de las caras de los dos dados objetivo. El jugador debe intentar igualar este número con la suma de algunos dados de su stock.
Dados elegidos
Son los dados del stock que el jugador selecciona en su turno para intentar igualar el número objetivo.
Suma seleccionada
Es la suma de los valores de los dados elegidos. Si esta suma es igual al número objetivo, la tirada es exitosa.
Tirada exitosa
Ocurre cuando la suma seleccionada es igual al número objetivo. El jugador gana puntos y transfiere los dados usados al contrincante.
Puntaje de ronda
Se calcula como: número objetivo × cantidad de dados elegidos (si la tirada es exitosa). Se suma al puntaje total del jugador.
Transferencia de dados
En una tirada exitosa, el jugador transfiere al oponente los dados elegidos. Si falla, puede recibir un dado del rival si este tiene más de uno.
Victoria automática
Si un jugador logra una tirada exitosa y se queda sin dados en su stock, gana automáticamente sumando 10.000 puntos.
Ronda
Cada jugador realiza una tirada por ronda. El juego dura tres rondas, salvo que alguien gane antes por quedarse sin dados.
Empate
Si ambos jugadores tienen el mismo puntaje al finalizar las tres rondas, el juego termina empatado.



Simulación de una partida
🎲 Inicio del juego
Angel y María tiran un dado de 6 caras para ver quién empieza:
Angel tira: 4
María tira: 2
👉 Angel comienza la partida.

🔁 Ronda 1
🔹 Turno de Angel
Dados objetivo (d12): 7 + 5 = 12 (número objetivo)
Stock actual: 6 dados (valores): [3, 4, 2, 6, 1, 5]
Combinación elegida: 3 + 4 + 5 = 12 ✅
Dados elegidos: 3 (3 dados)
Puntos: 12 × 3 = 36
Transfiere 3 dados a María
➡️ Angel: 3 dados restantes, 36 pts
➡️ María: 9 dados (recibió 3)

🔹 Turno de María
Dados objetivo (d12): 6 + 8 = 14 (número objetivo)
Stock actual: 9 dados (valores): [4, 6, 2, 1, 3, 5, 6, 2, 4]
Combinación elegida: 6 + 4 + 4 = 14 ✅
Dados elegidos: 3
Puntos: 14 × 3 = 42
Transfiere 3 dados a Angel
➡️ María: 6 dados, 42 pts
➡️ Angel: 6 dados (recuperó 3)

🔁 Ronda 2
🔹 Turno de Angel
Dados objetivo: 9 + 7 = 16
Stock: [2, 5, 6, 3, 4, 1]
Combinación elegida: 5 + 6 + 4 + 1 = 16 ✅
Dados elegidos: 4
Puntos: 16 × 4 = 64
Transfiere 4 dados a María
➡️ Angel: 2 dados, 100 pts
➡️ María: 10 dados

🔹 Turno de María
Dados objetivo: 3 + 10 = 13
Stock: [2, 5, 1, 6, 4, 2, 3, 5, 6, 2]
Combinación elegida: 6 + 5 + 2 = 13 ✅
Dados elegidos: 3
Puntos: 13 × 3 = 39
Transfiere 3 dados a Angel
➡️ María: 7 dados, 81 pts
➡️ Angel: 5 dados


🔁 Ronda 3
🔹 Turno de Angel
Dados objetivo: 6 + 6 = 12
Stock: [2, 6, 3, 5, 4]
Combinación elegida: 3 + 5 + 4 = 12 ✅
Dados elegidos: 3
Puntos: 12 × 3 = 36
Transfiere 3 dados a María
➡️ Angel: 2 dados, 136 pts
➡️ María: 10 dados

🔹 Turno de María
Dados objetivo: 8 + 4 = 12
Stock: [1, 6, 2, 3, 5, 4, 6, 3, 2, 1]
Combinación elegida: 6 + 4 + 2 = 12 ✅
Dados elegidos: 3
Puntos: 12 × 3 = 36
Transfiere 3 dados a Angel
➡️ María: 7 dados, 117 pts
➡️ Angel: 5 dados

Resultados finales
Jugador
Puntos
Dados stock
Angel
136
5 dados
María
117
7 dados


Nadie ganó automáticamente, así que el ganador de la partida es Angel con 136 puntos.
Consideraciones importantes
El programa debe estar realizado en C++ con un proyecto de aplicación de consola.
Debe disponer de un menú principal con las opciones descritas en el apartado de "Actividad".
Durante el transcurso del juego se debe mostrar los nombres de los jugadores (dos jugadores) y los puntos totales que viene acumulando.
Debe quedar claro durante el transcurso del juego cuáles son los dados del jugador que está jugando. Debe quedar claro al momento de seleccionar los dados cómo se realiza la selección de los mismos. Un ejemplo podría ser:

Donde cada dado tiene un código o índice que los identifica ordinalmente. Entonces si el usuario decide seleccionar el dado 2, el dado 4 y el dado 5 para la sumatoria. Sumarían los valores: 3 + 3 + 5 → 11

El desarrollo debe hacer uso de funciones y vectores.
No se aceptará el uso de variables de ámbito global ni tampoco la instrucción goto.
No es obligatorio que se dibujen los dados por pantalla. Se considera suficiente que se muestre el valor numérico de cada dado.
El lanzamiento de los dados debe ser aleatorio haciendo uso de las funciones srand y rand.
Debe quedar claro quien fue el ganador de la partida transcurridas las tres rondas o si fue empate.
En estadísticas se debe mostrar el nombre del jugador que haya obtenido el mayor puntaje entre todas las veces que se haya jugado una partida de Enfrendados. Si el programa se cierra el puntaje se restablecerá a 0.

