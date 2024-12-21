# Заняття 13

### Робота з рамками

Рамки (границі) у CSS використовуються для обрамлення елементів, додаючи видимі лінії навколо них. Рамки можуть мати різні кольори, товщини та стилі. Вони допомагають виділити певні частини веб-сторінки та покращити її зовнішній вигляд.

#### Основні властивості для роботи з рамками:

1. `border`
2. `border-width`
3. `border-style`
4. `border-color`

<br>

#### border

Властивість `border` є скороченою для встановлення ширини, стилю та кольору рамки одночасно.

```css
.element {
    border: 2px solid black;
}
```

- 2px: Товщина рамки.
- solid: Стиль рамки.
- black: Колір рамки.

#### border-width

Встановлює ширину рамки. Може приймати значення в пікселях (px), пунктах (pt), ем (em) тощо.

```css
.element {
    border-width: 4px;
}
```

#### border-style

Встановлює стиль рамки. Можливі значення: `none`, `solid`, `dashed`, `dotted`, `double`, `groove`, `ridge`, `inset`, `outset`.

```css
.element {
    border-style: dashed;
}
```

#### border-color

Встановлює колір рамки. Можна використовувати назви кольорів, HEX, RGB, RGBA, HSL, HSLA.

```css
.element {
    border-color: #ff0000;
}
```

### Інші властивості для роботи з рамками:

1. `border-radius`
2. `border-top`, `border-right`, `border-bottom`, `border-left`
3. `border-image`

#### border-radius
Встановлює заокруглення кутів рамки.

```css
.element {
    border: 2px solid black;
    border-radius: 10px;
}
```

#### border-top, border-right, border-bottom, border-left

Встановлює рамку лише з однієї сторони елемента.

```css
.element {
    border-top: 2px solid black;
    border-right: 4px dashed red;
    border-bottom: 2px solid black;
    border-left: 4px dashed red;
}
```

#### border-image

Використовується для встановлення зображення як рамки.

```css
.element {
    border: 10px solid transparent;
    border-image: url(border.png) 30 round;
}
```

### Шрифти

**[CDN Fonts](https://www.cdnfonts.com/)** - це сервіс, який надає зручний доступ до великої бібліотеки шрифтів для використання на ваших веб-сайтах. Замість того, щоб завантажувати шрифти на власний сервер, ви можете підключити їх безпосередньо зі стороннього сервера, що значно спрощує процес і покращує швидкість завантаження сторінок.

https://www.cdnfonts.com/

