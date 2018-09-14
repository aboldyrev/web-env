# web-env
Конфигурация докера для разворачивания web-окружения

Состоит из:
 - dnsmasq
 - nginx
 - php 7.2-fpm
 - mariaDB
 - PHPMyAdmin
 
Переменные окружения:
 - MYSQL_ROOT_PASSWORD — пароль для root пользователя БД
 - PATH_TO_SITES — путь до папки с сайтами, которую нужно подключить
 - MYSQL_DB_PATH — путь до папки, где будут храниться базы данных (обычно `/var/lib/mysql`)
 - PHP_MY_ADMIN_PORT — порт для PHPMyAdmin