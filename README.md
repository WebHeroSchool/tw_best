# Лучшие практики в JavaScript
1. Объявляйте переменные вверху

```js
// Вначале объявляем
var firstName, lastName, price, discount, fullPrice;

// Потом используем
firstName = "John";
lastName = "Doe";

price = 19.90;
discount = 0.10;

fullPrice = price * 100 / discount;
```


2. Инициализируйте переменные при их объявлении

```js
// Объявление и инициализация вначале
var firstName = "",
    lastName = "",
    price = 0,
    discount = 0,
    fullPrice = 0,
    myArray = [],
    myObject = {};
```

3. Не используйте ` new Object() `

```js
var x1 = {};           // новый объяет
var x2 = "";           // новый примитив строки
var x3 = 0;            // новый примитив  числа
var x4 = false;        // новый примитив  boolean
var x5 = [];           // новый масстив 
var x6 = /()/;         // новый regexp object
var x7 = function(){}; // новый function object
```

4. Остерегайтесь автоматических переобразований типов

```js
var x = "Hello";     // typeof x это строка
x = 5;               // измененный typeof x на чисор
```

5. Используйте === сравнение

```js
0 == "";        // true
1 == "1";       // true
1 == true;      // true

0 === "";       // false
1 === "1";      // false
1 === true;     // false
```

6. Используйте параметры по умолчанию

```js
function myFunction(x, y) {
    if (y === undefined) {
        y = 0;
    }
}

// Или в ES2015:
function (a=1, b=1) { // function code }
```

7. Заканчивайте свой Wwitch с Default

```js
switch (new Date().getDay()) {
    case 0:
        day = "Sunday";
        break;
    case 1:
        day = "Monday";
        break;
    case 2:
        day = "Tuesday";
        break;
    case 3:
        day = "Wednesday";
        break;
    case 4:
        day = "Thursday";
        break;
    case 5:
        day = "Friday";
        break;
    case 6:
        day = "Saturday";
        break;
    default:
        day = "Unknown";
}
```

8. Минимизируйте использование глобальных переменных

9. Используйте длинные, описательные имена

```js
// Плохо
function inv (user) { /* implementation */ }

// Хорошо
function inviteUser (emailAddress) { /* implementation */ }
```

10. Оставляйте осмысленные комментарии

```js
/**
 * Возвращает x в степени n, только для натуральных n
 *
 * @param {number} x Число для возведения в степень.
 * @param {number} n Показатель степени, натуральное число.
 * @return {number} x в степени n.
 */
function pow(x, n) {
  ...
}
```