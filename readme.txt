docker build -t my-hadoop .
docker run -p 8088:8088 -p  50030:50030 -p 50060:50060 -p 50070:50070 -p 50075:50075 --name my-hadoop-container -d my-hadoop



# start interactive shell in running container
docker exec -it my-hadoop-container bash

# once shell has started run hadoop "pi" example job
hadoop jar $HADOOP_HOME/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.8.1.jar pi 10 100

http://localhost:8088
