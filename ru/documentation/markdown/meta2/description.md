---
title: Описание мета свойств
displayName: Описание
order: 10
published: true
---

# Описание мета свойств
Мета свойства нужны для описания разделов и страницы. Они позволяют управлять их порядком и отображением на сайте.

<br/>

## [Использование](using)

Возможно использовать только 1 блок с метаданными на страницу. Он должны указываться с первого символа всего файла и содержать конструкцию:
```
---
[мета свойство 1]: [значение мета свойства 1]
[мета свойство 2]: [значение мета свойства 2]
---
```

### [Для создания раздела](section "Раздел")

Раздел в меню выглядит как сворачивающийся список. Он не может быть ссылкой и для его формирования необходимо создать
директорию, содержащую обязательный файл `metadata.md`. Раздел должен сопровождаться следующей метаинформацией:

```md
---
displayName: Название раздела
order: 10
published: true
---
```

### [Для создания статьи](article "Статья")

Статья в меню выглядит как ссылка. Для её формирования в начале файла нужно обязательно указать следующую метаинформацию:
```md
---
title: Название во вкладке браузера
displayName: Название в меню и в хлебных крошках
order: 10
published: true
---
```

## [Свойства](options)

| Мета свойство | Описание                                                                                                                                | Возможные значения и их описания                                                                        | Уже реализовано |  
|:--------------|:----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|:---------------:|
| title         | Название, которое отображаемое в названии браузерной вкладки                                                                            | *Любая строка*                                                                                          |        -        |  
| displayName   | Название документа отображаемое в меню и в хлебных крошках                                                                              | *Любая строка*                                                                                          |        +        |
| order         | Задаёт порядок элементов в меню относительно текущей директории и позволяет вычислить следующую и прошлую страницу в навигационном меню | *Любое число*                                                                                           |        +        |
| published     | Отобразить страницу или раздел в меню                                                                                                   | *true* - опубликовать<br/>*false* - скрыть                                                              |        +        |
| category      | Отобразить элемент на главной странице в соответствующем блоке                                                                          | *start* - "Начало работы"<br/>*services* - "Сервисы"<br/>*useful* - "Полезные статьи"<br/>*faq* - "FAQ" |        -        |
| categoryOrder | Задаёт порядок статей отображаемый в соответствующем разделе на главной странице                                                        | *Любое число*                                                                                           |        -        |
| categoryIcon  | Задаёт svg-иконку для категории                                                                                                         | *Путь до иконки*                                                                                        |        -        |
| headerName    | Отображает ссылку в шапке со соответствующим названием                                                                                  | *Любая строка*                                                                                          |        -        |
| headerOrder   | Определяет порядок статьи в шапке                                                                                                       | *Любое число*                                                                                           |        -        |
| footerName    | Отображает ссылку в подвале со соответствующим названием                                                                                | *Любая строка*                                                                                          |        -        |
| footerOrder   | Определяет порядок статьи в подвале                                                                                                     | *Любое число*                                                                                           |        -        |