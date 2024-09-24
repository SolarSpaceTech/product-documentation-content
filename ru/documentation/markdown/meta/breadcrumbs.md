---
title: Хлебные крошки
displayName: Хлебные крошки
order: 50
published: true
---

# Хлебные крошки

Свойство задаёт название документа отображаемое в меню и в хлебных крошках. Например, есть следующая файловая структура:

```
--ru
----metadata.md (displayName: Русский)
----documentation
------metadata.md (displayName: Документация)
------markdown
--------metadata.md (displayName: MD-элементы)
--------description.md (displayName: Описание)
------examples
--------metadata.md (displayName: Примеры)
--------description.md (displayName: Описание)
```

Языковой раздел при формировании хлебных крошек пропускается. Для вложенной структуры формирование происходит следующим образом.
Например, пользователь находится на странице `/ru/documentation/markdown/description`. В результате хлебные крошки будут формироваться так:
1. берется значение свойства `displayName` из `metadata.md` раздела `documentation` (Документация)
2. берется значение свойства `displayName` из `metadata.md` раздела `markdown` (MD-элементы)
3. берется значение свойства `displayName` из `description.md` (Описание)

В результате хлебные крошки сформируются в `Документация -- MD-элементы -- Описание`


