---
id: 204
title: Авторизация
displayName: Авторизация
order: 2
published: true
historyName: Авторизация
historyDescription: Авторизуйтесь для доступа к своему аккаунту и управления подключенными сервисами
---

# [Авторизация](authorization)

Если у вас еще нет аккаунта, вы можете [зарегистрироваться]([242]).

Если вы забыли пароль, у вас есть возможность его [восстановить]([208]).

Для авторизации в личном кабинете выполните следующие действия:

1.  Введите в адресной строке браузера адрес – https://my.solarspace.pro. Откроется страница авторизации.
![Start authorization page(95%)](https://img.solarspace.pro/docs/start-authorization-page.jpg "Стартовая форма авторизации")
2. Введите email и пароль, которые вы указывали при регистрации и нажмите на кнопку "Войти" для входа в личный кабинет.
![Active authorization form(50%)](https://img.solarspace.pro/docs/auth-active-form.jpg "Активная форма авторизации")
При вводе некорректных данных вы увидите сообщение "Логин или пароль неверен".
![Authorization form with incorrect email or password(50%)](https://img.solarspace.pro/docs/auth-incorrect-email-or-password.jpg "Авторизация с некорректным емайлом или паролем")
После 5 неудачных попыток авторизации с неверным паролем вам потребуется ввести капчу. Так система убедится, что форму заполняет реальный пользователь.
![Captcha on the authorization form(50%)](https://img.solarspace.pro/docs/auth-captcha.jpg "Капча на форме авторизации")
При отправке формы с некорректным кодом вы увидите сообщение "Неверный текст", и капча обновится. Количество попыток прохождения капчи неограничено.
![Captcha with wrong code on the authorization form(50%)](https://img.solarspace.pro/docs/auth-wrong-captcha.jpg "Неверный код для капчи на форме авторизации")
Когда капча пройдена, и поля "Логин" и "Пароль" заполнены корректно, кнопка "Войти" станет активной. Нажмите на нее для входа в личный кабинет.
![Success captcha on the authorization form(50%)](https://img.solarspace.pro/docs/success-auth-captcha.jpg "Успешная капча на форме авторизации")