# web-env
Конфигурация докера для разворачивания web-окружения

Состоит из:
 - nginx
 - php
 - node
 - mysql
 - phpmyadmin
 
Переменные окружения:
 - MYSQL_DB_PATH — путь до папки с базами
 - NGINX_LOGS_PATH — путь до папки логов NGINX (по умолчанию ./logs)
 - NGINX_PORT_HTTP — порт для протокола HTTP (по умолчанию 80)
 - NGINX_PORT_HTTPS — порт для протокола HTTPS (по умолчанию 443)
 
 
Список непоходимых алиасов:
 - php71 — ``alias php71="docker exec -it php7.1 php"``
 - composer71 — ``alias composer71="docker exec -it php7.1 composer"``
 - mysql — ``alias mysql="docker exec -it mariadb mysql"``
 - mysqldump — ``alias mysqldump="docker exec -it mariadb mysqldump"``
 - npm10 — ``alias npm="docker run -it aboldyrev/node:10.16.1 npm"``
 - yarn10 — ``alias yarn="docker run -it aboldyrev/node:10.16.1 yarn"``
 
Все нужные алиасы необходимо добавить в файл в домашней директории:
 - Linux — .bashrc или .zsh
 - MacOS — .bash_profile или .zsh
 
При необходимости перезагрузите терминал.