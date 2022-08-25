# Flappy Bird Parte 2


## Introducción
En éste lab crearás 2 objetos: juego y bird. Estos objetos tendrán los siguientes métodos y propiedades.

## El objeto juego

### Propiedades:
- timerId
- gravedad
- skyHeight


### Métodos:
1. `aleatorio()` 
- **¿Qué hace?**: Devuelve un numero aleatorio entre un minimo y máximo dado
- **¿Dónde se utiliza?**: `bird.bottom` llamará a `juego.aleatorio()` para calcular un numero aleatorio entre 10 y 570


2. `verificaColision()`
- **¿Qué hace?**: Llama a `bird.colision()` para revisar si `bird` tuvo una colision. Si `bird.colision()` devuelve el valor `true`, llama a `juego.terminar()` para terminar el juego.



3. `loop()`
- **¿Qué hace?** :Llama a `bird.efectoGravedad()`, `bird.dibujar()` y `juego.verificaColision()`

4. `iniciar()`
**¿Qué hace?** :inicia el juego. Agrega un event

5. `terminar()`: term

6.  `mostrarGameover()`: 

7. `pararEfectos()`:

#### El objeto bird:

Propiedades:
- div
- bottom
- left
- width
- height

Métodos:
- efectoGravedad
- dibujar
- mover
- colisión

