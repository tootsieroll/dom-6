# урок 6

### Что за единица измерения - `fr`?

**Единица измерения fr**
 представляет собой долю оставшегося в сетке пространства. Как и все CSS размеры, между числом и **единицей измерения**
 нет пробела

### Как можно задать грид с 5 колонками шириной по 20%? Минимум 2 способа

grid-template-columns: 20%,20%,20%,20%.20%

grid-template-columns: repeat(5,20%)

### Самостоятельно разберитесь, что такое `auto-fill` и `auto-fit` ?

`auto-fill` и `auto-fit` помогут в создании динамичных шаблонов:

**auto-fill**

Вместо того, чтобы указывать количество колонок и сколько раз им повторяться, мы просто можем сказать браузеру, чтобы он уместил как можно больше колонок с учетом указанной длины.

`auto-fill` как бы говорит “_я автоматически заполню строку таким количеством колонок, как это возможно с учетом заданной ширины_”. `auto-fill` используется в связке с `repeat()` таким образом:

```
grid-template-columns: repeat(auto-fill, 100px);
```

### Как сделать такую табличку? Параметры: первая колонка шириной 100 пикселей, вторая 30%. Первая строчка высотой 200 пикселей, вторая строчка 100 пикселе

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1f4613fc-2f5b-4be8-bc74-1affecbf8272/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1f4613fc-2f5b-4be8-bc74-1affecbf8272/Untitled.png)

```markup

```

grid-template-columns: 100px 30% 1fr

grid-template- rows: 200 px 100px

или grid-template:100px 30% 1fr/200px 100px

### Как сделать такое выравнивание в грид-контейнере?

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9530286c-633a-44dd-a8e0-543d51d669d6/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9530286c-633a-44dd-a8e0-543d51d669d6/Untitled.png)

space-between

### Что такое и как задается _grid area_?

CSS-свойство **grid** -**area**
 - это сокращённая форма записи для свойств **grid**
-row-start , **grid**
-column-start (en-US), **grid**
-row-end (en-US) и **grid**
-column-end (en-US). Определяет размер и местоположение грид-элемента в пределах **grid**
 row (en-US). **Задаёт**
 края грид-области (en-US) грид-элемента.

### Приведите пример использования `grid-template-areas` (не копированием из этого урока 😉)

```css
main {
  grid-area: main;
  display: grid;
  grid-template-columns: 20px 30% 30% 1fr 20px;
  grid-template-rows: 1fr 100px 100px 50px;
  grid-gap: 20px;
}
```

### Каким свойством можно задать такое поведение элементов?

auto-fill или minimax(50 px,200px)
