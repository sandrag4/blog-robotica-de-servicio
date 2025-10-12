# P1 - Localized Vacuum Cleaner

## Creación de la rejilla de navegación
Obtengo el mapa, lo convierto a escala de grises y le aplico erosión. He creado celdillas de tamaño 32x32 píxeles. Si menos del 14% de los pixeles de una celdilla están ocupados esa celdilla se marca como libre (en blanco), si no, se marca como ocupada (en negro). La función paint_map pinta las celdillas. 


## Transformación de coordenadas
Tengo una función para pasar la posición del robot en el mundo (HAL.getPose3d().x, HAL.getPose3d().y) a su posición en el mapa en píxeles, una función para pasar la posición del robot en el mundo a su posición en celdillas, una función para pasar de la celdilla al pixel del medio de esa celdilla, y una función para pasar de la posición en pixeles a la posición en el mundo.


## Planificación de ruta (algoritmo BSA)
Empiezo obteniendo la posición del robot en celdillas y en pixeles.

Voy guardando en return_cells las posibles celdillas de retorno (estas son las celdillas a distancia 1 hacia arriba, abajo, derecha e izquierda de la ultima celdilla añadida a la ruta.), una vez que una celdilla se añade a la ruta que va a seguir el robot, se borra de la lista de posibles celdillas de retorno.

El algoritmo empieza añadiendo a la ruta que va a seguir (visited_cells) todas las celdillas hacia arriba hasta encontrarse con una celdilla ocupada, una vez que no puede avanzar más hacia arriba, avanza hacia la derecha en caso de que sea posible (si no es posible avanza hacia la izquierda) cuando se encuentra una celdilla ocupada avanza hacia abajo, cuando no puede avanzar más hacia abajo avanza hacia la derecha (a la izquierda si no hay celdillas libres hacia la derecha) y cuando no puede avanzar más vuelve a ir hacia arriba. Y vuelve a repetirlo hasta que se encuentra que ha llegado a un punto crítico y no puede avanzar en ninguna dirección. Cada celdillas añadida se va pintando en el mapa de amarillo. El punto crítico lo pinta de rojo.

Cuando se encuentra en un punto crítico, elige como punto de retorno el último elemento de la lista de posibles puntos (return_cells) y lo añade a la lista de puntos de retorno que va a utilizar como puntos de retorno (return_cells_list). El punto de retorno se pinta en azul.

Para buscar el camino al punto de retorno, se utiliza el algoritmo de búsqueda BFS, una vez encontrado, se añade a la ruta que va a seguir el robot.

Este proceso se repite hasta que todas las celdillas libres están añadidas a la ruta (visited_cells) que va a seguir la aspiradora 


## Realización de la ruta planificada
El robot va siguiendo la ruta creada y marca cada celdilla por la que pasa en verde. 

Para avanzar de su posición a la siguiente celdilla, primero calcula el ángulo y la distancia al centro en pixeles de la siguiente celdilla, después gira hasta situarse con una orientación que le permita avanzar hacia delante hasta la siguiente celdilla de la ruta. Una vez obtenida la orientación adecuada, el robot avanza hacia delante hasta situarse mas o menos en el centro de la siguiente celdilla. Utilizo un PID para ajustar la velocidad lineal y angular.


## Imagen después de terminar

![Imagen Localized vacuum cleaner](https://github.com/sandrag4/blog-robotica-de-servicio/blob/main/imagenes/imagen-p1.png "Imagen localized acuum cleaner")


## Video
video:
[video localized vacuum cleaner](https://urjc-my.sharepoint.com/:v:/g/personal/s_gonzaleza_2022_alumnos_urjc_es/EZBba-yAsvFJnNU8-SWH86sB9M2YujARxjkHUg48UwKWcA?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=SfQVMx)




