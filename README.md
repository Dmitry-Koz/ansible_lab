<h1> Лабораторная №5 </h1>
В этой ветке лежит Ansible со следующим функционалом:

<ul>
<li>Устанавливает на серверах web1 web2 nginx</li>
<li>На серверах haproxy1, haproxy2 устанавливает и настраивает  отказоустойчивую связку HAProxy+Keepalived</li>
<li>На серверах web1, web2 Nginx работает по порту 8080 и отдает кастомную страницу</li>
<li>На серверах с HAProxy ПО обеспечивает балансировку нагрузки серверов web1 и web2 в режиме round-robin.</li>
</ul>
Структура файлов:

<ul>
<li>Vagrantfile - конфигурациооный файл с виртуальными машинами</li>
<li>index.yml - основной playbook который запускает роли</li>
<li>inventory - инвентори файл</li>
<li>proxy - папка с ролью для серверов группы server</li>
<li>web - папка с ролью для web</li>
<li>play.yml старый playbook без ролей (нужно допилить) </li>
</ul>

Для поднятия виртуалок команда:

[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%2336BCF7&lines=vagrant+up)](https://git.io/typing-svg)

Команда для запуска Ansible: 

[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%2336BCF7&lines=ansible-playbook+index.yml)](https://git.io/typing-svg)

<h3>Работа балансировки:</h3>

<img src="./ img/img5.1.png"/>

<img src="./ img/img5.2.png"/>

<h3>Проверка отказоустойчивости</h3>
<h4>Отключим master сервер, на котором работает страница, резервный сервер становиться master, страница продолжает работать</h4>

<img src="./ img/img5.3.png"/>

<img src="./ img/img5.4.png"/>

<img src="./ img/img5.1.png"/>
