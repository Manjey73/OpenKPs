Драйвер приборов ЗАО НПФ Логика

пока тестовый вариант, только сборка, без исходников

При настройке приборов с протоколом СП Сеть через порт RS232 
Параметрs шаблона 
DevTemplate/Address = "false" или "no" (кавычки не вводятся) - Адрес прибора будет равен 128(dec) + Адрес прибора из БД Scada
При работе по RS485 в данном параметре задается собственный адрес сервера (целочисленное)

DevTemplate/readLastErr = "false"  запрещает выполнять очередные запросы при ошибке, "true" - выполняет следующие запросы шаблона.
Данная команда не работает в режиме шины RSbus, в ней при ошибке остальные запросы сессии прерываются.

DevTemplate/parDescrUse = "true" создаст имена Тегов с учетом описания параметра ParDescr + ParName, = "false" создаст имена тегов только по параметру ParName

ObjGroup/ObjName - является именем меню, создавая разные имена, создаются разные меню в окне КП Коммуникатора (одинаковые имена группируются в группы меню)

Групировка внутри меню выполняется так же по номеру сигнала ObjVal/Signal - номер сигнала указывается в БД Входных каналов

p.s.
Некоторые параметры не участвуют в драйвере, может со временем будут, а может быть нет. Например poolTime пока нигде не участвует.