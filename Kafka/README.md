# Create Topic

```bash
docker exec broker kafka-topics --bootstrap-server broker:9092 --create --topic <topic-name>
```

# list topic

```bash
docker exec broker kafka-topics --bootstrap-server broker:9092 --list
```


# Write message to topic

```bash
docker exec --interactive --tty broker kafka-console-producer --bootstrap-server broker:9092 --topic <topic-name>
```

# Read messages from the topic 

```bash
docker exec --interactive --tty broker kafka-console-consumer --bootstrap-server broker:9092 --topic <topic-name> --from-beginning
```

# Stop the kafka broker 
## if you stop the Kafka Broker with this command you will lose the docker container which means that you will also lose all of the Kafka topics.

```bash
docker compose down
```