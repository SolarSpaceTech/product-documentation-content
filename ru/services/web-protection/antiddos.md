---
id: 217
seoTitle: AntiDDoS — базовая веб-защита для вашего сайта
seoDescription: Защитите свой сайт от DDoS-атак с помощью AntiDDoS от Solar Space. Сервис обеспечивает базовый уровень веб-защиты. Узнайте больше о преимуществах и активируйте услугу прямо сейчас!
order: 2
published: true
historyName: AntiDDoS
displayName: AntiDDoS
historyDescription: Описание сервиса AntiDDoS, который защищает веб-ресурсы от атак, направленных на замедление работы сайта или его недоступность
category: Сервисы
categoryName: AntiDDoS
categoryDescription: Защита ресурса от DDoS-атак
categoryOrder: 1
categoryIcon: https://img.solarspace.pro/docs/anti-ddos.svg
---

# [AntiDDoS](antiddos)

WEB AntiDDoS обеспечивает базовый уровень [веб-защиты]([240]) в рамках комплексного решения Solar Space.  

Сервис защищает сайты и веб-приложения от DDoS-атак.  

**DDoS-атака** *(от англ. Distributed Denial of Service — распределенный отказ в обслуживании)* состоит в отправке множества запросов к веб-ресурсу. Этот "паразитный" трафик перегружает ресурсы сервера, и сайт начинает работать медленно или совсем перестает загружаться.  

Для подавления DDoS-атак используется комплекс инструментов. Основные — лимиты на количество запросов и JavaScript-челлендж.

1. Лимиты на количество запросов. Сервис анализирует связку "IP-адрес пользователя + путь, к которому он обращается". Если количество запросов в секунду с одного IP-адреса по одному и тому же пути превышает установленный в системе лимит, пользователь увидит ошибку 429 (```Too Many Requests```, слишком много запросов).   
В следующую секунду он сможет дальше делать запросы. Если это легитимный пользователь, и он разово превысил лимит, то дальше он сможет беспрепятственно попасть на веб-ресурс. Если волна из запросов выглядит как цунами, то источнику таких запросов сервер защиты и дальше будет отдавать ошибку 429.  

2.  JavaScript-Challenge (JS Challenge). Прежде чем предоставить пользователю доступ к защищаемому сайту, система отправляет ему HTML-страницу с математической формулой, которую должен выполнить его браузер. Если он этого не сделает, значит, это не браузер, а автоматизированная программа. Такой запрос не получит доступ к сайту.

[//]: # (В основе **WEB AntiDDoS** от Solar Space лежит механизм reverse proxy — обратного прокси-сервера. Это означает, что для защиты веб-ресурса нужно заменить его IP-адрес на IP-адрес нашего сервера. Таким образом весь входящий трафик перенаправится сначала на сервер Solar Space. Там система проводит технический и статистический анализ трафика:)
[//]: # (- Технический анализ предполагает анализ сетевых данных, данных протоколов и SSL-сертификатов 'цифровых сертификатов подлинности сайта')
[//]: # (- Статистический анализ отслеживает всплески трафика или признаки аномального пользовательского поведения)

> **WARNING**
> #### Важно
> WEB AntiDDoS — это обязательный уровень защиты, без которого не могут быть подключены WEB Antibot и WAF Lite

На странице сервиса AntiDDoS доступно его краткое описание и переключатель для активации услуги. AntiDDoS – базовый уровень защиты ресурса, без него невозможна работа [Antibot]([216]) и [WAF Lite]([234]). Поэтому активация других сервисов возможна только при условии активного AntiDDoS.
![AntiDDoS (95%)](https://img.solarspace.pro/docs/antiddos.jpg "antiddos")

Анализ занимает доли секунды, поэтому WEB AntiDDoS не влияет на скорость работы самого сайта

На основе анализа **WEB AntiDDoS** отсеивает часть трафика, которая не соответствует заданным параметрам, а остальную переадресовывает на защищаемый сайт. Именно поэтому настройка перенаправления трафика с помощью смены DNS-А записи – обязательный пункт при подключении защиты в личном кабинете Solar Space. Пока трафик не перенаправлен, защита не работает.  

WEB AntiDDoS обезопасит веб-ресурс от атаки массовыми запросами **на уровне L3-L4 модели OSI**. При этом ботов сервис отсеять не сможет, поскольку настроен на анализ других параметров. Для комплексной защиты ресурса рекомендуем подключать WEB AntiDDoS в комплексе с сервисами:
- [WEB Antibot]([216]) — для фильтрации ботов, которые ищут уязвимости веб-ресурса, замедляют скорость работы сайта, спамят в комментариях и формах обратной связи, негативно влияют на поведенческие факторы, которые оценивают поисковые системы
- [WAF Lite]([234]) — для защиты от вредоносных запросов, которые «маскируются» под обращения реальных пользователей и приводят к взлому пользовательских аккаунтов и утечке данных

