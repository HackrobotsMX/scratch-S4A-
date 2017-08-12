# Scratch-S4A-

#### Objetivo:

Simulación de un semáforo, por medio de bloques la programación e implementarlo con Arduino.

#### Material:

* Computadora personal.
* [Scratch](https://scratch.mit.edu/scratch_1.4/)
* [S4A, Interfaz de Scratch For Arduino](http://s4a.cat/index_es.html)
* [Firmware para S4A](http://vps34736.ovh.net/S4A/S4AFirmware16.ino) (Importante: Guardarlo en un bloc de notas con extensión .ino)
* LEDS: rojo, verde y amarillo
* Resistencias de 220 Ohms
* Cable Dupont
* Protoboard (Tablilla para pruebas de circuitos electrónicos)
* Arduino Uno

#### Procedimiento:

1. El firmware que descargamos con extensión .ino, lo abrimos con el programa de Arduino. Seguido damos clic en el icono de la palomita (Verificar).

2. Una vez verificado que el programa no tenga errores. El archivo lo cargaremos a la placa del Arduino. Previo a la carga verificamos que la placa sea reconocido con el programa de la siguiente forma:
Damos clic en la pestaña "Herramientas", seguido elegimos el "Puerto" y seleccionamos el que diga "COMX(Arduino/Geniuno Uno)" donde la X nos representan un numero de puerto. Como se muestra en la siguiente imagen.

3. Descargamos el programa a la placa de Arduino, dándole clic en el icono de la flecha (Cargar).

4. Una vez descargado el programa a la placa de Arduino, cerramos el programa de Arduino y procedemos a abrir a aplicación de Scratch For Arduino  (S4A).

5. Cuando se abre el programa nos mostrara la leyenda de "Buscando Placa", una vez que la detecta, se quitara el mensaje y además en la placa de Arduino veremos dos LEDs (en la placa los identificamos como Rx y Tx, como se muestra en la imagen) indicándonos que existe una comunicación y que S4A ha reconocido nuestra placa.

6. S4A usualmente viene en inglés, pero podemos cambiar el lenguaje para entender los bloques que usaremos, para hacer el cambio de idioma, en la parte superior se encuentra un icono de un círculo simulando el idioma y seleccionamos el español. Como se muestra en la siguiente imagen.

7. Ahora procedemos a crear nuestro semáforo. Primero eliminaremos la imagen que nos aparece de Arduino. Esto se logra dando clic derecho en la imagen que se encuentra en la parte inferior derecha.

Y veremos que se nos borraron los bosques de la parte derecha, para regresar los bloques y tener el semáforo como Arduino. Ya que la imagen anterior que eliminamos, nos realizaba la comunicación entre S4A y Arduino, eso también lo podemos en la placa ya que los LEDs (Rxr y Tx) se encuentran apagados.
Para nuestro semáforo, damos clic "Dibujar objeto como Arduino".

Nos abrirá una pantalla (Editor de Pinturas) con el dibujo de la placa de Arduino, esta la borramos y dibujamos nuestro semáforo.

Una vez que terminamos de realizar nuestro semáforo, veremos que en nuestro programa regresaron los bloques de la parte izquierda y además los LEDs de la placa se encuentran nuevamente encendidos.

8. Lo siguiente será generar diferentes disfraces para que podamos hacer el cambio de las luces del semáforo, esto se hace de la siguiente manera:
Damos clic en la pestaña de "Disfraces" y veremos que nos muestra nuestro semáforo, le damos dos veces copiar. Seguido los renombramos y a cada uno lo editaremos, esto porque se tiene el color rojo y nos faltan el amarillo y verde. Como se muestra en la siguiente imagen.

9. Una vez que se realizaron nuestros disfraces, procedemos a ir a la programación de nuestro semáforo. Primero, regresamos a la pestaña de "Programas", en esta pestaña vamos a arrastrar los bloques que tenemos en la parte izquierda, esto lo hacemos dando un clic izquierdo y sin soltar, lo arrastramos en la parte central de la pestaña de "Programas". Empezaremos con la parte superior de los bloques, seleccionamos el bloque de Control  (color naranja) y tomaremos el bloque que dice "Al presionar tecla", como se muestra en la siguiente imagen.

Este bloque lo que realizará es que al presionar la tecla espacio iniciara nuestro programa. 
Para el siguiente paso, del mismo bloque de Control tomaremos la instrucción "Por siempre", el cual se encarga de hacer que el programa sea repetitivo. Y lo colocamos debajo del primer bloque que arrastramos.

10. Ya que tenemos la estructura principal de nuestro programa, procedemos a encender los LEDs, por lo cual regresamos al bloque de Mover (bloque azul), y arrastramos un bloque que dice "digital 13 encendido” y dos de "digital 13 apagado", los cuales introduciremos en donde está nuestro bloque “por siempre”. Los que son de apagado les cambiamos el valor de 12 y 11 para simular el encendido de una luz de semáforo, para ello tenemos entonces que en el puerto 13 se conectara un LED rojo, en el 12 un LED amarillo y en el 11 un LED verde. La conexión se realizará al final.

Ahora le daremos un tiempo a la luz roja, para esto regresamos de nuevo al bloque de Control arrastramos el bloque que dice "esperar 1 segundo". Y lo ponemos al final de los últimos bloques azules. El valor de un segundo lo modificamos a 5.

Este proceso lo repetimos dos veces más, pero ahora para la luz amarilla y verde. Recuerda que los bloques deben seguir dentro del bloque "por siempre". Como se muestra a continuación.

Ya que tenemos esta parte, ahora procedemos a agregar los disfraces, para ello en el bloque de Apariencia (bloque morado), seleccionamos el que dice "cambiar el disfraz a", estos bloques van antes de iniciar el bloque de encedido o apagado, por ejemplo en el primero tendríamos "cambiar el disfraz a rojo", después de esperar 5 segundos, agregamos el bloque de "cambiar el disfraz a amarillo" y en el siguiente será el verde. Como se muestra a continuación.

Al presionar la tecla espacio, veremos en la parte derecha como cambia nuestro semáforo cada 5 segundos.
Ahora toca hacerlo de forma física. Como se mencionó anteriormente, en el pin 13 tendremos el LED rojo, en el 12 el LED amarillo y en el 11 el LED verde. La conexión del Arduino con los LEDs y la protoboard se muestra a continuación.

###### Recuerda que el LED tienes dos pines o patitas, el pin largo es el lado positivo y el cual irá conectado al Arduino, en cambio el pin corto va a ir con la resistencia la cual llegará al negativo.

Por último, el reto será que tú debes realizar el funcionamiento de un semáforo de verdad, ya que un semáforo no funciona solo cada 5 segundos y recuerda que la imaginación la pones tú, puedes seguir experimentado S4A y divertirte.

Programa completo. (No debes hacer trampa, primero inténtalo) :)
