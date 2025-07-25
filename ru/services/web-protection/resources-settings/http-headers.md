---
id: 214
seoTitle: HTTP-заголовки — что это такое, как работают, зачем нужны
seoDescription: HTTP-заголовки — это простой способ улучшить производительность сайта и повысить безопасность. Как работают HTTP-заголовки. Зачем вашему сайту HTTP-заголовки
displayName: HTTP-заголовки
order: 3
published: true
historyName: HTTP-заголовки
historyDescription: Что такое HTTP-заголовки, инструкция по добавлению HTTP-заголовков
category: Настройка ресурсов
categoryName: HTTP-заголовки
categoryDescription: Добавление HTTP-заголовков
categoryOrder: 3
categoryIcon: https://img.solarspace.pro/docs/http-settings.svg
---

# [HTTP-заголовки](http-headers)

> **INFO**
> **Обратите внимание**  
> Эта вкладка необязательна для заполнения. Если вы не используете HTTP-заголовки для своего сайта, их не нужно добавлять. Наличие или отсутствие HTTP-заголовков не влияет на эффективность работы наших сервисов защиты.

HTTP-заголовки — это простой способ улучшить производительность сайта и повысить безопасность. Правильные заголовки снижают риск распространенных веб-атак, таких как межсайтовый скриптинг или кликджекинг. В этой статье рассмотрим, что такое HTTP-заголовки, как они работают, и какие заголовки нужно добавить в ответы сервера, чтобы оптимизировать работу сайта и сделать взаимодействие пользователей с ним более безопасным.

### [Что такое HTTP-заголовки](what-is-http-headers)

Когда пользователь хочет открыть какой-то сайт, его браузер отправляет запрос к серверу этого сайта. Сервер принимает запрос, отправляет в ответ нужный сайт, и он открывается в браузере. Для пользователя это взаимодействие выглядит, как пара кликов. Для того, чтобы это стало возможным, браузер и сервер обмениваются служебной информацией с помощью HTTP-сообщений: запросов и ответов.

В каждом HTTP-сообщении содержится HTTP-заголовок, благодаря которому браузер пользователя и сервер сайта понимают, как им взаимодействовать друг с другом.

### [Как работают HTTP-заголовки](how-http-headers-works)

HTTP-заголовки запроса передают серверу информацию о том, какой именно ресурс хочет открыть пользователь, как он намерен с ним взаимодействовать: к примеру, посмотреть видео или скачать документ.

HTTP-заголовки ответов, которые отправляет сервер, тоже содержат информацию: название открываемого сайта, в каком формате пользователь получит данные и так далее. Если мы пытаемся открыть сайт и видим ошибку 404, это тоже ответ сервера. Таким образом он сообщает браузеру, что нужная нам страница не найдена. Это происходит, если владелец сайта ее удалил.

Каждый HTTP-заголовок состоит из двух частей: ключа (key) и значения (value).

Ключ представляет собой название заголовка, которое описывает передаваемую информацию (например, Content-Type). Значение уточняет параметры или инструкции для обработки запроса или ответа (например, text/html; charset=UTF-8).

| Key          | Value        | Что означает |
|:-------------|:-------------|:-------------|
| Connection   | keep-alive   | Заголовок указывает серверу, что соединение нужно оставить открытым: сервер не закроет соединение сразу после отправки ответа, и следующий запрос от этого же клиента к серверу будет выполнен быстрее.   |
| Cache-control    | no-cache, no-store, must-revalidate cервер    |  Сообщает клиенту, что кэширование контента веб-ресурса запрещено, и каждая его копия должна быть получена непосредственно с сервера.   |

