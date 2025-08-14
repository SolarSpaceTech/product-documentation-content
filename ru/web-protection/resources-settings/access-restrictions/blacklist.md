---
id: 211
seoTitle: Black list, Черный список — настройка доступа Solar Space
seoDescription: Black list — функция добавления IP-адресов в черный список. Добавьте IP-адреса (IPv4) и подсети (группы IP-адресов), запрос от которых система будет сразу блокировать без дополнительных проверок
displayName: Настройки Black list
order: 10
published: true
historyName: Настройки Black list
historyDescription: Инструкция по формированию черного списка IP-адресов для автоматической блокировки запросов
---



# [Black list](black-list)

Функция **Black list** позволяет добавлять IP-адреса и подсети, запросы от которых будут блокироваться без дополнительных проверок.

Чтобы открыть раздел, перейдите в панель управления и выберите вкладку **«Ограничения доступа»**.

![access-restriction (95%)](https://img.solarspace.pro/docs/on-prem/web-protection/settings/blacklist.png "Раздел видов ограничения доступа")

## [Добавление IP-адресов и подсетей](adding-ip-addresses-&-subnet-to-blacklist)

Вы можете:

* Добавить IP-адрес или подсеть вручную
* Импортировать список из файла `.csv`

Если список пуст, будет доступна кнопка **«Добавить»** для ручного ввода.

![access-restriction (95%)](https://img.solarspace.pro/docs/on-prem/web-protection/settings/add-ip-manual.png "Добавление IP-адреса вручную")

Для импорта списка используйте кнопку **«Импортировать список»**.

![access-restriction (95%)](https://img.solarspace.pro/docs/on-prem/web-protection/settings/import-csv-start.png "Окно импорта CSV")

После выбора файла вы сможете указать способ добавления — замена текущего списка или добавление к нему.

![access-restriction (95%)](https://img.solarspace.pro/docs/on-prem/web-protection/settings/import-csv-mode.png "Выбор режима импорта CSV")

### Формат IP

* Вводите адреса в корректном формате IPv4 или CIDR.
* Для одиночного IP префикс `/32` система подставит автоматически.
* При вводе зарезервированных диапазонов отобразится предупреждение.

![access-restriction (95%)](https://img.solarspace.pro/docs/on-prem/web-protection/settings/ip-format-warning.png "Пример некорректного формата IP")

После добавления IP-адреса или загрузки файла нажмите **«Сохранить»**.

![access-restriction (95%)](https://img.solarspace.pro/docs/on-prem/web-protection/settings/ip-list-saved.png "Список IP после сохранения")

## [Дополнительные действия](Additional-actions)

* **Редактирование** — нажмите иконку карандаша напротив записи.
* **Поиск** — Используйте поле поиска для нахождения нужного IP-адреса — система обнаружит его в списке независимо от заданного уровня.
* **Добавление новых** — используйте кнопку «+».
* **Удаление** — отметьте адреса галочками и нажмите «Удалить». Для удаления всех адресов используйте «Выбрать все» и затем «Удалить».

> **INFO**
> После любых изменений нажимайте **«Сохранить»**, чтобы применить их.
