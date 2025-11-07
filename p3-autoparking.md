# P3 - Autoparking

## Alinear el coche
El coche avanza y gira hacia la derecha hasta que el laser de delante detecta que está suficientemente cerca de otro coche. En ese momento, calcula cuanto tiene que girar para alinearse usando el angulo del rayo del laser que detecto la menor distancia.

Después, el coche avanza hacia delante mientras que gira a la izquierda hasta que ha girado el ángulo calculado anteriormente. Cuando deja de girar, el coche ya está alineado y empieza a avanzar recto hacia delante para buscar un hueco en el que aparcar. 


## Encontrar hueco de aparcamiento
El coche avanza hacia delante mientras utiliza los últimos rayos del laser de delante, los primeros rayos del laser de detras y el tercio central del laser de la derecha para comprobar si hay un hueco libre para aparcar.

Cuando encuentra un hueco, el coche avanza hacia delante utilizando la odometría para comprobar cuando dejar de avanzar y empezar con las maniobras para aparcar,


## Aparcar
El coche retrocede mientras que gira hasta alcanzar un ángulo concreto, En ese momento, retrocede recto una cierta distancia. Después sigue retrocediendo pero gira mientras retrocede. Finalmente termina de aparcar avanzando un poco hacia delante.



## Videos
video con dos coches:
[video autopaking dos coches](https://urjc-my.sharepoint.com/:v:/g/personal/s_gonzaleza_2022_alumnos_urjc_es/Ebbi4iDd5ipBnzZz8QSQqPoBOreae-ygA_UpQVRyDQVALA?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=0lDn3l)

video con el coche de delante:
[video autopaking coche de delante](https://urjc-my.sharepoint.com/:v:/g/personal/s_gonzaleza_2022_alumnos_urjc_es/EdsSYoOz6pxKoJHWzx_pdSIBNPC6kHm0ZbYYlQmRBTI8JA?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=3Td987)

video con el coche de detras:
[video autopaking coche de detras](https://urjc-my.sharepoint.com/:v:/g/personal/s_gonzaleza_2022_alumnos_urjc_es/ESxXag0FbehChb0vbclLdEUBX9B4smgr3Z3wsvXTZJFO2w?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=1RElLW)




