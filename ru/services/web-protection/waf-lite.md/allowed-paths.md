---
id: 284
seoTitle: Разрешенные пути WAF Lite
seoDescription: Добавление разрешенных путей для WAF Lite
displayName: Разрешенные пути WAF Lite
order: 4
published: true
historyName: Разрешенные пути WAF Lite
historyDescription: Описание функционала добавления разрешенных путей WAF Lite, который разрешает доступ для конкретных путей
category: WAF Lite
---

# [Разрешенные пути WAF Lite](allowed-paths-for-waf-lite)

Разрешенные пути — это список URI (адресов или маршрутов внутри веб-приложения), к которым WAF Lite разрешает доступ без проверки.

### [Как настроить разрешенные пути для WAF Lite](how-to-edit-allowed-paths-for-waf-lite)

Как это работает:

1. Вы указываете в личном кабинете Solar Space  домен и разрешенные пути для него.
2. WAF Lite анализирует путь (URI) входящих HTTP-запросов и сравнивает его с заранее заданным списком разрешенных путей.
3. Если путь входит в этот список, сервис пропускает запрос без проверки.

Разрешенные пути позволяют:

- Уменьшить нагрузку на сервер: если известно, что определенные пути безопасны, можно настроить их пропуск без дополнительной проверки, что снизит нагрузку на систему безопасности и ускорит обработку запросов
- Снизить количество ложных срабатываний, если легитимные действия пользователей или автоматизированных сервисов не вписываются в типовые шаблоны поведения

### [Как добавить разрешенные пути в личном кабинете](how-to-add-allowed-paths-at-personal-account)

Для добавления разрешенных путей выполните следующие действия:

1. Перейдите на вкладку [Веб-защиты]([240]).
![wp-for-allowed-paths (95%)](https://img.solarspace.pro/docs/wp-for-allowed-paths.jpg "веб-защита для разрешенных путей")

2. Откройте нужный ресурс, нажав на его имя.
![choose-domain-for-allowed-paths (50%)](https://img.solarspace.pro/docs/choose-domain-for-allowed-paths.jpg "выберите домен для настройки разрешенных путей")

3. Перейдите на вкладку "WAF Lite" и выберите раздел "Разрешенные пути".
![allowed-paths-full (50%)](https://img.solarspace.pro/docs/allowed-paths-full.jpg "главная страница разрешенных путей")

4. Добавьте разрешенные пути вручную:

Нажмите на кнопку “Добавить”.

![tap-to-add-allowed-paths (50%)](https://img.solarspace.pro/docs/tap-to-add-allowed-paths.jpg "выбор домена для разрешенных путей")

Выберите домен, для которого добавляете разрешенные пути.

![choose-domain-for-adding-allowed-paths (50%)](https://img.solarspace.pro/docs/choose-domain-for-adding-allowed-paths.jpg "выбор домена для разрешенных путей")

Введите название пути в формате ```https://www.sitename.ru/folder/source/name```.

![adding-allowed-paths (50%)](https://img.solarspace.pro/docs/adding-allowed-paths.jpg "введите разрешенный путь")

Сохраните изменения.

![save-allowed-paths (50%)](https://img.solarspace.pro/docs/save-allowed-paths.jpg "сохранение разрешенных путей")


[//]: # (после выкатки на прод загрузки разрешенных путей файлом .csv, дополнить эту инструкцию с шагами)

