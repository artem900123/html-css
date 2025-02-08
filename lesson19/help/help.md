# Заняття 19

## Накладання і обтікання блоків


Накладання та обтікання блоків — це важливі концепції в CSS, які дозволяють керувати розташуванням елементів на веб-сторінці. 

## **1. Накладання блоків**

Накладання блоків відбувається, коли елементи розташовуються один поверх одного. Це часто використовується для створення складних макетів, накладання тексту на зображення тощо.

### **Властивість `position`**
Для накладання блоків використовується властивість `position`. Основні значення:
- **`static`** (за замовчуванням): Елемент розташовується в нормальному потоці документа.
- **`relative`**: Елемент розташовується відносно свого звичайного положення.
- **`absolute`**: Елемент розташовується відносно найближчого позиціонованого предка (або відносно вікна браузера, якщо такого предка немає).
- **`fixed`**: Елемент зафіксований на екрані, незалежно від прокрутки сторінки.
- **`sticky`**: Елемент "прилипає" до екрану при прокрутці.

### **Приклад накладання блоків**
```html
<div class="container">
  <div class="box box1">Box 1</div>
  <div class="box box2">Box 2</div>
</div>
```

```css
.container {
  position: relative;
  width: 300px;
  height: 200px;
  border: 2px solid black;
}

.box {
  width: 100px;
  height: 100px;
  color: white;
  text-align: center;
  line-height: 100px;
}

.box1 {
  background-color: red;
  position: absolute;
  top: 20px;
  left: 20px;
}

.box2 {
  background-color: blue;
  position: absolute;
  top: 50px;
  left: 50px;
}
```

**Результат**:
- `Box 1` і `Box 2` накладаються один на одного, оскільки вони мають `position: absolute`.

---

## **2. Обтікання блоків**

Обтікання блоків дозволяє тексту або іншим елементам "обтікати" плаваючий елемент. Для цього використовується властивість `float`.

### **Властивість `float`**
Основні значення:
- **`left`**: Елемент плаває ліворуч, і інші елементи обтікають його справа.
- **`right`**: Елемент плаває праворуч, і інші елементи обтікають його зліва.
- **`none`** (за замовчуванням): Елемент не плаває.

### **Приклад обтікання**
```html
<div class="container">
  <div class="float-box">Float Box</div>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
</div>
```

```css
.container {
  width: 300px;
  border: 2px solid black;
  padding: 10px;
}

.float-box {
  width: 100px;
  height: 100px;
  background-color: yellow;
  float: left;
  margin-right: 10px;
}
```

**Результат**:
- Жовтий блок плаває ліворуч, а текст обтікає його справа.

---

## **3. Очищення обтікання**

Коли елементи плавають, вони можуть порушувати структуру макету. Для вирішення цієї проблеми використовується очищення обтікання.

### **Властивість `clear`**
Основні значення:
- **`left`**: Очищує обтікання ліворуч.
- **`right`**: Очищує обтікання праворуч.
- **`both`**: Очищує обтікання з обох сторін.
- **`none`** (за замовчуванням): Не очищує обтікання.

### **Приклад очищення обтікання**
```html
<div class="container">
  <div class="float-box">Float Box</div>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
  <div class="clearfix"></div>
  <p>Another paragraph after clearing the float.</p>
</div>
```

```css
.container {
  width: 300px;
  border: 2px solid black;
  padding: 10px;
}

.float-box {
  width: 100px;
  height: 100px;
  background-color: yellow;
  float: left;
  margin-right: 10px;
}

.clearfix {
  clear: both;
}
```

**Результат**:
- Після плаваючого блоку текст починається з нового рядка завдяки `clear: both`.

---

## **4. Використання `z-index` для керування порядком накладання**

Коли елементи накладаються, їх порядок можна контролювати за допомогою властивості `z-index`. Елемент з більшим значенням `z-index` розташовується поверх інших.

### **Приклад використання `z-index`**
```html
<div class="container">
  <div class="box box1">Box 1</div>
  <div class="box box2">Box 2</div>
</div>
```

```css
.container {
  position: relative;
  width: 300px;
  height: 200px;
  border: 2px solid black;
}

.box {
  width: 100px;
  height: 100px;
  color: white;
  text-align: center;
  line-height: 100px;
  position: absolute;
}

.box1 {
  background-color: red;
  top: 20px;
  left: 20px;
  z-index: 2;
}

.box2 {
  background-color: blue;
  top: 50px;
  left: 50px;
  z-index: 1;
}
```

**Результат**:
- `Box 1` (червоний) розташовується поверх `Box 2` (синього), оскільки має більший `z-index`.
