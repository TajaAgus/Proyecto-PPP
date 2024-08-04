#### Diferencia entre field y property (C#)
- Los fields almacenan datos directamente, normalmente con modificadores de acceso privados o protegidos para encapsularlos. Son ideales para gestionar el estado interno de un objeto. 
- Las properties proporcionan un acceso controlado a los fields mediante métodos getter y setter, lo que permite la validación y la integración lógica.

#### Time.deltaTime
`Time.deltaTime` es el tiempo que pasa entre un frame y el siguiente. En cada frame, se ejecuta el método `Update`. Si multiplicas este valor por una velocidad, aseguras que esa velocidad sea constante sin importar cuántos frames por segundo esté corriendo el juego.

Ejemplo: Si el juego corre a 2 frames por segundo y tu velocidad es 1 unidad por segundo, entonces 1 segundo dividido por 2 frames da 0.5. Al multiplicar 0.5 por la velocidad (1), obtienes que el desplazamiento en ese frame es de 0.5 unidades.

#### Eje Z y transform.forward (Unity)
En el contexto de Unity y sistemas de coordenadas 3D, el eje Z es uno de los tres ejes que definen la posición y la dirección de los objetos en el espacio tridimensional. Los ejes X, Y y Z forman un sistema de coordenadas cartesiano.

1. **Eje X**: Representa la dirección horizontal. Aumentar el valor en el eje X mueve el objeto hacia la derecha (en el espacio mundial).
    
2. **Eje Y**: Representa la dirección vertical. Aumentar el valor en el eje Y mueve el objeto hacia arriba (en el espacio mundial).
    
3. **Eje Z**: Representa la dirección de profundidad. Aumentar el valor en el eje Z mueve el objeto hacia adelante en el espacio mundial (hacia el usuario si estamos mirando una vista ortográfica de frente).
    

En Unity, el sistema de coordenadas sigue la convención de mano izquierda, lo que significa que:

- El eje X positivo apunta a la derecha.
- El eje Y positivo apunta hacia arriba.
- El eje Z positivo apunta hacia adelante.

Cuando se dice que `transform.forward` apunta en la dirección del eje Z local del objeto, se refiere a que, independientemente de cómo esté rotado el objeto, `transform.forward` siempre apunta en la dirección que corresponde al eje Z en el espacio local del objeto.

Por ejemplo, si tienes un objeto con una rotación en Unity y deseas moverlo hacia adelante desde su perspectiva, usarías `transform.forward` porque esto apunta en la dirección del eje Z local del objeto, que puede diferir del eje Z mundial debido a la rotación del objeto.

Visualmente, si observas el Gizmo en el editor de Unity (el pequeño sistema de ejes de colores que aparece cuando seleccionas un objeto), verás algo como esto:

- Eje X: Rojo
- Eje Y: Verde
- Eje Z: Azul

El eje Z (azul) es el que apunta hacia adelante desde la perspectiva del objeto cuando no tiene rotación aplicada.