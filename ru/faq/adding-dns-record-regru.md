---
id: 283
seoTitle: Добавление DNS-записей в регистраторе reg.ru
seoDescription: Пошаговая инструкция по добавлению DNS-записей в регистраторе reg.ru для работы сервисов защиты
displayName: Как добавить DNS-записи в регистраторе reg.ru?
order: 9
published: true
historyName: Как добавить DNS-записи в регистраторе reg.ru?
historyDescription: Инструкция по добавлению DNS-записей в регистраторе reg.ru
#category: FAQ
#categoryName: Как добавить DNS-записи в регистраторе reg.ru?
categoryDescription: Добавление DNS-записей в reg.ru
categoryOrder: 2
categoryIcon: https://img.solarspace.pro/docs/eye.svg
---

# [Как добавить DNS-записи в регистраторе reg.ru](how-to-add-dns-record-regru)


В этой статье описано, как добавить **A-запись** в настройках домена, зарегистрированного в reg.ru. Эта запись используется для перенаправления трафика через сервер защиты.

Если вы используете nic.ru, инструкция по добавлению DNS-записей [здесь]([282]).
Если вы используете другого провайдера, действия будут аналогичны, но названия разделов могут отличаться.

Войдите в личный кабинет reg.ru с вашим паролем и логином.

![log-in-regru (50%)](https://img.solarspace.pro/docs/log-in-regru.jpg "Вход в reg.ru")

Нажмите на **«Хостинг»** в левом меню или в разделе **«Мои услуги»** на главной странице.

![choose-way-to-hosting (95%)](https://img.solarspace.pro/docs/choose-way-to-hosting.jpg "Путь к управлению хостингом")

Оба пути переведут вас на страницу «Хостинги». Нажмите на три точки справа в строке вашего хостинга и выберите **«Панель управления»**.

![hostings-&-control-panel-regru (95%)](https://img.solarspace.pro/docs/hostings-&-control-panel-regru.jpg "Панель управления хостингом")

В открывшейся панели выберите **«Управление DNS»**. Откроется список доменов.

![control-dns-records-create-record-regru (95%)](https://img.solarspace.pro/docs/control-dns-records-create-record-regru.jpg "Создать DNS-запись")

Кликните на название нужного домена, чтобы открыть страницу с DNS-записями. Нажмите **«Создать запись»**.

![control-dns-records-create-record-regru1 (95%)](https://img.solarspace.pro/docs/control-dns-records-create-record-regru1.jpg "Создать DNS-запись")

Вы увидите форму создания новой записи.

![new-dns-record-regru (95%)](https://img.solarspace.pro/docs/new-dns-record-regru.jpg "Добавление DNS-записей")

### [Добавление A-записи](adding-a-record)

* **Имя** — введите имя домена
* **TTL** — введите время хранения записи в кэше (например, `300` секунд)
* **Тип** — выберите **A (адрес Internet v4)**
* **IP-адрес** — вставьте полученный IP-адрес

Нажмите **«Создать»**.

![new-domain-record-dns-a-regru (50%)](https://img.solarspace.pro/docs/new-domain-record-dns-a-regru.jpg "Добавление DNS-A-записи")

Все остальные A-записи и AAAA-записи в таблице необходимо удалить, чтобы весь входящий трафик шёл через сервер защиты.

![done-dns-records (95%)](https://img.solarspace.pro/docs/done-dns-records.jpg "Подтверждение DNS-записей")

