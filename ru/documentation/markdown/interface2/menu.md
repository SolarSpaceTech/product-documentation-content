---
title: Навигация по статьям
displayName: Навигация по статьям
order: 10
published: true
---

# Навигация по статьям

- для отображения меню должна быть соответствующая файловая структура;
- чтобы создать раздел меню нужно создать директорию в `documentation` того или иного языка внутри созданной директории
создать файл `metadata.md`;
- для создания статьи создайте файл в необходимом разделе;
- для управления порядком элементов используйте `order`. Чем меньше его значение, тем выше в списке меню
оно будет. Для удобства при первоначальном формировании структуры файлов в качестве `order` можно указывать значения
кратные 10, чтобы упростить дальнейшее перемещение разделов и статей.;
- для сокрытия статьи или раздела используйте поле `published`;
- имя отображаемое для статьи в меню берется из `displayName`.

## Пример

Для файловой структуры:
```aiignore
--ru
----metadata.md
----documentation
------metadata.md
------start.md (order: 1, displayName: Стартовая страница)
------markdown
--------metadata.md (order: 10, displayName: MD-элементы)
--------examples
----------metadata.md (order: 999, displayName: Примеры)
----------blockquote.md (order: 10, displayName: Информационный блок)
----------code.md (order: 60, displayName: Блок кода)
----------heading.md (order: 9, displayName: Заголовки)
--------meta
----------metadata.md (order: 10, displayName: Метаданные)
----------breadcrumbs.md (order: 50, displayName: Хлебные крошки)
----------description.md (order: 10, displayName: Описание)
----------language.md (order: 30, displayName: Добавление языка)
----------menu.md (order: 40, displayName: Навигация по статьям)
----------url.md (order: 20, displayName: Формирование путей)
```

В результате чего будет сформировано меню:

```aiignore
Докуметация
--(Стартовая страница) /ru/documentation/start

--(Метаданные)
----(Описание) /ru/documentation/meta/description
----(Формирование путей) /ru/documentation/meta/url
----(Добавление языка) /ru/documentation/meta/language
----(Навигация по статьям) /ru/documentation/meta/menu
----(Хлебные крошки) /ru/documentation/meta/breadcrumbs

--(Примеры)
----(Заголовки) /ru/documentation/examples/heading
----(Информационный блок) /ru/documentation/examples/blockquote
----(Блок кода) /ru/documentation/examples/code
```
