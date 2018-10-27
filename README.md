## Мониторинг соединений к базам 1С Предприятия средствами Zabbix

Для обнаружения баз используется LLD Zabbix, используемая версия 4.0, но в принципе должно работать и на 3.4, ниже не получится, используются зависимые элементы данных.

Описание подготовлено для операционной системы Windows.

Для получения информации используются консольные утилиты RAS (сервер) и RAC (клиент).
Для установки сервера в качестве службы используется команда:

`sc create "1C:Enterprise RAS" binpath= "C:\Program Files\1cv8\Х.Х.Х.ХХХХ\bin\ras.exe cluster --service" displayname= "1C:Enterprise RAS" start= auto` 

Для запуска - команда:

`net start "1C:Enterprise RAS"`

Шаблон для Zabbix: 1c-zabbix.xml

На текущий момент снимаются количество сеодинений к каждой базе и к кластеру в целом.
