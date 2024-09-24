---
title: Ссылки в шапке
displayName: Ссылки в шапке
order: 60
published: true
---

# Ссылки в шапке

Для формирования ссылок в шапке нужно в метаданных статей указывать поля:
- `headerName` - Задаст название статьи
- `headerOrder` - задаст её порядок

```aiignore
--ru
----metadata.md
----documentation
------metadata.md
------start.md (order: 1, displayName: Стартовая страница, headerName: Как начать, headerOrder: 10)
------markdown
--------metadata.md (order: 10, displayName: MD-элементы)
--------examples
----------metadata.md (order: 999, displayName: Примеры)
----------blockquote.md (order: 10, displayName: Информационный блок, headerName: Информационный блок, headerOrder: 30)
----------code.md (order: 60, displayName: Блок кода)
----------heading.md (order: 9, displayName: Заголовки)
--------meta
----------metadata.md (order: 10, displayName: Метаданные)
----------breadcrumbs.md (order: 50, displayName: Хлебные крошки)
----------description.md (order: 10, displayName: Описание)
----------language.md (order: 30, displayName: Добавление языка)
----------menu.md (order: 40, displayName: Навигация по статьям, headerName: Навигация по статьям, headerOrder: 20)
----------url.md (order: 20, displayName: Формирование путей)
```

то в результате в заголовке будет 3 ссылки в соответствующем порядке:
```aiignore
--(Как начать)/ru/documentation/start
--(Навигация по статьям)/ru/documentation/meta/menu
--(Информационный блок)/ru/documentation/examples/blockquote
```
