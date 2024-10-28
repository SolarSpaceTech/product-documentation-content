---
id: 234
title: Вкладка - WAF Lite
displayName: WAf Lite
order: 3
published: true
historyName: WAF Lite
historyDescription: Защита от взлома сайта
category: Сервисы
categoryName: WAF Lite
categoryDescription: Защита от взлома сайта
categoryOrder: 7
categoryIcon: https://img.solarspace.pro/docs/waf.svg
---

# [Вкладка "WAF Lite"](waf-lite)
На странице сервиса WAF Lite вы можете прочитать краткое описание и подключить его  

Если вы выбрали версию защиты, в состав которой входит WAF Lite, то ползунок на этой странице уже находится в состоянии "Подключено"    
Вы можете активировать WAF Lite при условии, что у вас уже активированы сервисы AntiDDoS и Antibot  
Если сервис отключен, вы увидите текст: "WAF Lite подключен, но не работает, потому что вы выключили Antibot"

![WAF Lite (80%|left)](https://img.solarspace.pro/docs/field-waf.jpg "waf-lite")

На странице сервиса есть список типов атак, защиту от которых обеспечивает WAF Lite 

![protection-from-types-of-attacks (80%|left)](https://img.solarspace.pro/docs/protection-from-types-of-attacks-waf.jpg "Защита от типов атак")

В блоке "Заблокированные атаки" расположены кнопки "Заблокированные атаки" и "Список исключений". При нажатии на них можно просмотреть подробную информацию

![blocked-requests (80%|left)](https://img.solarspace.pro/docs/blocked-attacks-waf.jpg "Заблокированные атаки")


### [Заблокированные атаки](blocked-attacks)

При нажатии на кнопку “Заблокированные атаки” вы перейдете на страницу заблокированных сервисом атак. По умолчанию откроется список за последние сутки, но период можно изменить. Если система не зафиксировала атак за этот период, вы увидите сообщение "Угроз, соответствующих настройкам фильтра, не найдено"

![threats-not-found (80%|left)](https://img.solarspace.pro/docs/threats-not-found-blocked-attacks.jpg "Угрозы не найдены")

В первом поле можно выбрать ресурсы, для которых будет отображаться отчет

![list-of-domains (80%/left)](https://img.solarspace.pro/docs/all-domains-blocked-attacks.jpg "Список доменов")

Во втором поле можно изменить период отображения отчета. После выбора вы увидите список атак за нужные даты

![blocked-attacks-report-period (80%|left)](https://img.solarspace.pro/docs/time-blocked-attacks.jpg "Период отчета о заблокированных атаках")

В третьем поле можно изменить часовой пояс. Выберите "Локальный часовой пояс" или "UTC + 00"

![timezone-of-blocked-attacks (80%|left)](https://img.solarspace.pro/docs/timezone-blocked-attacks.jpg "Выбор часового пояса")

Список заблокированных атак:

![list-of-blocked-attacks (80%|left)](https://img.solarspace.pro/docs/all-attacks-blocked-attacks.jpg "Список заблокированных атак")

Краткая информация об атаке отражается в следующих полях:

- Дата – дата совершения атаки на ресурс

- Домен – домен, подвергшийся атаке

- Путь – по какому пути была совершена атака

- Сообщение об атаке – название типа атаки

- Код ответа – код ответа WAF Lite на совершенную атаку

- Тип запроса – метод совершения атаки

Для всех полей кроме “Сообщения об атаке” доступна сортировка по возрастанию/убыванию.

Для просмотра подробной информации об атаке нажмите на стрелочку в правой части строки или на иконку троеточия для вызова меню

![buttons-blocked-attack (80%|left)](https://img.solarspace.pro/docs/buttons-blocked-attacks.jpg "Кнопки в строке заблокированной атаки")

![two-buttons-of-blocked-attack (30%)](https://img.solarspace.pro/docs/description-buttons-blocked-attacks.jpg "Описание кнопок заимодействия с заблокированной атакой")

При нажатии на стрелочку или на пункт меню "Подробнее" в правой части экрана откроется окно с информацией об атаке

![detail-info-about-blocked-attack (80%|left)](https://img.solarspace.pro/docs/attack-info-blocked-attacks.jpg "Подробная информация о заблокированной атаке")

Если нажмете "Закрыть", окно закроется. Если нажмете "Разрешить данный запрос", он пропадет из списка заблокированных атак и в дальнейшем не будет блокироваться при условии, что придет по тому же пути. Также вы можете выбрать вариант "Разрешить данный запрос", не открывая это окно. Достаточно нажать на три точки в строке атаки и кликнуть по второму пункту в появившемся меню

### [Список исключений](list-of-exceptions)

Список разрешенных запросов вы найдете в разделе "Список исключений" на вкладке WAF Lite

![list-of-exceptions (80%|left)](https://img.solarspace.pro/docs/list-of-exceptions.jpg "Список исключений")

Запрос можно удалить из списка разрешенных. Для этого нажмите на иконку корзины справа в строке

![button-for-deleting-exception (80%|left)](https://img.solarspace.pro/docs/delete-exceptions.jpg "Удаление исключения")

Для быстрого перемещения между страницами нажмите на кнопку "Список исключений" или "Заблокированные атаки" в правой верхней части страницы.  
Название кнопки будет отличаться в зависимости от того, на какой странице вы сейчас находитесь

![button-exceptions (80%|left)](https://img.solarspace.pro/docs/button-exceptions.jpg "Кнопка Список исключений")

![button-blocked-attacks (80%|left)](https://img.solarspace.pro/docs/button-attacks.jpg "Кнопка Заблокированные атаки")

Если вы не добавили ни одно исключение, при переходе в "Список исключений" вы увидите надпись "Исключений не найдено"

![exceptions-not-found (80%|left)](https://img.solarspace.pro/docs/not-found-exceptions.jpg "Исключений не найдено")


### [Защита от типов атак](protection-from-types-of-attacks)

1. Scanner Detection
2. HTTP protection
3. Local File Inclusion (LFI)
4. Remote File Inclusion (RFI)
5. Remote Code Execution (RCE)
6. PHP Injection (PHPi)
7. Generic Attack
8. Cross Site Scripting (XSS)
9. SQL Injection (SQLi)
10. Session Fixation
11. JAVA
12. Leakaages
13. Leakages-SQL
14. Leakages-JAVA
15. Leakages-PHP
16. Leakages Microsoft IIS
17. WEB shells
