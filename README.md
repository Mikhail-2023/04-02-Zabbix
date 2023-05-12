# Домашнее задание к занятию "`Система мониторинга Zabbix`" - `Колобов Михаил`
---

### Задание 1

`Приведите ответ в свободной форме........`

1. ![01-02](screen/task_1/01-02.PNG)
2. ![01-03](screen/task_1/01-03.PNG)
3. ![01-03-01](screen/task_1/01-03-01.PNG)
4. ![01-03-02](screen/task_1/01-03-02.PNG)
5. ![01-03-03](screen/task_1/01-03-03.PNG)
6. ![01-03-04](screen/task_1/01-03-04.PNG)
7. ![01-03-05](screen/task_1/01-03-05.PNG)
8. ![01-03-06](screen/task_1/01-03-06.PNG)
9. ![01-03-07](screen/task_1/01-03-07.PNG)
10. ![01-03-08](screen/task_1/01-03-08.PNG)
11. 

`Текст использованных команд`

sudo apt install postgresql

systemctl status zabbix-server.service

su - postgres -c 'psql --command "CREATE USER zabbix WITH PASSWORD '\'123456789\'';"'

su - postgres -c 'psql --command "CREATE DATABASE zabbix OWNER zabbix;"'

find / -name zabbix_agentd.conf

find / -name zabbix_server.conf

sed -i 's/# DBPassword=/DBPassword=123456789/g' /etc/zabbix/zabbix_server.conf

systemctl restart zabbix-server apache2

systemctl enable zabbix-server zabbix-agent apache2
