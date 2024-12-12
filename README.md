# Kafka Training

![Badge de Licença](https://img.shields.io/badge/.NET-8.0.0-blue.svg?style=flat-square&logo=dotnet)
![Badge de Licença](https://img.shields.io/badge/Kafka-0.0.0-orange.svg?style=flat-square&logo=kafka)
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

### KAFKA RUN

### Dependencies

- [StackExchange.Redis 2.8.22]()
