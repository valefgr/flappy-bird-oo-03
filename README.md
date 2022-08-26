# Flappy Bird Parte 2


## Introducción
En éste lab crearás 2 objetos: juego y bird. Estos objetos tendrán los métodos y propiedades que se describen a continuación.

## El objeto juego

### Propiedades:
- timerId
- **¿Qué hace?**: 
- **¿Dónde se utiliza?**: 

- gravedad
- **¿Qué hace?**: 
- **¿Dónde se utiliza?**: 

- skyHeight
- **¿Qué hace?**: 
- **¿Dónde se utiliza?**: 


### Métodos:
1. `aleatorio()` 
- **¿Qué hace?**: Devuelve un numero aleatorio entre un minimo y máximo dado
- **¿Dónde se utiliza?**: `bird.bottom` llamará a `juego.aleatorio()` para calcular un numero aleatorio entre 10 y 570


2. `verificaColision()`
- **¿Qué hace?**: Llama a `bird.colision()` para revisar si `bird` tuvo una colision. Si `bird.colision()` devuelve el valor `true`, llama a `juego.terminar()` para terminar el juego.
- **¿Dónde se utiliza?**:  `juego.loop()` llamará a `juego.verificaColision()` para revisar constantemente si hubo una colisión.  


3. `loop()`
- **¿Qué hace?** :Llama a `bird.efectoGravedad()`, `bird.dibujar()` y `juego.verificaColision()`
- **¿Dónde se utiliza?**: `juego.iniciar()` inicia un `setInterval()` que llama a `juego.loop()` cada 20 milisegundos. De ésta manera cada 20 milisegundos se aplicará el efecto de gravedad a bird, se dibujará bird en su nueva posicion, y se verificará si hubo una colisión.


4. `iniciar()`
- **¿Qué hace?** : Agrega un eventListener de tal forma que cada que se pulse una tecla, se llamará al bird.move. También asigna a `juego.timerId` un `setInterval()` que llama a `juego.loop()` cada 20 milisegundos. 
- **¿Dónde se utiliza?**: `juego.iniciar()` se llama para iniciar el juego. A través del setInterval() cada 20 milisegundos se aplicará el efecto de gravedad a bird, se dibujará bird en su nueva posicion, y se verificará si hubo una colisión. A través del eventListener, se puede mover bird.

5. `terminar()`
- **¿Qué hace?**: Limpia el timer guardado dentro de `game.timerId` (el que llama cada 20 milisegundos a `game.loop`). También, llama a `juego.mostrarGameOver()` y `juego.pararEfectos()`. 
- **¿Dónde se utiliza?**: El metodo `juego.terminar()` se llama cuando hay una colision


6.  `mostrarGameover()`
- **¿Qué hace?**:  Agrega el id "game-over" al elemento html con clase `.message`
- **¿Dónde se utiliza?**: `juego.terminar()` llama a `juego.mostrarGameOver` para mostrar el mensaje "Game Over" cuando el juego termina.

7. `pararEfectos()`
- **¿Qué hace?**: quita el id al elemento con clase `.ground`. También agrega el id "fall" al div con clase `.bird`
- **¿Dónde se utiliza?**: `juego.terminar()` llama a `juego.pararEfectos()` para que bird deje de aleatear y el suelo deje de moverse. 


## El objeto bird:

### Propiedades
- div
- **¿Qué hace?**: 
- **¿Dónde se utiliza?**: 

- bottom
- **¿Qué hace?**: 
- **¿Dónde se utiliza?**: 

- left
- **¿Qué hace?**: 
- **¿Dónde se utiliza?**: 

- width
- **¿Qué hace?**: 
- **¿Dónde se utiliza?**: 

- height
- **¿Qué hace?**: 
- **¿Dónde se utiliza?**: 

### Métodos:

1. `efectoGravedad()`
- **¿Qué hace?**: 
- **¿Dónde se utiliza?**: 

2. `dibujar()`
- **¿Qué hace?**: 
- **¿Dónde se utiliza?**: 

3. `mover()`
- **¿Qué hace?**: 
- **¿Dónde se utiliza?**: 

4. `colision()`
- **¿Qué hace?**: 
- **¿Dónde se utiliza?**: 

