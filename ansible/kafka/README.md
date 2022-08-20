
## Testing

```sh
sudo su - kafka
bash
/data/kafka/kafka/bin/kafka-topics.sh --create --topic test-topic6 --bootstrap-server 192.168.251.251:9092,192.168.251.252:9092,192.168.251.253:9092 --replication-factor 3 --partitions 3

/data/kafka/kafka/bin/kafka-console-producer.sh --broker-list 192.168.251.251:9092 --producer.config /data/kafka/kafka/config/producer.properties --topic test-topic6

/data/kafka/kafka/bin/kafka-console-consumer.sh --bootstrap-server 192.168.251.251:9092,192.168.251.252:9092,192.168.251.253:9092 --topic test-topic6 --from-beginning

