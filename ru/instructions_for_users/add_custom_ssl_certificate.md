### **Добавление своего SSL-сертификата**

Если вы выбрали пункт "Свой сертификат", справа откроется форма добавления. В ней укажите приватный и публичный ключ текстом или загрузите их файлы в соответствующие поля.

![screen]()

> Если вы используете SSL-сертификат Let's Encrypt (LE), вам не нужно его обновлять. Он будет продлеваться автоматически.  
Если вы используете свой сертификат, не забывайте загрузить в личный кабинет актуальную версию после его обновления.

На вкладке "Домен и SSL" можно включить расширенный функционал: "Редирект с www" и "Редирект на HTTPS". Это не требует дополнительной оплаты.

![screen]()

- Редирект с WWW – перенаправление трафика на домен без www.
Поисковые системы рассматривают URL-адреса с "www" и без "www" как разные страницы, а для пользователей эта разница неочевидна. Если в адресе вашего сайта используется" www", а пользователи для экономии времени вводят адрес без "www", то включенный редирект перенаправит их на ваш сайт. При отключенном редиректе сервер не найдет нужную страницу.
- Редирект на HTTPS – если подключить эту функцию, все запросы к серверу, отправленные по небезопасному протоколу HTTP, будут автоматически переходить на безопасный протокол HTTPS, что сделает взаимодействие пользователя с сайтом защищенным.
- Перенаправление трафика через сервера защиты - перенаправляет трафик ресурса на сервера защиты. Если пути трафика не настроены или вам нужно их переустановить, нажмите иконку круглой стрелки.  

Откроется меню "Перенаправление трафика через сервера защиты". Нажмите иконку ![screen]() чтобы скопировать значение из поля "DNS-A". Это IP-адрес сервера защиты Solar Space. На сайте своего хостинг-провайдера откройте настройки домена, который нужно поставить под защиту.  

Создайте новую DNS-A запись и введите туда данные, скопированные из поля "DNS-A". Все остальные DNS-A записи и AAAA записи на сайте своего хостинг-провайдера нужно удалить.. Выберите верифицируемый ресурс на вкладке "Неверифицируемые" или "Все". Поставьте галочку слева от имени домена и нажмите кнопку "Верифицировать".  

После этого нажмите кнопку "Верифицировать" в нижней части экрана. Запрос на верификацию уйдет вашему хостинг-провайдеру.  

Нажмите кнопку “Отменить” чтобы окно верификации.

![screen]()
