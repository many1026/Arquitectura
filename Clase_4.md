# MAP REDUCE

Sparl guarda en la RAM y hadoop guarda en el disco. Los dos de manera local
Shuffle(HADOOP): Es la transferencia de datos; algo que spark no lo hace porque hay que transferir por red.
Las operaciones en disco es 10 veces más lenta que las operaciones de RAM


## USAMOS SPARK PORQUE MAXIMIZA EL USO DE LA RAM Y MINIMIZA ACCESOS DIRECTOS POR EL DISCO

MAPREDUCE resuelve problemas paralelos tipo SIMD
sPARK usa el DAG y trata de optimizar los shuffle


Disco mecanico vs disco solido
Disco mecanico(duro) es muy lento y disco solido es rapido.

Kubernetics(Orquestador de dockers)
Dockers: Paquetes de maquina virtuales


### Apache Spark (HDFS Y YARN):
Cada vez se esta dejando de utiizar YARN. Porque YARN se ha logrado optimizar


RDD es un mini data lake, es un bucket de spark.
un data lake organizado en bases de datos tengo un data warehouse.
