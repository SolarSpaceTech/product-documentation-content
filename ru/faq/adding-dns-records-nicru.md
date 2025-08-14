---
id: 282
seoTitle: Добавление DNS-записей в nic.ru
seoDescription: Пошаговая инструкция по добавлению DNS-записей в регистраторе nic.ru для работы сервисов защиты
title: Как добавить DNS-записи в регистраторе nic.ru?
displayName: Как добавить DNS-записи в регистраторе nic.ru?
order: 8
published: true
historyName: Добавление DNS-записей в nic.ru Как добавить DNS-записи в регистраторе nic.ru?
historyDescription: Инструкция по добавлению DNS-записей в регистраторе nic.ru
category: FAQ
categoryOrder: 2
categoryIcon: https://img.solarspace.pro/docs/eye.svg
---

# [Как добавить DNS-записи в регистраторе nic.ru](how-to-add-dns-record-by-nicru)


В этой статье описано, как добавить **A-запись** в настройках домена, зарегистрированного в nic.ru. Эта запись используется для перенаправления трафика через сервер защиты.

Если вы используете reg.ru, инструкция по добавлению DNS-записей [здесь]([283]).
Если вы используете другого провайдера, действия будут аналогичны, но названия разделов могут отличаться.

Войдите в личный кабинет nic.ru с вашим паролем и логином (номер договора NIC-D или NIC-REG).

![log-in-nicru (50%)](https://img.solarspace.pro/docs/log-in-nicru.jpg "Вход в nic.ru")

Перейдите в раздел **«DNS-хостинг»**, где находятся настройки управления вашим хостингом и ресурсными записями.

![dns-hosting-nicru (95%)](https://img.solarspace.pro/docs/dns-hosting-nicru.jpg "DNS-хостинг")

В столбце **«Состояние»** должен быть статус «Предоставляется». Это значит, что DNS-хостинг подключен к домену, и вы можете управлять записями. Нажмите **«Управление DNS-зонами»** под названием услуги.

![dns-zone-management-nicru (50%)](https://img.solarspace.pro/docs/dns-zone-management-nicru.jpg "Управление DNS-зонами")

Проверьте, что имя домена в столбце **«Домены на услуге»** соответствует редактируемому DNS-хостингу. Затем нажмите на название домена.

![click-on-domain-nicru (50%)](https://img.solarspace.pro/docs/click-on-domain-nicru.jpg "Имя домена")

Откроется страница **«Ресурсные записи»**.

![add-new-dns-record-nicru (95%)](https://img.solarspace.pro/docs/add-new-dns-record-nicru.jpg "Добавление новой DNS-записи")

### [Добавление A-записи](adding-a-record)

Нажмите **«Добавить новую запись»**.

![dns-records-page (95%)](https://img.solarspace.pro/docs/dns-records-page.jpg "Ресурсные записи")

В форме укажите:

* **Name** — имя домена
* **Type** — выберите **A**
* **IP address** — введите IP-адрес, предоставленный для перенаправления трафика
* **TTL** — время хранения записи в кэше (например, `300` секунд)

Нажмите **«Добавить»**.

![dns-a-record-nicru (50%)](https://img.solarspace.pro/docs/dns-a-record-nicru.jpg "Добавление DNS-A-записи")

Нажмите **«Выгрузить зону»**.

![aproove-dns-a-record-nicru (95%)](https://img.solarspace.pro/docs/aproove-dns-a-record-nicru.jpg "Выгрузка DNS-зоны")

После выгрузки зоны изменения вступят в силу.

![done-dns-a-record-nicru (95%)](https://img.solarspace.pro/docs/done-dns-a-record-nicru.jpg "DNS-записи успешно загружены")

Удалите все лишние A- и AAAA-записи, чтобы весь входящий трафик направлялся на указанный сервер.

![done-dns-records (95%)](https://img.solarspace.pro/docs/done-dns-records.jpg "Подтверждение DNS-записей")

