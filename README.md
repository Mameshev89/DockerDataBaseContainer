# Задача №1 - PostgreSQL

Вам необходимо подготовить приложение к тестированию на СУБД PostgreSQL (используйте образ 12-alpine, если он недоступен, то берите последний опубликованный на DockerHub). Возьмите собранный jar-файл db-api.jar, аналогично примеру на лекции положите рядом файл application.properties, но в строке: jdbc:mysql://... поменяйте mysql на postgresql.

Вам нужно дописать остальные настройки (хост, порт, БД, имя пользователя и пароль).

Кроме того, вам нужно подготовить файл docker-compose.yml, в котором прописать настройки для запуска контейнера PostgreSQL. Всю информацию о его (контейнера) запуске вы найдёте на официальной странице образа на Docker Hub.

Запустите сначала docker-compose up и только после того, как БД запустится, запустите целевое приложение: java -jar db-api.jar (если нужно поменять порт запуска, по умолчанию он 9999, то добавьте в файл application.properties строку server.port=<нужный номер порта>).

Если вы сделали всё правильно, то приложение запустится и на GET http://localhost:9999/api/cards выдаст вам JSON с картами:
  

![](Screenshot_96.png)



