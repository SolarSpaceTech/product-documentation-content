---
id: 21
title: Изображения - Markdown-разметка
displayName: Изображения
order: 110
published: true
historyName: Изображения
historyDescription: Использование в Markdown-разметки
---

# Изображения
В этом разделе рассмотрены изображения и как их использовать.

<br/>

## Описание
Для создания изображения используют синтаксис:
```md
![Название изображения (ширина:высота|позиционирование)](путь/до/превью|путь/до/изображения "Скрытый текст изображения")
```
- `Название изображения` это отображаемый текст, который увидит пользователь в случае, если произойдёт ошибка загрузки изображения;
- `ширина` - ширина изображения, можно задавать любую css единицу измерения (по умолчанию изображение растягивается на всю ширину);
- `высота` - высота изображения, можно задавать любую css единицу измерения (по умолчанию изображение учитывает пропорции
в соответствии с высотой и исходным изображением)
- `позиционирование` - может принимать значения `left`, `right` и `center`. `left` - прижимает изображение слева и заставляет текст
обтекать справа. `right` - прижимает изображение справа и заставляет тест обтекать слева. `center` - помещает изображение по центру
без возможности обтекания текста слева и справа.
- `путь/до/превью` это url до уменьшенной версии изображения;
- `путь/до/изображение` это url до полной версии изображения;
- `Скрытый текст изображения` это текст который будет показываться при наведении на изображение.

<br/>

## Пример использования
```md
![image (25%)](https://placehold.co/400x625|https://placehold.co/800x1250 "Some text")

![image (25%|right)](https://placehold.co/1600x2500 "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.

<br/>

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image (25%|left)](https://placehold.co/1600x2500 "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.

<br/>

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image (50%|center)](https://placehold.co/1600x2500 "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.

<br/>

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image](https://placehold.co/1600x2500 "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
```

<br/>

## Результат

![image (25%)](https://placehold.co/400x625|https://placehold.co/800x1250 "Some text")

![image (80px:125px|right)](https://placehold.co/1600x2500 "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.

<br/>

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image (25%|left)](https://placehold.co/1600x2500 "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.

<br/>

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image (50%|center)](https://placehold.co/1600x2500 "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.

<br/>

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image](https://placehold.co/1600x2500 "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
