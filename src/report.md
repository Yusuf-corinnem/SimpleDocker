# REPORT
## Part 1. Готовый докер
- Выкачка docker-образа nginx:\
![pull](scr/p1/1.png)
- Проверка наличия образа:\
![images](scr/p1/2.png)
- Запуск образа:\
![start](scr/p1/3.png)
- Проверка запуска образа:\
![check_start](scr/p1/4.png)
- Вызов команды `docker inspect determined_newton`:
    - Размер контейнера: "ShmSize": 67108864
    - Список замапленных портов: "80/tcp": null
    - Ip контейнера: "IPAddress": "172.17.0.3"
- Остановка образа:\
![stop](scr/p1/5.png)
- Проверка остановки:\
![check_stop](scr/p1/6.png)
- Запуск с портами 80 и 443:\
![start_80_443](scr/p1/7.png)
- localhost:80:\
![nginx](scr/p1/8.png)
- Перезапуск контейнера:\
![restart_container](scr/p1/9.png)
- Проверка запуска контейнера:\
![check_start_container](scr/p1/10.png)

## Part 2. Операции с контейнером
- Содержимое файла nginx.conf:\
![nginx.conf](scr/p2/1.png)
- Создание на локальной машине файла nginx.conf:\
![create_nginx.conf](scr/p2/2.png)
- Настройка /status:\
![/status](scr/p2/3.png)
- Копирование nginx.conf:\
![cp_nginx.conf](scr/p2/4.png)
- Перезапуск nginx:\
![reload_nginx](scr/p2/5.png)
- Страница со статусом:\
![status](scr/p2/6.png)
- Экспорт контейнера:\
![export](scr/p2/7.png)
- Остановка контейнера:\
![stop](scr/p2/8.png)
- Удаление образа, не удаляя перед этим контейнеры:\
![rm_image](scr/p2/9.png)
- Удаление остановленного контейнера:\
![rm_container](scr/p2/10.png)
- Импорт контейнера:\
![import](scr/p2/11.png)
- Запуск импортированного контейнера:\
![start_import](scr/p2/12.png)
- Проверка адреса localhost:80/status:\
![check_status](scr/p2/13.png)

## Part 3. Мини веб-сервер
- Команды для установки необходимого: `apt update; apt install gcc -y; apt install spawn-fcgi -y; apt install libfcgi-dev -y; apt install vim -y`
- Мини-сервер:\
![miniserver](scr/p3/2.png)
- Страница localhost:81:\
![localhost:81](scr/p3/1.png)

## Part 4. Свой докер
- Сбор исходников:\
![src](scr/p4/1.png)
- Запуск и `docker build`:\
![build](scr/p4/2.png)
- Проверка `docker images`:\
![images](scr/p4/3.png)
- Проверка мини-сервера:\
![check_miniserver](scr/p4/4.png)
- Перезапуск:\
![restart](scr/p4/5.png)
- Статус сервера:\
![status](scr/p4/6.png)

## Part 5. Dockle
- dockerfile:\
![file](scr/p5/1.png)
- `build` и `dockle`:\
![dockle](scr/p5/2.png)

## Part 6. Базовый Docker Compose
- Поднятие контейнера:\
![up](scr/p6/1.png)
- Остановка контейнеров:\
![down](scr/p6/2.png)
- Вывод:\
![output](scr/p6/3.png)
- docker-compose.yml:\
![yml](scr/p6/4.png)