# Introduction to Kafka
Kafka is a distributed system consisting of servers and clients that communicate via a high-performance TCP network protocol. It can be deployed on bare-metal hardware, virtual machines, and containers in on-premise as well as cloud environments.

# Steps
To begin preparing for Kafka Apps, we will follow the given steps:

## Step 1:  Start the zookeeper service
``` .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties ```

## Step 2:  Start the kafka service
``` -.\bin\windows\kafka-server-start.bat .\config\server.properties ```

## Step 3: Create a unique topic
``` .\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create –topic Texas-Snow ```

## Step 4: List all created topics
``` .\bin\windows\kafka-topics.bat --zookeeper localhost:2181 –list ```

## Step 5: Start a Kafka producer for writing messages to your unique topic
``` .\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic Texas-Snow```">
<img src = "Kafka Producer.PNG">

## Step 6: start a Kafka consumer for retrieving messages from your unique topic
``` 
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic bearcat-messages Texas-Snow --from-beginning 
```
<img src = "Kafka Consumer.PNG">

