# Домашнее задание № 2 (авторизация SASL_PLAINTEXT в режиме Kraft)

<img src="images/start-broker.png" alt="image is absent">

<p style="text-align: center;">Рис. 1</p>
На рис. 1 Запускается Kafka с Kraft: сгенерировано UUID кластера, отформатировваны папки для журналов, запущен брокер

<img src="images/create-topic-principal.png" alt="image is absent">

<p style="text-align: center;">Рис. 2</p>

На рис. 2 создан топик test. Первому пользователю (Bob) выданы права на запись в этот топик. Второму пользователю (Alice)
выданы права на чтение этого топика. Третьему пользователю (Client) не выданы никакие права на этот топик

<img src="images/list-producer-consumer.png" alt="image is absent">

<p style="text-align: center;">Рис. 3</p>

На рис. 3 От имени каждого пользователя выполны команды:
* Получить список топиков
* Записать сообщения в топик
* Прочитать сообщения из топика