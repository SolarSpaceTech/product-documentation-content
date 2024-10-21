---
id: 203
title: Вкладка - Настройки Black List
displayName: Настройки Black List
order: 1
published: true
historyName: Настройки Black List
historyDescription: Обучение персонала
category: Настройка ресурсов
categoryName: Настройки Black List
categoryDescription: Обучение персонала
categoryOrder: 6
categoryIcon: https://img.solarspace.pro/docs/users.svg
footerName: Настройки Black List
footerOrder: 10
---

### **Black list**
Добавьте IP-адреса (IPv4) и подсети (группы IP-адресов), запрос от которых система будет сразу блокировать без дополнительных проверок. Их можно прописать вручную или загрузить списком в формате .csv.

Если вы еще не добавили ни одного IP-адреса в Black list, то увидите кнопки "Добавить" (для добавления IP-адресов вручную) и "Импортировать список" (для загрузки файла со списком). 

![screen]()

При нажатии на кнопку "Импортировать список" справа откроется окно для загрузки файла в формате .csv. Когда вы добавите файл, кнопка "Импортировать" в нижней части экрана станет активной.

![screen]()

Если вы будете добавлять IP-адреса в Black list вручную, обратите внимание: IP-адрес должен состоять из уровней, разделенных точкой. Если ввести его в некорректном формате, система покажет сообщение "Введите IP или подсеть в CIDR-нотации".
Если ввести IP-адрес сети которая не используется в сети Интернет и предназначена только для частного пользования, под этим полем появится текст "Это зарезервированная подсеть".

![screen]()

> Слеш "/" и число "32" вводить не нужно. Система проставит их сама исходя из введенного вами IP-адреса.

После введения IP-адреса/подсети или загрузки файла со списком нажмите кнопку "Сохранить" в нижней части экрана.

![screen]()

В нижней части экрана вы увидите сообщение "Настройки ресурса успешно сохранены". Добавленный IP-адрес отражается в списке подлежащих блокировке.

![screen]()

Если хотите отредактировать введенные данные, нажмите на иконку карандаша рядом с полем поиска.
Если хотите добавить новые IP-адреса/подсети, нажмите на кнопку "+" рядом с полем поиска.
Для загрузки списка нажмите иконку загрузки файла в верхнем правом углу формы. 

![screen]()

Нужный IP-адрес можно найти через поле поиска. Вы можете задать в нем любой уровень. Если IP-адрес есть в списке, система его найдет.

![screen]()

Если IP-адреса нет в списке, вы увидите сообщение “ничего не найдено”.

![screen]()

Для удаления IP-адреса из Black list нажмите на иконку редактирования в виде карандаша рядом с полем поиска. После этого найдите нужный IP-адрес в списке и нажмите на крестик справа от него.

![screen]()
![screen]()                   

Если нужно удалить несколько IP-адресов, отметьте их галочками слева от поля и нажмите на кнопку "Удалить" в нижней части формы. Также вы можете удалить все адреса из списка: нажмите на кнопку "Выбрать все" в нижней части формы и затем на кнопку "Удалить".

![screen]()

После внесения любых изменений в Black list нажимайте кнопку "Сохранить" в нижней части экрана. После этого ваши корректировки отразятся в интерфейсе.

![screen]()
