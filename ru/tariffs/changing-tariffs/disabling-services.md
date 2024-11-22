---
id: 260
title: Отключение сервисов
displayName: Отключение сервисов
order: 3
published: true
historyName: Отключение сервисов
historyDescription: Инструкция по отключению сервисов
---

# [Отключение сервисов](disabling-services)

**При отключении активного сервиса изменения вступят в силу со следующего расчетного периода.**

Отключение сервисов означает понижение уровня защиты: с продвинутого на базовый или оптимальный, либо с оптимального на базовый.

> **WARNING**
> **Важно**  
> При удалении сервиса AntiDDoS защита веб-ресурса полностью отключается

Для отключения сервисов выполните следующие действия:
1. Измените уровень защиты:
   - С **продвинутого** на **оптимальный** – для отключения сервиса WAF Lite. Активными останутся сервисы **AntiBot** и **AntiDDoS**
![Change to optimal level(75%)](https://img.solarspace.pro/docs/change-to-optimal-level.jpg "Изменение на оптимальный уровень")
   - С **продвинутого** на **базовый** – для отключения сервисов WAF Lite и Antibot. Активным останется сервис **AntiDDoS**
![Change to basic level(75%)](https://img.solarspace.pro/docs/change-to-basic-level.jpg "Изменение на базовый уровень")
   - С **оптимального** на **базовый** – для отключения сервиса Antibot. Активным останется сервис AntiDDoS
![Change to basic level(75%)](https://img.solarspace.pro/docs/change-to-basic-level.jpg "Изменение на базовый уровень")
2. Укажите значение для поля "Ширина канала" и нажмите на кнопку "Применить".
3. Проверьте информацию в блоке "Изменения тарифа" и нажмите на кнопку "Сохранить".
![Disabling services for billing(75%)](https://img.solarspace.pro/docs/disabling-services-for-billing.jpg "Сохранение отключения сервисов")
4. Если на балансе недостаточно средств, нажмите кнопку "Пополнить баланс".
![Recharge for disabling services(35%)](https://img.solarspace.pro/docs/recharge-for-disabling-services.jpg "Пополнение баланса при отключении сервисов")
5. Если на вашем счете достаточно средств, появится сообщение об успешном изменении тарифа. Изменения вступят в силу со следующего расчетного периода.
![Successful tariff change(35%)](https://img.solarspace.pro/docs/successful-tariff-change.jpg "Успешное изменение тарифа")
