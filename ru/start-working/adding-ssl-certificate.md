---
id: 271
title: Добавление SSL-сертификата
displayName: Добавление SSL-сертификата
order: 8
published: true
historyName: Добавление SSL-сертификата
historyDescription: Инструкция по добавлению SSL-сертификата для шифрования пользовательких данных
---

# [Добавление SSL-сертификата](adding-ssl-certificate)

Для корректной работы ресурса необходимо добавить SSL-сертификат. Он шифрует всю информацию, которая передается между пользователем и сайтом, чтобы защитить конфиденциальные данные в случае перехвата их злоумышленниками.

SSL-сертификат можно добавить только для домена, который прошел проверку по DNS-A-записи и находится в статусе "Под защитой".

Перейдите в раздел [Веб-защита]([https://my.solarspace.pro/web-protection]) и справа в строке ресурсов нажмите на иконку редактирования.

![edit-ssl-certificate(95%)](https://img.solarspace.pro/docs/edit-ssl-certificate.jpg "Редактирование SSL-сертфиката")

Вы можете загрузить свой сертификат или сгенерировать бесплатный сертификат LE (Let's Encrypt), который будет автоматически продлеваться на платформе Solar Space.

![add-or-change-ssl-certificate(95%)](https://img.solarspace.pro/docs/add-or-change-ssl-certificate.jpg "Добавление или изменение SSL-сертификата")
2. Выберите нужный вариант добавления сертификата и нажмите на кнопку "Сохранить".

![save-added-certificates(95%)](https://img.solarspace.pro/docs/save-added-certificates.jpg "Сохранение добавленного сертификата")

В течении нескольких секунд статус SSL-сертификата изменится.

![success-ssl-certificates(95%)](https://img.solarspace.pro/docs/success-ssl-certificates.jpg "Подтверждение SSL-сертификата")
3. Теперь вы можете переключить галочку в блоке "Редирект на HTTPS", чтобы обеспечить безопасное взаимодействие пользователей с вашим сайтом.

![activate-redirect-on-https-and-save(95%)](https://img.solarspace.pro/docs/activate-redirect-on-https-and-save.jpg "Активация редиректа на HTTPS и сохранение")

Для добавления собственного сертификата на платформу вы можете загрузить файл приватного и публичного ключа, либо вставить его текстом и нажать кнопку "Добавить".

![adding-personal-certificate-with-pupluc-key-and-private-key(55%)](https://img.solarspace.pro/docs/adding-personal-certificate-with-pupluc-key-and-private-key.jpg "Добавление личного сертфиката с публичным и персональным ключами")
