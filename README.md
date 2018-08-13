# hadoopwindowsinstructions

1. Download Zookeeper version - zookeeper-3.4.12 and Kafka version - kafka_2.10-0.10.1.1
2. The code of zookeeper and kafka is packaged together
3. zookeeper server has to be started with the below command (please note all the commands has to be executed in admin command mode)
	D:\hadoop\zookeeper\extracted\zookeeper-3.4.12\bin\zkserver
4. kafka server has to be started with the below command
	D:\hadoop\kafka_2.10-0.10.1.1\bin\windows>kafka-server-start.bat D:\hadoop\kafka_2.10-0.10.1.1\config\server.properties
5. We can test the application by passing the commands as below : 

PRODUCER 
D:\hadoop\kafka_2.10-0.10.1.1\bin\windows>kafka-console-producer.bat --broker-list localhost:9092 --topic test
sabari
testing
going on
please confirm
receiver is
receiving messages
or not
yes
receiving terminal is receiving messages

CONSUMER 

D:\hadoop\kafka_2.10-0.10.1.1\bin\windows>kafka-console-consumer.bat --zookeeper localhost:2181 --topic test
Using the ConsoleConsumer with old consumer is deprecated and will be removed in a future major release. Consider using the new consumer by passing [bootstrap-server] instead of [zookeeper].
testing
going on
please confirm
receiver is
receiving messages
or not
yes
receiving terminal is receiving messages

TO PRODUCE VIA A TEXT FILE : 
D:\hadoop\kafka_2.10-0.10.1.1\bin\windows>kafka-console-producer.bat --broker-list localhost:9092 --topic test < D:\Sabari\test.txt

As a result, automatically the consumer will read the inputs accordingly through the same topic named 'test'
