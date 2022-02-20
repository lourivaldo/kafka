

```
docker exec -it gokafka bash
go mod init github.com/lourivaldo/fc2-gokafka
go run cmd/producer/main.go

docker exec -it go-kafka_kafka_1 bash
kafka-topics --create --bootstrap-server=localhost:9092 --topic=teste --partitions=3
kafka-console-consumer --bootstrap-server=localhost:9092 --topic=teste

go get github.com/confluentinc/confluent-kafka-go/kafka

go run cmd/consumer/main.go

kafka-consumer-groups --bootstrap-server=localhost:9092 --group=goapp-group --describe
```