# kafka-installation-steps

## kafka commands

### we need to run the commands in different powershell windows

### Command to run zookeeper service (First step and keep terminal open)

```.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties ```

### Command to start the kafka service (Second step and keep terminal open)
``` .\bin\windows\kafka-server-start.bat .\config\server.properties ```

### Command to create a kafka topic (Third step, here we are creating topic)
```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic anil-bomma```

### Command to list the created topics (Fourth step, here we are listing all topic)
``` .\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list ```

### Command to delete the topic (Fifth step, here we are deleting the topic with given topic name)
```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --delete --topic anil-bomma ```

### Command to run the producer (will publish queue to consumer)
This allows you to send the messages to the topic

``` .\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic anil-bomma ```

### Command to run the consumer (will listen request queue from the producer)
It will display the messages sent to the topic

``` .\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic anil-bomma --from-beginning```