В [личном кабинете](https://my.solarspace.pro/web-protection 'личный кабинет - веб-защита') Solar Space вы можете добавить HTTP-заголовки ответов, которые ваш сервер будет отправлять в ответ на запросы к нему. Далее приведем конкретные примеры заголовков, которые будут полезны для веб-ресурсов.

### [Зачем вашему сайту HTTP-заголовки](why-your-website-needs-headers)

HTTP-заголовки, добавленные в ответ сервера, положительно влияют:

1. На уровень безопасности. Они снижают риск атак, цель которых – завладеть данными пользователей и перехватить конфиденциальную информацию.
2. На управление сайтом. Существуют атаки, позволяющие полностью или частично перехватить управление веб-ресурсом и использовать его в своих целях. С помощью определенных HTTP-заголовков можно минимизировать риски таких атак.
3. На производительность веб-ресурса. Некоторые HTTP-заголовки помогают сайту работать быстрее, а серверу — эффективнее использовать мощности.

Разберем подробнее примеры заголовков для каждого из этих пунктов.

#### Безопасность
|    Key      |       Value       | Что означает |
|:------------|:------------------|:-------------|
| Strict-Transport-Security    | max-age=31536000; includeSubDomains        |     Этот заголовок указывает браузеру использовать только защищенный протокол HTTPS для соединений с этим доменом и всеми его поддоменами в течение одного года (31536000 секунд). max-age=31536000 – задаёт срок действия политики (в данном случае 1 год). includeSubDomains – применяет политику ко всем поддоменам текущего домена. Это защищает взаимодействие сайта и пользователя от атак типа «человек посередине», которые возможны при незащищенной передаче данных с помощью протокола HTTP. Во время таких атак злоумышленник перехватывает данные, которыми обмениваются сервер и клиент. |
| Content-Security-Policy    | default-src 'self'; script-src 'self   |  default-src 'self' – указывает, что все ресурсы (скрипты, стили, изображения и т.д.) могут загружаться только с собственного сервера. script-src 'self' – уточняет, что загружать и выполнять скрипты разрешено исключительно с того же домена. Это помогает предотвратить атаки типа XSS (межсайтовый скриптинг). Во время такой атаки в веб-страницу внедряется вредоносный скрипт, который начинает выполняться, как только пользователь открывает эту страницу. Целью таких атак обычно становятся личные данные пользователей. |

> **INFO**
> #### Обратите внимание
> Заголовок Content-Security-Policy нуждается в постоянном обновлении. Используйте его, если готовы поддерживать актуальность данных.

#### Управление сайом и политикой доступов

|    Key      |       Value       | Что означает |
|:------------|:------------------|:-------------|
| X-Frame-Options | SAMEORIGIN                         | Указывает, что встроить вашу веб-страницу или ее фрагмент можно только на вашем же домене. Если вместо SAMEORIGIN в поле значения указать DENY, то встраивание веб-страницы будет запрещено на любых ресурсах.  Обезопасит от атак вида clickjacking (кликджекинг): когда часть веб-страницы интегрируется на посторонний ресурс, настоящее содержимое которого будет невидимым для пользователя. Так вполне законопослушные сайты становятся орудием в руках мошенников. |
| X-XSS-Protection | 1; mode=block                     | Указывает браузеру, что нужно включить встроенную защиту от атак вида XSS (межсайтовый скриптинг). При обнаружении подозрительных скриптов браузер не будет пытаться их очистить, а сразу заблокирует. Защищает пользователей от кражи данных или других последствий XSS-атак. |

#### Повышение производительности

|    Key      |       Value       | Что означает |
|:------------|:------------------|:-------------|
| Cache-Control | public, max-age=3600 | Заголовок для управления кэшированием. Параметр public указывает, что сохранять ответ сервера можно в любом кэше – в браузере пользователя, на прокси-серверах или в сети доставки контента, если сайт использует ее. Параметр max-age=3600 сообщает, что ответ может быть сохранен на 3600 секунд (1 час). Это уменьшит количество запросов к серверу, так как браузер в течение часа будет использовать сохраненную копию веб-страницы, не обращаясь к серверу и не расходуя его ресурсы. |
| Content-Encoding | gzip | Этот заголовок указывает, что содержимое ответа сервера сжато с использованием алгоритма gzip. Браузер автоматически "разжимает" данные при получении, так что пользователь не заметит разницы, но страница загрузится быстрее. |

Добавьте эти заголовки в [личном кабинете](https://my.solarspace.pro/web-protection 'личный кабинет - веб-защита') Solar Space, чтобы повысить эффективность и безопасность вашего сайта.

### [Как работать с HTTP-заголовками в личном кабинете](how-to-work-with-http-headers-in-your-personal-account)

Чтобы открыть страницу "HTTP-заголовки" перейдите на страницу [Веб-защита]([https://my.solarspace.pro/web-protection]), нажав на иконку облака в левом меню с любой страницы личного кабинета.

![Web protection for http headers (95%)](https://img.solarspace.pro/docs/web-protection-for-http-headers.jpg "Веб-защита для перехода в HTTP-заголовки")

Откроется страница со списком ваших ресурсов. Выберите нужный вам ресурс, кликнув по нему.

![tap-on-domain-for-http-headers 55%](https://img.solarspace.pro/docs/tap-on-domain-for-http-headers.jpg "Нажмите на строку ресурса")

Или нажмите на три точки в правой части строки ресурса.

![three-dots-by-resource-for-http-headers 55%](https://img.solarspace.pro/docs/three-dots-by-resource-for-http-headers.jpg "Три точки для перехода в настройки ресурса")

Выберите "Настройки".

![choose-settings-for-http-headers 55%](https://img.solarspace.pro/docs/choose-settings-for-http-headers.jpg "Настройки для перехода в HTTP-заголовки")

Вы увидите страницу со стартовой вкладкой "Домен и SSL". Нажмите на вкладку "HTTP-заголовки"

![http-headers (95%)](https://img.solarspace.pro/docs/field-http-headers.jpg "Вкладка HTTP-заголовки")

На этой вкладке вы можете управлять HTTP-заголовками. Они сообщают серверу, какое желаемое действие нужно выполнить для конкретного ресурса. Если у вас еще нет ни одного заголовка, отображается кнопка "Добавить".

При нажатии на эту кнопку открывается форма с двумя обязательными полями для заполнения "Key" и "Value".
- **Key** — ключ заголовка
- **Value** — значение заголовка
![add key & value (95%)](https://img.solarspace.pro/docs/key-value-http-headers.jpg "Добавление параметров 'ключ значение'")

После заполнения полей "Key" и "Value" кнопка "Сохранить" станет активной. Нажмите на нее, чтобы сохранить HTTP-заголовок.

![http-header added (95%)](https://img.solarspace.pro/docs/save-key-value-http-headers.jpg "Сохранение HTTP-заголовка")

На этой вкладке вы можете:
- **Добавлять новые HTTP-заголовки**, нажав на кнопку "Добавить"
- **Редактировать существующие HTTP-заголовки**, нажав на иконку карандаша
- **Удалять существующие HTTP-заголовки**, нажав на иконку корзины
- **Выполнять поиск по полям "Key" или "Value"**. Нужное поле выберите в выпадающем списке
![edit http-header (95%)](https://img.solarspace.pro/docs/edit-key-value-http-headers.jpg "Редактирование HTTP-заголовка")

При удалении заголовка нажмите "Сохранить" для подтверждения действия. Вы увидите сообщение "HTTP-заголовок успешно удален".

![delete http-header (95%)](https://img.solarspace.pro/docs/delete-key-value-http-headers.jpg "Удаление HTTP-заголовка")