---
id: 208
seoTitle: Подключение сервисов — Solar Space
seoDescription: Подключение сервисов Веб-защиты на платформе Solar Space. Выберите желаемый уровень защиты и настройте параметры тарифа
displayName: Подключение сервисов
order: 3
published: true
historyName: Подключение сервисов
historyDescription: Настройте и оплатите тариф, чтобы активировать выбранные сервисы
category: Аккаунт и профиль
categoryName: Подключение сервисов
categoryDescription: Выбор и активация пакета услуг
categoryOrder: 20
categoryIcon: https://img.solarspace.pro/docs/payment.svg
audienceScope: internal
tags: 
  - accent
  - quick start
---

# [Подключение сервисов](choosing-services)

На этой странице вы можете выбрать один из доступных тарифов веб-защиты:

- **Бесплатный тариф** — сервис [AntiDDoS]([217]) (ограничение: до 1 Мбит/с, один ресурс)
- **Базовый тариф** — сервис [AntiDDoS]([217])
- **Оптимальный тариф** — сервисы [AntiDDoS]([217]) + [Antibot]([216])
- **Продвинутый тариф** — сервисы [AntiDDoS]([217]) + [Antibot]([216]) + [WAF Lite]([234])
- **Демо-тариф на 14 дней** — сервисы [AntiDDoS]([217]) + [Antibot]([216]) + [WAF Lite]([234]), полный функционал без ограничений


---

## [Подключение сервиса](service-connection)

1. Нажмите на кнопку «Подключить» в тарифе «Веб-защита» после [подтверждения аккаунта]([243]).  
   Откроется форма выбора уровня защиты.  
   ![Enable web protection (95%)](https://img.solarspace.pro/docs/saas/choosing-services/enable-web-protection.png "Подключение Веб-защиты")  

2. Укажите желаемый тариф:
   - **Бесплатный тариф** — только [AntiDDoS]([217]), ограничение по каналу 1 Мбит/с и один ресурс.  
     ![Free level of Web-protection (95%)](https://img.solarspace.pro/docs/saas/choosing-services/free-level-of-protection.png "Бесплатный уровень защиты")
   - **Базовый тариф** — только [AntiDDoS]([217]).  
     ![Basic level of Web-protection (95%)](https://img.solarspace.pro/docs/saas/choosing-services/basic-level-of-protection.png "Базовый уровень защиты")
   - **Оптимальный тариф** — [AntiDDoS]([217]) + [Antibot]([216]).  
     ![Optimal level of Web-protection (95%)](https://img.solarspace.pro/docs/saas/choosing-services/optimal-level-of-protection.png "Оптимальный уровень защиты")
   - **Продвинутый тариф** — [AntiDDoS]([217]) + [Antibot]([216]) + [WAF Lite]([234]).  
     ![Advanced level of Web-protection (95%)](https://img.solarspace.pro/docs/saas/choosing-services/advanced-level-of-protection.png "Продвинутый уровень защиты")

3. После выбора тарифа появятся поля для настройки параметров:  
   - **Ширина канала** — определяет объём трафика, проходящий через защиту.  
     Для простого сайта-визитки обычно достаточно 10–30 Мбит/с.  
     В бесплатном тарифе значение фиксировано (1 Мбит/с).  
   - **Количество запросов в секунду (RPS)** — отражает нагрузку на сайт.  
     Этот параметр нужен только в продвинутом тарифе (с WAF Lite).  
     Например, визитке хватает 5–10 RPS, интернет-магазину — от 50 RPS и выше.  

4. Проверьте параметры тарифа и нажмите кнопку «Применить».  
   ![Submit Web-protection (95%)](https://img.solarspace.pro/docs/saas/choosing-services/submit-web-protection.png "Сохранить параметры Веб-защиты")

5. В форме «Настройки тарифа» укажите оплачиваемый период (от 1 до 12 месяцев) и нажмите кнопку «Оформить».  
   ![Confirmation Web-protection (95%)](https://img.solarspace.pro/docs/saas/choosing-services/confirmation-web-protection.png "Оформить Веб-защиту")

6. После выбора сервисов перейдите к шагу [оплаты]([276]).

---

## [Демо-тариф](demo-plan)

Демо-тариф даёт возможность протестировать весь функционал веб-защиты бесплатно в течение 14 дней.  
В этот период доступны [AntiDDoS]([217]), [Antibot]([216]) и [WAF Lite]([234]) без ограничений по каналу и количеству запросов. Можно подключать любое количество ресурсов — так, как если бы у вас был полноценный платный тариф.  

![Demo level of Web-protection (95%)](https://img.solarspace.pro/docs/saas/choosing-services/demo-level-of-protection.png "Демо-тариф")

### Особенности подключения
- Демо можно активировать только один раз для аккаунта.  
- Доступен пользователям, у которых ранее не было активных тарифов с сервисами, входящими в демо.  
- После активации весь функционал работает в полном объёме.  

![Demo of Web-protection (95%)](https://img.solarspace.pro/docs/saas/choosing-services/demo-of-protection.png "Демо-тариф")

### Рекомендации тарифа
По окончании демо система автоматически формирует **персональные предложения платных тарифов** на основе статистики использования.  

![Demo recommendations of Web-protection (95%)](https://img.solarspace.pro/docs/saas/choosing-services/demo-recommendations.png "Рекомендации по итогам демо")

- Если нагрузка не превышала 1 Мбит/с и RPS оставался низким — система предложит базовые варианты (например, 2 Мбит/с и 5 RPS).  
- Если нагрузка была выше — будут предложены более мощные тарифы (например, 30 Мбит/с и 20 RPS).  
- Варианты подбираются из трёх уровней: **Базовый**, **Оптимальный**, **Продвинутый**, с указанием рекомендуемой ширины канала и количества запросов.  