---
id: 265
title: Постановка домена под защиту
displayName: Постановка домена под защиту
order: 7
published: false
historyName: Постановка домена под защиту
historyDescription: Настройте и оплатите тариф, чтобы активировать выбранные сервисы
---

# [Постановка домена под защиту](domain-name-protection)

Чтобы подключить домен под защиту, нужно настроить перенаправление трафика на защищенный IP-адрес Solar Space, изменив IP-адрес в А-записи вашего домена. Для этого выполните следующие действия:

1. Перейдите в раздел Веб-защита, кликнув на соответствующую иконку в боковом меню.
![web protection start page(75%)](https://img.solarspace.pro/docs/web-protection-start-page.jpg "Старовая страница ВЕБ-защиты")

2. Найдите в списке нужный ресурс и перейдите в раздел Настройки, нажав на название ресурса, либо на иконку с тремя точками справа в строке ресурса.
![web protection choose domain protection settings(75%)](https://img.solarspace.pro/docs/web-protection-choose-domain-protection-settings.jpg "Настройки веб-защиты домена")

На странице ресурса будет отображаться список его доменов и их статусы.

3. В блоке справа нажмите кнопку "Настроить трафик".
![web protection traffic settings(75%)](https://img.solarspace.pro/docs/web-protection-traffic-settings.jpg)

В открывшемся окне скопируйте IP-адрес из поля DNS-А, нажав на иконку копирования.
![web protection traffic redirect(75%)](https://img.solarspace.pro/docs/web-protection-traffic-redirect.jpg)

4. Перейдите на сайт своего DNS-регистратора или хостинг-провайдера и откройте интерфейс редактирования DNS-записей. Измените значение А-записей всех защищаемых доменов и поддоменов на защищенный IP-адрес Solar Space. Остальные A-записи и AAAA-записи на сайте своего DNS-регистратора или хостинг-провайдера нужно удалить.
![web protection a record in host provider(75%)](https://img.solarspace.pro/docs/web-protection-a-record-in-host-provider.jpg)

5. Вернитесь в личный кабинет Solar Space и нажмите кнопку "Подтвердить" в окне перенаправления трафика.

Процесс обновления A-записи обычно занимает не более 1-2 часа, но некоторые DNS-серверы могут обновляться до суток. После их обновления статус домена изменится на "Настроен", и в блоке "Настройка" появится сообщение, что трафик успешно перенаправлен.
![traffic has been successfully redirected(75%)](https://img.solarspace.pro/docs/traffic-has-been-successfully-redirected.jpg)