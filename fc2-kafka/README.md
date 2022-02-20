

```
docker-compose up -d
docker exec -it fc2-kafka_kafka_1 bash
kafka-topics --create --topic=teste --bootstrap-server=localhost:9092 --partitions=3
kafka-topics --list --bootstrap-server=localhost:9092

kafka-topics --bootstrap-server=localhost:9092 --topic=teste --describe

kafka-console-consumer --bootstrap-server=localhost:9092 --topic=teste 
docker exec -it fc2-kafka_kafka_1 bash
kafka-console-producer --bootstrap-server=localhost:9092 --topic=teste 
kafka-console-consumer --bootstrap-server=localhost:9092 --topic=teste --from-beginning

kafka-console-producer --bootstrap-server=localhost:9092 --topic=teste 
kafka-console-consumer --bootstrap-server=localhost:9092 --topic=teste --group=x

kafka-consumer-groups --bootstrap-server=localhost:9092 --group=x --describe
kafka-console-consumer --bootstrap-server=localhost:9092 --topic=teste --group=x --consumer-property client.id=test1
```