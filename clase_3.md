# HDFS File system de hadoop & Distributed data storage
Contiene un nodo maestro y un conjunto n de nodos esclavos(workers)
Maestro dirige los recurso hacia los workers
# Arquitectura minima
Existen dos replicas de los maestros(m1, m2, m3)
- M1 Standby
- M2 Activo
- M3 Secundario Esta pendiente a caidas de los otros dos y toma ese lugar y actualiza(no modifica) los metadatos que estan en la RAM
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
Por defecto, los archivos se replican 3 veces, pero se puede cambiar.
# Uso de Hadoop
Se utiliza para la lectura de grandes volumenes de datos.
fsimage contiene todos los metadatos guardados en los nodos esclavos
Cuando yo subo mis datos estos se guardan en los discos duros 
Todos los archivos se guardan en los discos duros de los esclavos
# lectura de datos
Spark
Si el archivo no cabe en la RAM, mueve los datos a la memoria del disco duro y esta parte donde la guarda se llama en espacio de memoria virtual 
Pagesys
Swap
HADOOP mueve el programa a las direcciones de memoria
# PARQUET VS CSV
- Parquet: Texto comprimido, siempre son mas chicos, ya tienen tipo y no necesitas definir schema, 
- CSV: Texto, no tiene tipos(se lee todo string), tienes que definir schema,
  En spark TODAS LAS TABLAS SON INMUTABLES

Spark en escala es solo para spark: saber bien pyspark es facil hacer el salto a escala


# Hadoop o spark
HADOOP tiene HDFS Y YARN 
Esto usaba MAP REDUCE, es deir, aplicar una funcion a todos los datos. Se abandono este paradigma porque usaba intensivamente el disco y no aprovehcaba la RAM a diferencia de spark.
Spark mueve de RAM a RAM, no utiliza el disco.



# YARN Optimiza el uso de los recursos
Gestiona recursos y administra cuando los nodos esclavos mandan info
Cada nodo que se ejecuta en un proceso, se ejecuta en un contenedor
Ejecucion perezoso en una tabla: 
Si quiero hacer un group by esta puede esperar hasta que el grafo de ejecucion se vea obligado, y esto logra una optimizacion.
Ver diagrama de como es la secuencia de trabajo en YARN.
Zookeeper: Es el nodo que se encarga de 

