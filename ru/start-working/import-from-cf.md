---
id: 265
title: Импорт из CloudFlare
displayName: Импорт из CloudFlare
order: 8
published: false
historyName: Импорт из CloudFlare
historyDescription: Инструкция по импорту ресурсов из CloudFlare
---

# [Импорт из CloudFlare](import-from-cf)

Функция импорта из CloudFlare предназначена для быстрого автоматического переноса ресурсов со всеми доменами в личный кабинет Solar Space.

Это избавит от необходимости переносить ресурсы вручную, а значит, сэкономит время и снизит риск ошибок при миграции.

Для импорта ресурсов из CloudFlare выполните следующие действия:

1. Нажмите на кнопку "Импорт из CloudFlare" в правом верхнем углу экрана: <br>
   - Если вы новый пользователь без ресурсов
![Import on start page(75%)](https://img.solarspace.pro/docs/import-on-start-page.jpg "Импорт на стартовой странице")
   - Если у вас уже есть аккаунт с созданными ресурсами на странице "Мои ресурсы"
![Import on resources page(75%)](https://img.solarspace.pro/docs/import-on-resources-page.jpg "Импорт на странице всех ресурсов")
2. Перейдите в личный кабинет CloudFlare и скопируйте значения из полей:
   - **Email Address** – это поле находится на странице https://dash.cloudflare.com/profile в разделе "Preferences"
![Copy email on Cloudflare(60%)](https://img.solarspace.pro/docs/email-cf.jpg "Поле емайла в Cloudflare")
   - **Global API Key** – это поле находится на странице https://dash.cloudflare.com/profile/api-tokens в разделе "API Keys". Нажмите на кнопку "View" для просмотра поля
![View api-key on Cloudflare(60%)](https://img.solarspace.pro/docs/api-key-cf.jpg "Просмотр api-key в Cloudflare")
   Введите пароль от CloudFlare для подтверждения действия и скопируйте ключ, указанный в поле
![Copy api-key on Cloudlare(50%)](https://img.solarspace.pro/docs/copy-api-key-cf.jpg "Копирование api-key в Cloudflare")
3. Вернитесь на платформу Solar Space и введите эти значения в соответствующие поля: </br>
   - **Email Address** – адрес электронной почты, на который зарегистрирован аккаунт в CloudFlare. Он может отличаться от email, указанного при регистрации в Solar Space </br>
   - **Global API key** – ключ, по которому осуществляется импорт </br>
4. Нажмите на кнопку "Импортировать".
![Import from Cloudflare(60%)](https://img.solarspace.pro/docs/import-from-cf.jpg "Импорт из Cloudflare")
5. Импорт ресурсов займет не более 1 минуты. После этого появится список перенесенных ресурсов со всеми доменами. </br>
Успешно импортированные ресурсы отмечены по умолчанию "галочкой". Вы можете: </br>
   - **Удалять** домены у ресурсов (для импорта ресурс должен содержать хотя бы один домен) </br>
   - **Редактировать** названия ресурсов </br>
   - **Снимать** "галочку" с тех ресурсов, которые вы не хотите добавлять в личный кабинет Solar Space </br>
   - **Сортировать** домены в алфавитном порядке
![Editing functions after import(75%)](https://img.solarspace.pro/docs/editing-functions.jpg "Функции редактирования после импорта")
6. В 2025 году появится возможность поддержки ресурсов с IPv6 и SSL-сертификатами WildCard, которые обеспечивают защиту всех поддоменов. Пока при импорте таких ресурсов появляются предупреждающие сообщения: </br>
   - **Для доменов в формате IPv6**: "Домен содержит DNS-A и DNS-AAAA запись (IPv6), поддержка которой на данный момент недоступна. Этот функционал появится в 1 квартале 2025 года"
![Domain contains 4a(75%)](https://img.solarspace.pro/docs/domain-should-contain-aaaa.jpg "Домен содержит 4а запись")
   - **Для доменов с WildCard-сертификатом**: "Поддержка доменов с опцией Wildcard на данный момент недоступна. Этот функционал появится в 1 квартале 2025 года"
![Domains with Wildcard unavailable(75%)](https://img.solarspace.pro/docs/wildcard-unavailable.jpg "Домены в формате Wildcard недоступны")
   - **Для доменов, у которых отсутствует А запись**: "У домена отсутствует DNS-A запись. Пожалуйста, добавьте ее в настройки своего регистратора/хостинг-провайдера или в настройках ресурса на платформе CloudFlare и повторите импорт ресурсов"
![DNS-A not exist(75%)](https://img.solarspace.pro/docs/dns-a-not-exist.jpg "У домена отсутствует DNS-A запись")
   - Если **домен уже существует на платформе Solar Space**, появится соответствующее предупреждение
![Domain already exist(75%)](https://img.solarspace.pro/docs/domain-exist-in-lk.jpg "Домен уже существует")
7. После выбора всех ресурсов и нажатия на кнопку "Сохранить" появится сообщение об успешном импорте ресурсов. Они будут отображаться на странице ["Мои ресурсы"]([246]). Для перехода на нее нажмите на кнопку "Мои ресурсы" в нижней части страницы.
![Success import page(50%)](https://img.solarspace.pro/docs/success-import.jpg "Страница успешного импорта")