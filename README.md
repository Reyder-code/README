# GRID
## Grid - макет, разделяющий веб-страницу на столбцы и строки

## **Как использовать:**

## HTML задаем класс для нужного блока:
```html
<body>
	<div class=”container”></div>
</body>
```
## Задаем свойства в CSS:
### Контейнер создается с помощью свойства display: grid; а затем задаются свойства для размещения элементов внутри контейнера
```css
.container{
     display: grid;
}
```
### Колонки и строки задаются с помощью: 
- grid-template-columns 
- grid-template-rows

Например, 
```css
.container{
     display: grid;
     grid-template-columns: 1fr 2fr 1fr; 
}
```
- fr - это единица измерения, которая говорит браузеру какую часть экрана использовать для создания grid клетки.
Например, есть две клетки. 1fr и 2fr. Это значит, что вторая клетка будет в два раза больше, чем первая. То есть, занимать 2/3 свободного пространства. 

Чтобы объеденить клетки и дать им название, используем:
- grid-template-areas
```css
.container{
     display: grid;
     grid-template-columns: 1fr 2fr 1fr; 
     grid-template-areas: 
     ". . ."
     ". . ."
     ". . ."; 
}
```

Чтобы задать расстояние между ячейками внутри сетки используем:
- gap
```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  gap: 20px;
}
```
Также можно использовать два значения для gap. Первое значение задает расстояние между строками, а второе - между колонками. Например:
```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  gap: 20px 10px;
}
```

## Grid Placement
Чтобы горизонтально выравнить элементы внутри ячеек грида используем:
- justify-items:
     - center (Выравнивает по центру)
     - start (Выравнивает по правому краю)
     - end (Выравнивает по левому краю)
```css
.container {
     display: grid;
     grid-template-columns: 1fr 1fr;
     justify-items: center;
}
```
Чтобы вертикально выравнить элементы внутри ячеек грида используем:
- align-items
     - center (Выравнивает по центру)
     - start (Выравнивает по правому краю)
     - end (Выравнивает по левому краю)
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
}

```

Чтобы горизонтально выравнять грид на основе свободного пространтсва внутри контейнера используем:
- justify-content
     - center (Выравнивает по центру)
     - start (Выравнивает по правому краю)
     - end (Выравнивает по левому краю)
     - space-between (столбцы грида будут равномерно распределены по ширине контейнера, начиная с левой границы и заканчивая правой границей, с равным расстоянием между ними)
     - space-around (столбцы грида будут равномерно распределены по ширине контейнера, с равным расстоянием как слева, так и справа)
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  justify-content: center;
}
```

Чтобы вертикально выравнять грид на основе свободного пространтсва внутри контейнера используем:
- align-content
     - center (Выравнивает по центру)
     - start (Выравнивает по правому краю)
     - end (Выравнивает по левому краю)
     - space-between (строки грида будут равномерно распределены по высоте контейнера, начиная с верхней границы и заканчивая нижней границей, с равным расстоянием между ними)
     - space-around (строки грида будут равномерно распределены по высоте контейнера, с равным расстоянием как сверху, так и снизу)
```css
.container {
  display: grid;
  grid-template-rows: 1fr 1fr;
  align-content: center;
}
```

## **Для упрощения задачи используйте сайт** https://grid.layoutit.com/

