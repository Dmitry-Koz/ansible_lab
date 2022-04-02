В этой ветке находится ansible, которая устанавливает nginx на виртуальных машинах web1, web2, robin
устанавливает порт 8080 для nginx на серверах web1, web2 и генерирует кастомную страницу, зайдя на которую можно понять на каком сервере вы находитесь. Также на сервере robin настраивает балансировку нагрузки серверов web1 и web2 в режиме round-robin
<ul>
<li>nginx.yml - playbook<li/>
<li>ansible.cfg  конфигурационный файл ansible<li/>
<li>inventory    inventory файл<li/>
index.html.j2  кастомная страница html
nginx_port.conf.j2  конфигурационный файл для смены портов nginx
nginx_server.conf.j2  конфигурационный файл для настройки балансировки 
<ul/>

asible-playbook nginx.yml команда для запуска  playbook
