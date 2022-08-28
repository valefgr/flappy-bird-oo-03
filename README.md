# Flappy Bird Parte 3

## Introducción

En los labs anteriores agregaste el HTML y CSS del juego flappy bird. En éste lab comenzarás a agregar la lógica y funcionalidad del juego.  

## Instrucciones

Dentro de `script.js` verás que se encuentran dos objetos: `juego` y `bird`. 

Agrega los siguientes métodos y propiedades a `bird` y `juego`. Las descripciones para los métodos y propiedades del objeto bird y juego se encuentran más abajo en este README.

1. Agrega la propiedad `juego.timerId`
2. Agrega la propiedad `juego.gravedad`
3. Agrega el método `juego.aleatorio`
4. Agrega la propiedad `bird.div`
5. Agrega la propiedad `bird.bottom`
6. Agrega la propiedad `bird.left`
7. Agrega la propiedad `bird.width`
8. Agrega la propiedad `bird.height`
9. Agrega el método `bird.efectoGravedad`
10. Agrega el método `bird.dibujar`
11. Agrega el método `bird.mover`
12. Agrega el método `juego.loop`
13. Agrega el método `juego.iniciar`


## El objeto juego

### Propiedades:
1. `timerId`
- **¿Qué valor tiene?**: `juego.timerId` tiene como valor el numero `0` (para iniciar)
- **¿Dónde se utiliza?**: `juego.timerId` se utilizará dentro de `juego.inicar()` para guardar un timer que llame cada 20 milisegundos a `juego.loop`

2. `gravedad`
- **¿Qué valor tiene?**: `juego.gravedad` tiene como valor el numero `2`
- **¿Dónde se utiliza?**: La variable `gravedad` representa el numero de pixeles que se restarán a `bird.bottom` cuando se aplique el método `bird.efectoGravedad()`


### Métodos:
1. `aleatorio()` 
- **¿Qué hace?**: Devuelve un numero aleatorio entre un minimo y máximo dado
- **¿Dónde se utiliza?**: `bird.bottom` llamará a `juego.aleatorio()` para calcular un numero aleatorio entre `10` y `570`


2. `loop()`
- **¿Qué hace?** :Llama a `bird.efectoGravedad()`, `bird.dibujar()` y `juego.verificaColision()`
- **¿Dónde se utiliza?**: `juego.iniciar()` inicia un `setInterval()` que llama a `juego.loop()` cada 20 milisegundos. De ésta manera cada 20 milisegundos se aplicará el efecto de gravedad a bird, se dibujará bird en su nueva posicion, y se verificará si hubo una colisión


3. `iniciar()`
- **¿Qué hace?** : Agrega un eventListener de tal forma que cada que se pulse una tecla, se llame a `bird.move`. También asigna a `juego.timerId` un `setInterval()` que llame a `juego.loop()` cada 20 milisegundos. 
- **¿Dónde se utiliza?**: `juego.iniciar()` se tiene que llamar para iniciar el juego. A través del `setInterval()` cada 20 milisegundos se aplicará el efecto de gravedad a `bird`, se dibujará `bird` en su nueva posicion, y se verificará si hubo una colisión. A través del eventListener, se puede mover `bird`



## El objeto bird:

### Propiedades
1. `div`
- **¿Qué valor tiene?**: `bird.div` tiene como valor el elemento html con clase `.bird`
- **¿Dónde se utiliza?**: `bird.div` se utiliza dentro del método `bird.dibujar` de tal forma que se pueda dibujar el elemento en posiciones determinadas

2. `bottom`
- **¿Qué valor tiene?**: `bird.bottom` tiene un valor aleatorio entre `10` y `570`. Para calcular este valor aleatorio `bird.bottom` utiliza el método `juego.aleatorio()`
- **¿Dónde se utiliza?**:  El valor de `bird.bottom` basicamente determina en donde se va a posicionar el elemento `bird`. Por lo tanto `bird.bottom` se utiliza en los metodos `bird.efectoGravedad()`, `bird.dibujar()`, `bird.mover()` y `bird.colision()`

3. `left`
- **¿Qué valor tiene?**: `bird.left` tiene como valor el numero `250`
- **¿Dónde se utiliza?**: `bird.left` se utiliza dentro de `bird.dibujar()`. El valor de bird.left basicamente determinará el numero de pixeles a la izquierda del elemento con clas `.bird`

4. `width`
- **¿Qué valor tiene?**: `bird.width` tiene como valor el numero `60`
- **¿Dónde se utiliza?**: El valor de de `bird.width` se utilizará más adelante para determinar si hubo una colision entre `bird` y los `obstaculos`

5. `height`
- **¿Qué valor tiene?**: `bird.height` tiene como valor numero `45`
- **¿Dónde se utiliza?**: El valor de de `bird.height` se utilizará más adelante para determinar si hubo una colision entre `bird` y los `obstaculos`

### Métodos:

1. `efectoGravedad()`
- **¿Qué hace?**: `bird.efectoGravedad()` disminuye la propiedad `bird.bottom` por el valor de `juego.gravedad`
- **¿Dónde se utiliza?**: `juego.loop()` llama a `bird.efectoGravedad()`. Recuerda que `juego.loop()` se llama cada 20 milisegundos a través de `juego.iniciar()`. 

2. `dibujar()`
- **¿Qué hace?**: `bird.dibujar()` asigna a la propiedad bottom de `bird.div` (el elemento html con clas bird) el valor en pixeles de la propiedad `bird.bottom`
- **¿Dónde se utiliza?**: `juego.loop()` llama a `bird.dibujar()`. Recuerda que `juego.loop()` se llama cada 20 milisegundos a través de `juego.iniciar()`. 

3. `mover()`
- **¿Qué hace?**: `bird.mover()` agrega `40` a `bird.bottom`
- **¿Dónde se utiliza?**: `juego.iniciar()` agrega un eventListener de tal forma que cuando se pulse una tecla, se llame a `bird.mover()`



