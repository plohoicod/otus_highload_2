# otus_highload_1

Для запуска необходимо сбилдить приложение в JAR файл, развернуть контейнеры для приложения и базы данных с помощью команды:
```
docker-compose up
```

Приложение будет доступно по адресу `http://localhost:8081/`

JMetr план для запуска теста  - `Test Plan.jmx`

Миграция данных пользователей из файла `users.csv.zip` c помощью команды внутри psql:

```
\copy otus.users (login, password, name, surname, birthday, gender, interests, city) from '/Users/ydpolivt/IdeaProjects/otus_highload_2/users.csv' delimiter ',' csv header;
```