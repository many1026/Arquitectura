# HDFS
Contiene un nodo maestro y un conjunto n de nodos esclavos(workers)
Maestro dirige los recurso hacia los workers
# Arquitectura minima
Existen dos replicas de los maestros(m1, m2, m3)
- M1 Standby
- M2 Activo
- M3 Secundario Esta pendiente a caidas de los otros dos y toma ese lugar
 Hay al menos 6 nodos workers
