В данной сборке используется база данных Postgresql!!!


Перед запуском контейнеров нужно создать файл инициализации для базы данных.

Если используется Postgresql:

docker run --rm guacamole/guacamole /opt/guacamole/bin/initdb.sh --postgresql > ./docker/postgresql/initdb.sql

Если используется MySql/MariaDB

docker run --rm guacamole/guacamole /opt/guacamole/bin/initdb.sh --mysql > ./docker/mariadb/initdb.sql

После выполнения команды для создания файла инициализации выполняем команду docker compose up -d


Образ guacamole будет доступен по адресу http://[адрес контейнера][8087 или установленный в docker-compose.yaml]/guacamole/

Логин по умолчанию: guacadmin
Пароль по умолчанию: guacadmin
