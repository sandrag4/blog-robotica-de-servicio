# P3 - Autoparking

## Alinear el coche
El coche avanza y gira hacia la derecha hasta que el laser de delante detecta que está suficientemente cerca de otro coche. En ese momento, empieza a comprobar con el laser derecho si obstaculos que hay estan alineados con el coche.

Después, el coche avanza hacia delante mientras que gira a la izquierda hasta detecta que está alineado. Cuando el coche ya está alineado, deja de girar y empieza a avanzar recto hacia delante para buscar un hueco en el que aparcar. 


## Encontrar hueco de aparcamiento
El coche avanza hacia delante mientras utiliza los últimos rayos del laser de delante, los primeros rayos del laser de detras y el tercio central del laser de la derecha para comprobar si hay un hueco libre para aparcar.

Cuando encuentra un hueco, el coche avanza hacia delante utilizando la odometría para comprobar cuando dejar de avanzar y empezar con las maniobras para aparcar,


## Aparcar
El coche retrocede mientras que gira hasta alcanzar un ángulo concreto, En ese momento, retrocede recto una cierta distancia. Después sigue retrocediendo pero gira mientras retrocede. Finalmente termina de aparcar avanzando un poco hacia delante.


## Videos
video con dos coches:
[video autopaking dos coches](https://urjc-my.sharepoint.com/:v:/g/personal/s_gonzaleza_2022_alumnos_urjc_es/Efx2SUs3PbBDiwpnudAaPKUBTX6wCxiJ7o2L4OcWuQgbBw?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=Tpent0)

video con el coche de delante:
[video autopaking coche de delante](https://urjc-my.sharepoint.com/:v:/g/personal/s_gonzaleza_2022_alumnos_urjc_es/EWhIH5DMgGlAvrgBtkPLDd8BHpvN6Y4YEKw08vMpCu_cYg?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=xyg4eg)

video con el coche de detras:
[video autopaking coche de detras](https://urjc-my.sharepoint.com/:v:/g/personal/s_gonzaleza_2022_alumnos_urjc_es/EcVwNXoER59PnC0SRykO8o4B-TZZa9_KZDKjRe2WqmkSZQ?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=Ulo9lV)




