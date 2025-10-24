# P2 - Rescue People

## Buscar supervivientes
Envío el dron a la zona de los supervivientes. Cuando el dron llega a la zona, empieza a realizar una espiral cuadrada para buscar a las personas, lo comando por posición para garantizar una altura de 1,3 metros. Utilizo esta altura para que haar detecte las caras correctamente pero no está lo suficientemente bajo como para que le alcanzen las olas.


## Detectar caras
He hecho un filtro hsv para eliminar el mar, evitando asi que se detecte el mar erroneamente como cara, después paso la imagen a escala de grises y la ecualizo. Voy rotando la imagen en ángulos de 30 grados y voy comprobando si detecta la cara de alguna persona con haar. 

Si detecta alguna cara, compruebo si esa persona ya fue añadida a la lista de personas encontradas y la añado si no está en la lista.


## Bateria baja
Cuando el dron lleva volando unos 5 minutos (300 segundos), el dron considdera que su bateria es baja y vuelve para recargarse. Después de recargar su batería, vuelve a la posición donde dejó de buscar a las peronas y reanuda su búsqueda.


## Video
video:
[video rescue people](https://urjc-my.sharepoint.com/:v:/g/personal/s_gonzaleza_2022_alumnos_urjc_es/EQyMvljFp0JPkjzEw510mS8B-lxmpYYwZ6uGG4NhDl0p-g?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=sVWLZw)




