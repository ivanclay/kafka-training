# Kafka Training

![Badge de Licença](https://img.shields.io/badge/.NET-8.0.0-blue.svg?style=flat-square&logo=dotnet)
![Badge de Licença](https://img.shields.io/badge/Apache_Kafka-2.13_3.0.0-orange.svg?style=flat-square&logo=apachekafka)
![Badge de Licença](https://img.shields.io/badge/git-2.42.0-lightgrey.svg?style=flat-square&logo=git)
![Badge de Licença](https://img.shields.io/badge/docker-27.2.0-orange.svg?style=flat-square&logo=docker)

![Badge de Versão](https://img.shields.io/badge/app-v_1.0.0-green.svg?style=flat-square&logo=app)
![Badge de Status do Projeto](https://img.shields.io/badge/status-training-blue.svg?style=flat-square)

It is only a Kafka training repository

### Contextualization


### KAFKA Install (Windows WSL2)

```sh
    wget -O- https://apt.corretto.aws/corretto.key | sudo apt-key add -
```

```sh
    sudo add-apt-repository 'deb https://apt.corretto.aws stable main'
```

```sh
    sudo apt-get update; sudo apt-get install -y java-11-amazon-corretto-jdk
```

```sh
    wget https://archive.apache.org/dist/kafka/3.0.0/kafka_2.13-3.0.0.tgz
```

```sh
    tar xzf kafka_2.13-3.0.0.tgz
```

### ZOOKEEPER RUN

```sh
    ./zookeeper-server-start.sh ../config/zookeeper.properties
```

### KAFKA RUN

```sh
    ./kafka-server-start.sh ../config/server.properties
```
### KAFKA UTILITIES RUN

#### TOPICS

```sh
    ./kafka-topics.sh --list --bootstrap-server localhost:9092
```


```sh
    ./kafka-topics.sh -create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic tp-test
```

```sh
    ./kafka-topics.sh --describe --bootstrap-server localhost:9092 --topic tp-test
```

```sh
   ./kafka-topics.sh --alter --bootstrap-server localhost:9092 --topic tp-test --partitions 2
```

```sh
    ./kafka-topics.sh --delete --bootstrap-server localhost:9092 --topic tp-test
```

```sh
    ./kafka-configs.sh --alter --bootstrap-server localhost:9092 --entity-type topics --entity-name tp-test --add-config retention.ms=1000
```

#### PRODUCERS

```sh
    ./kafka-console-producer.sh --broker-list localhost:9092 --topic tp-test
```

```sh
    ./kafka-console-producer.sh --broker-list localhost:9092 --topic tp-test --property parse.key=true --property key.separator=;
```
#### CONSUMERS

```sh
    ./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic tp-test --from-beginning
```

```sh
    ./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic tp-test --from-beginning --property print.key=true --property key.separator=;
```
#### CONSUMER GROUPS

```sh
   ./kafka-consumer-groups.sh --list --bootstrap-server localhost:9092 
```

```sh
   ./kafka-consumer-groups.sh --bootstrap-server localhost:9092 --group cgp-test --reset-offsets --to-earliest --topic tp-test --execute
```

```sh
  ./kafka-consumer-groups.sh --describe --group cgp-test --bootstrap-server localhost:9092
``` 


```sh
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic tp-test --from-beginning --group cgp-test
``` 
### Dependencies

- [--]()
