---
id: 215
title: Вкладка - Настройки IP-адресов
displayName: Настройки IP-адресов
order: 6
published: true
historyName: Настройки IP-адресов
historyDescription: Защита от ботнет атак
category: Настройка ресурсов
categoryName: Настройки IP-адресов
categoryDescription: Защита от ботнет атак
categoryOrder: 2
categoryIcon: https://img.solarspace.pro/docs/icon_06.svg
---

# [Вкладка Настройки IP](ip-settings)

![ip settings (80%|left)](https://img.solarspace.pro/docs/field-ip-settings.jpg "Вкладка Настройки IP")

Нажмите "Добавить IP" для добавления IP-адреса вашего ресурса.
Если у вас несколько IP-адресов, вы увидите форму расширенных настроек с возможностью добавить новый IP и подключить расширенный функционал.

Откроется страница настроек IP, где все поля предзаполнены по умолчанию, кроме поля "IPv4".
Если у вас есть дополнительный IP-адрес, его нужно ввести в это поле.
Появится строка с полями для вашего IP-адреса.

![add ip address (80%|left)](https://img.solarspace.pro/docs/add-ip-settings.jpg "Добавление IP-адреса")


Все предзаполненные поля можно редактировать:

- **Тип** – выберите из выпадающего списка "Основной или "Запасной". По умолчанию установлен "Основной". Если вы установите "Запасной" (резервный), он подключится только при недоступности основного IP-адреса

<br/>

- **Вес** – значение от 1 до 100, которое отражает приоритет IP-адреса в рамках защиты от атак. Чем важнее и критичнее для вашего бизнеса доступность конкретного IP-адреса, тем выше должен быть его вес. Например, если у вас два IP-адреса, доступность которых одинаково важна, то в поле "Вес" для каждого должно быть значение "50". Если для одного поставить значение "70", а для другого "30", то система защиты будет направлять больше трафика на IP-адрес с бОльшим весом

<br/>

- **Ошибки** – значение от 1 до 10 000, которое отражает количество допустимых ошибок при соединении с сервером. При превышении количества ошибок система пометит сервер недоступным и не будет переводить на него трафик. По умолчанию установлено "0", то есть при первой же ошибке соединения система присвоит серверу статус "Недоступен"

<br/>

- **Пауза** – значение от 1 до 1800, обозначает время в секундах, через которое система попытается повторно восстановить соединение с сервером, помеченным статусом “Недоступен”



После этого нажмите кнопку "Сохранить" в нижней части страницы

![save ip-address (80%|left)](https://img.solarspace.pro/docs/save-ip-settings.jpg "Сохранение нового IP-адреса")

Если в поле ввода IP-адреса ввести уже существующий IP-адрес, отобразится соответствующая надпись о том, что такой IP-адрес уже есть.

![ip exist (80%|left)](https://img.solarspace.pro/docs/double-ip-settings.jpg "Уведомление о существующем IP-адресе")

Если у вас один IP-адрес, то в правой части страницы будет раздел "Дополнительные функции", с возможностью настроить блок "Порты IP-адресов".

Порты установлены "По умолчанию", если вам нужно, вы можете изменить этот параметр на HTTP или HTTPS. Порты IP-адресов определяют, через какой порт будет устанавливаться соединение с сервером-источником. Доступны три варианта: "По умолчанию", "HTTP 80", "HTTPS 443".

![advanced feauters with 1 ip (80%|left)](https://img.solarspace.pro/docs/port-ip-settings.jpg "Дополнительные функции, если IP-адрес один")


- **Порт 80** поддерживает протокол HTTP – информация передается между браузером и сервером в виде обычного текста, что небезопасно

<br/>

- **Порт 443** поддерживает протокол HTTPS – информация, передаваемая между сервером и браузером, зашифровывается, что повышает безопасность обмена данными

<br/>

- **По умолчанию** – означает, что если на вкладке "Домен и SSL" у вас включен расширенный функционал "Редирект на HTTPS", то трафик проходит через безопасный порт 443. Если настройка "Редирект на HTTPS" на вкладке "Домен и SSL" у вас отключена, то трафик проходит через незащищенный порт 80


Если у вас несколько IP-адресов, то в правой части экрана отображается окно с еще одной дополнительной функцией: IP-hash. При введении нескольких IP-адресов с типом "Основной", она сразу будет активной.

![ip hash (80%|left)](https://img.solarspace.pro/docs/ip-hash-ip-settings.jpg "IP-hash")

IP-hash – это метод распределения нагрузки между серверами. Он гарантирует, что пользователь с конкретным IP подключится к тому же серверу, с которым работал ранее. Этот алгоритм часто используют для веб-приложений, поскольку в них пользователь взаимодействует с интерфейсом, – например, заходит в личный кабинет, добавляет товары в корзину. При использовании IP-hash балансировки пользователь подключится к тому же сеансу: ему не понадобится снова заходить в личный кабинет.

> **INFO**
> #### Обратите внимание
> Функция IP-hash доступна, если все введенные IP-адреса имеют тип "Основной"

Для удаления IP нажмите на иконку корзины в строке с нужным адресом, в обновленной странице нажмите кнопку "Сохранить".

Если необходимо вернуть удаленный ресурс, нажмите кнопку "Отменить".

![change deleted ip (80%|left)](https://img.solarspace.pro/docs/cancel-or-save-deleted-ip.jpg "Сохранение или отмена удаленного IP-адреса")