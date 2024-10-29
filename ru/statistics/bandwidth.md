---
id: 236
title: Вкладка - Ширина канала
displayName: Ширина канала
order: 2
published: true
historyName: Ширина канала
historyDescription: Просмотр графика пропускной способности
category: Статистика
categoryName: Ширина канала
categoryDescription: Просмотр графика пропускной способности
categoryOrder: 2
categoryIcon: https://img.solarspace.pro/docs/icon_12.svg
---

### Ширина канала

Здесь вы можете посмотреть подробную информацию о трафике. В верхней части над графиком можно выбрать домены, установить период отображения отчета, часовой пояс и частоту обновления

![Filters for "Bandwidth" tab(70%)](https://img.solarspace.pro/docs/statistic-bandwidth-filters.jpg "Фильтры ширины канала")

Под графиком обозначены 4 типа трафика:

1. Тарифицируемый – определяется объемом полосы трафика, зафиксированной в вашем тарифе. Для расчета используется алгоритм 95-го перцентиля по исходящему и входящему легитимному (очищенному) трафику. Это означает, что в течение месяца исходящий и входящий легитимный (очищенный) трафик измеряются и фиксируются каждые 5 минут. Для каждого из видов трафика в конце месяца исключаются 5% пиковых значений, и из оставшихся 95% выбирается максимальный показатель. Это и есть 95-й перцентиль. Система сравнивает 95-й перцентиль исходящего трафика и 95-й перцентиль входящего легитимного трафика. Из этих двух значений выбирается наибольшее, которое используется для расчета оплаты


2. Исходящий – трафик, который ваш сервер отправил посетителям вашего сайта


3. Входящий – общий трафик, который платформа фильтрации принимает и проверяет на предмет подозрительной активности. Включает в себя и реальных пользователей и паразитный трафик: DDoS-атаки, фишинг и спам, вредоносные файлы и коды, автоматические программы для сканирования на уязвимости


4. Входящий легитимный – трафик после очистки системой защиты и фильтрации вредоносных запросов, то есть только реальные пользователи и полезные роботы поисковых систем

![Traffics for "Bandwidth" tab(70%)](https://img.solarspace.pro/docs/statistic-bandwidth-traffics.jpg "Трафики ширины канала")

Нажимая на название типа трафика, вы можете исключить его из графика. В этом случае его название станет серым. Чтобы этот тип трафика снова отображался в отчете, повторно нажмите на его название