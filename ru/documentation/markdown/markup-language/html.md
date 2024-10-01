---
title: HTML
displayName: HTML
order: 140
published: true
historyName: HTML
historyDescription: Использование в Markdown-разметки
---

# HTML
В данном разделе описано использование HTML в markdown разметке.

<br/>


## Описание
В качестве HTML может быть использоваться практически любая разметка, но стоит учитывать, что если возможно
использовать текущий движек для преобразования markdown в HTML, то стоит использовать именно его.
Например, если использовать стандартный HTML-тег изображения, то он не будет оформлен должным образом
и будет нельзя запустить обозреватель изображения.

<br/>


## Пример использования

```md
<h4></h4>
<p></p>
<img src="https://placehold.co/400x600" alt="Заглушка"/>
<table>
  <tr>
    <th>Header 1</th>
    <th>Header 2</th>
  </tr>
  <tr>
    <td>Row 1 - Column 1</td>
    <td>Row 1 - Column 2</td>
  </tr>
  <tr>
    <td>Row 2 - Column 1</td>
    <td>Row 2 - Column 2</td>
  </tr>
</table>
<br>
```

<br/>

## Результат

<h4></h4>
<p></p>
<img src="https://placehold.co/400x600" alt="Заглушка"/>
<table>
  <tr>
    <th>Header 1</th>
    <th>Header 2</th>
  </tr>
  <tr>
    <td>Row 1 - Column 1</td>
    <td>Row 1 - Column 2</td>
  </tr>
  <tr>
    <td>Row 2 - Column 1</td>
    <td>Row 2 - Column 2</td>
  </tr>
</table>
<br>
