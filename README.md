# hadoop-windows

<img src="./img.png">

 - http://localhost:9870/dfshealth.html#tab-overview

 - http://localhost:8088/cluster

 - https://www.ncei.noaa.gov/pub/data/uscrn/products/daily01/2015/CRND0103-2015-TX_Austin_33_NW.txt


run start-all.cmd


there are 2 Possible Solutions to resolve

First:

Your namenode and datanode cluster ID does not match, make sure to make them the same.

In name node, change ur cluster id in the file located in:

$ nano HADOOP_FILE_SYSTEM/namenode/current/VERSION 
In data node you cluster id is stored in the file:

$ nano HADOOP_FILE_SYSTEM/datanode/current/VERSION
Second:

Format the namenode at all:

Hadoop 1.x: $ hadoop namenode -format

Hadoop 2.x: $ hdfs namenode -format
