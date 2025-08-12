---
id: 215
seoTitle: Целевой IP — Solar Space
seoDescription: Как настроить IP-адреса вашего ресурса. Как настроить несколько IP-адресов в личном кабинете. Как удалить IP-адреса вашего ресурса — пошаговая инструкция Solar Space
displayName: Целевой IP
order: 2
published: true
historyName: Целевой IP
historyDescription: Инструкция по добавлению IP-адресов и настройка балансировки трафика с дополнительными функциями
category: Настройка ресурсов
categoryName: Целевой IP
categoryDescription: Настройка целевого IP-адреса ресурса и балансировка трафика
categoryOrder: 2
categoryIcon: https://img.solarspace.pro/docs/ip-settings.svg
---




# [Целевой IP](ip-settings)

Раздел **Целевой IP** позволяет управлять IP-адресами ресурса и настраивать балансировку трафика.

![Web protection IP (95%)](https://img.solarspace.pro/docs/on-prem/web-protection/settings/web-protection-ip.png "Веб-защита — добавление IP")

## [Добавление IP-адреса](adding-ip)

1. Перейдите в раздел **Целевой IP**.
2. Нажмите **Добавить IP**.
3. Заполните поле **IPv4** (адрес должен отличаться от уже существующих).
4. Настройте дополнительные параметры:

   * **Тип** — основной или запасной. Запасной IP используется при недоступности основного.
   * **Вес** — число от 1 до 100, определяющее приоритет IP при распределении трафика.
   * **Ошибки** — количество допустимых ошибок до пометки IP как недоступного.
   * **Пауза** — время в секундах до повторной попытки подключения.
5. Нажмите **Сохранить**.

> **INFO**
> При вводе уже существующего IP система отобразит предупреждение.

![Web protection for adding IP (95%)](https://img.solarspace.pro/docs/on-prem/web-protection/settings/web-protection-for-adding-ip.png "Веб-защита — добавление IP")

## [Дополнительные функции](additional-functions)

Если задан один IP, доступна настройка **Портов IP-адреса**:

* **По умолчанию** — зависит от настройки "Редирект на HTTPS".
* **HTTP (80)** — передача данных в открытом виде.
* **HTTPS (443)** — передача данных в зашифрованном виде.

![Web protection for IP ports (95%)](https://img.solarspace.pro/docs/on-prem/web-protection/settings/web-protection-for-ip-ports.png "Веб-защита — порты IP")

Если задано несколько IP, становится доступна функция **IP-hash** — алгоритм балансировки нагрузки, при котором все запросы от одного IP-адреса направляются на один и тот же сервер.

Это особенно важно для веб-сервисов с пользовательскими сессиями: онлайн-магазинов, личных кабинетов и других приложений, где нужно сохранять состояние сеанса. Благодаря IP-hash пользователь продолжает работу без необходимости повторной авторизации.

![Web protection for IP-hash (95%)](https://img.solarspace.pro/docs/on-prem/web-protection/settings/web-protection-for-ip-hash.png "Веб-защита — IP-hash")

> **INFO**
> IP-hash доступен только при использовании IP с типом "Основной".

## [Удаление IP-адреса](deleting-ip)

![Web protection for deleting IP (95%)](https://img.solarspace.pro/docs/on-prem/web-protection/settings/web-protection-for-deleting-ip.png "Веб-защита — удаление IP")

1. Нажмите значок корзины рядом с IP.
2. Нажмите **Сохранить**.
3. Для восстановления используйте кнопку **Отменить** или значок стрелки.



