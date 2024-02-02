# HDFS File system de hadoop & Distributed data storage
Contiene un nodo maestro y un conjunto n de nodos esclavos(workers)
Maestro dirige los recurso hacia los workers
# Arquitectura minima
Existen dos replicas de los maestros(m1, m2, m3)
- M1 Standby
- M2 Activo
- M3 Secundario Esta pendiente a caidas de los otros dos y toma ese lugar y actualiza los metadatos que estan en la RAM
 Hay al menos 6 nodos workers
La informacion viaja hacia
Los datos no se mueven, se mueven los programas. Esto es para agilizar y no depender de la latencia(lo que haria un cuello de botella)
Shared Edit crece lentamente y journal crece rapido porque contiene los metadatos
# Arquitecturas
EN BIG DATA ME INTERES LEER, NO ESCRIBIR
Se dice que el disco se fragmenta, cuando yo borro archivos de mi disco duro y dejo espacios en este disco. 
Esto es ineficiente porque el cabezal se mueve de esquina a esquina y se tarda en hacer esta consulta.
Un grupo de bloques se llama cluster o agrupaciones. 
Cuando escribo en un disco duro, me interesa tener bloques pequeños para no desperdiciar espacio. En big data no.
Cuando hacemos una particiones, los metadatos estan en la RAM, no en el disco.
