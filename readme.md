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
 - php — ``alias php71="docker exec -it php7.1 php"`` (команда будет не php, а php71)
 - composer — ``alias composer="docker exec -it php7.1 composer"``
 - mysql — ``alias mysql="docker exec -it mariadb mysql"``
 - mysqldump — ``alias mysqldump="docker exec -it mariadb mysqldump"``
 - npm — ``alias npm="docker run -it node npm"``
 - yarn — ``alias yarn="docker run node yarn"``
 
Все необходимые алиасы необходимо добавить в файл в домашней директории:
 - Linux — .bashrc или .zsh
 - MacOS — .bash_profile или .zsh