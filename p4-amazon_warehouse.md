# P4 - Amazon warehouse

## Registro del mapa
He elegido 8 puntos del mundo y sus respectivas coordenadas en pixeles del mapa para registrar el mapa. Después he creado la función world_to_pixel para pasar de coordenadas del mundo a coodenadas en pixeles, y la función pixel_to_world para pasar de coordenadas del mapa a coordenadas del mundo. 


## Creación del plan
En el holonómico utilizo SE2StateSpace y en el ackermann utilizo DubinsStateSpace. Como start utilizo la posición del robot y como goal utilizo la coordenada de la estantería y la coordenada en la que quiero dejar la estantería. En isStateValid compruebo que ningún pixel del robot (o del robot con estanteria) esté en un pixel ocupado del mapa, si no coincide ningún pixel el esta es válido.
Cuando se consigue el plan, creo una lista con las coordenadas por las que tiene que pasar el robot para llegar a la coordenada objetivo (la coordenada de la estantería o la coordenada en la que va a dejar la estantería)


## Ir a la coordenada objetivo
Voy calculando la distancia entre la posición y del robot y la siguiente coordenada por la que tiene que pasar y el ángulo, y según la orientación del robot se establece la velocidad lineal y angular. En robot holonómico siempre avanza hacia delante ya que puede girar en el sitio, y el robot ackermann puede avanzar hacia delante y retroceder. El holonómico gira sobre sí mismo para colocarse después de haber llegado al goal (función turn_to_align). 


## Eliminar estantería levantada
Una vez levantada la estantería, pinto de blanco en el mapa en la posición en la que estaba la estantería.


## Añadir estantería movida
Una vez que se deja una estantería, pinto de negro en el mapa en la posición en la que se ha dejado la estantería.


## Videos
video holonomico:
[video holonomico](https://urjc-my.sharepoint.com/:v:/g/personal/s_gonzaleza_2022_alumnos_urjc_es/EboHUz2A9JxAnM_Qlsvdh6ABJ70HaafwNSv_bE_iHQg0_g?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=FyeX4D)

video ackermann:
[video ackermann](https://urjc-my.sharepoint.com/:v:/g/personal/s_gonzaleza_2022_alumnos_urjc_es/EQtQG8B82_NOlVg4Dnw36rgBDIsj9bZSaRfU4TibivNSmg?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=j3gcfS)
