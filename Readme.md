<h1>Лабораторная работа №4</h1>

В этой ветке находится ansible, которая устанавливает nginx на виртуальных машинах web1, web2, robin
устанавливает порт 8080 для nginx на серверах web1, web2 и генерирует кастомную страницу, зайдя на которую можно понять на каком сервере вы находитесь. Также на сервере robin настраивает балансировку нагрузки серверов web1 и web2 в режиме round-robin

+ nginx.yml - playbook
+ ansible.cfg  конфигурационный файл ansible
+ inventory    inventory файл
+ index.html.j2  кастомная страница html
+ nginx_port.conf.j2  конфигурационный файл для смены портов nginx
+ nginx_server.conf.j2  конфигурационный файл для настройки балансировки

<h3> Порядок действий </h3> <br/>
Команда для поднятия виртуальных машин<br/>
vagrant up
Команда для запуска playbook
[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%2336BCF7&lines=vagrant+up)](https://git.io/typing-svg)
