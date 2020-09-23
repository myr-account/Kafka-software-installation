# Kafka-software-installation
## Software download
Firstly we need to download the software form Apache organization through the following link: [https://www.apache.org/dyn/closer.cgi?path=/kafka/2.6.0/kafka_2.13-2.6.0.tgz](https://www.apache.org/dyn/closer.cgi?path=/kafka/2.6.0/kafka_2.13-2.6.0.tgz)
## Starting services through kafka
1. To start zookeeper service, we need to open powershell as Administrator in the kafka folder and run the following command <br/>
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
1. Now we need to run the kafka service in another powershell as Administrator window <br/>
.\bin\windows\kafka-server-start.bat .\config\server.properties
1. I have created a "daily-routine" as my topic
1. created topics like, "daily-routine","cricket-history"
1. To start the kafka producer, <br/>
.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic daily-routine <br/>
This is the producer where we enter the daily-routine topic messages
1. To start kafka consumer, <br/>
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic daily-routine --from-beginning <br/>
This is the consumer where we recive the entered topic messages