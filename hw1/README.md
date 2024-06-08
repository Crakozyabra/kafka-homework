# Домашнее задание № 1

<img src="hw1.png" alt="image is absent">

<p style="text-align: center;">Рис. 1</p>
На рис. 1:

* в первом консольном окне
    * Разархивирован файл с Kafka ```tar -xzf kafka_2.13-3.7.0.tgz```
    * Запущен Zookeeper ```bin/zookeeper-server-start.sh -daemon config/zookeeper.properties```
    * Запущена Kafka ```bin/kafka-server-start.sh -daemon config/server.properties```
    * Создан топик quickstart ```bin/kafka-topics.sh --create --topic quickstart --bootstrap-server localhost:9092```
    * Выведена информация о созданном топике ```bin/kafka-topics.sh --describe --topic quickstart --bootstrap-server localhost:9092```

* во втором консольном окне создан producer для созданного топика
```bin/kafka-console-producer.sh --topic quickstart --bootstrap-server localhost:9092``` и в
топик отправлено 2 сообщения

* в третьем консольном окне создан consumer для созданного топика
```bin/kafka-console-consumer.sh --topic quickstart --from-beginning --bootstrap-server localhost:9092``` и получено
2 сообщения из топика

* в четвертом консольном окне остановлены Kafka ```bin/kafka-server-stop.sh``` и Zookeeper ```bin/zookeeper-server-stop.sh```