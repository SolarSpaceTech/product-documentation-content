---
title: Ссылки в подвале
displayName: Ссылки в подвале
order: 40
published: true
---

# Ссылки в подвале

Для формирования ссылок в подвале нужно в метаданных статей указывать поля:
- `footerName` - Задаст название статьи
- `footerOrder` - задаст её порядок

```aiignore
--ru
----metadata.md
----documentation
------metadata.md
------start.md (order: 1, displayName: Стартовая страница, footerName: Как начать, footerOrder: 10)
------markdown
--------metadata.md (order: 10, displayName: MD-элементы)
--------examples
----------metadata.md (order: 999, displayName: Примеры)
----------blockquote.md (order: 10, displayName: Информационный блок, footerName: Информационный блок, footerOrder: 30)
----------code.md (order: 60, displayName: Блок кода)
----------heading.md (order: 9, displayName: Заголовки)
--------meta
----------metadata.md (order: 10, displayName: Метаданные)
----------breadcrumbs.md (order: 50, displayName: Хлебные крошки)
----------description.md (order: 10, displayName: Описание)
----------language.md (order: 30, displayName: Добавление языка)
----------menu.md (order: 40, displayName: Навигация по статьям, footerName: Навигация по статьям, footerOrder: 20)
----------url.md (order: 20, displayName: Формирование путей)
```

то в результате в подвале будет 3 ссылки в соответствующем порядке:
```aiignore
--(Как начать)/ru/documentation/start
--(Навигация по статьям)/ru/documentation/meta/menu
--(Информационный блок)/ru/documentation/examples/blockquote
```
