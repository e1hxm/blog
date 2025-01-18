+++
date = '2025-01-15T18:53:24+03:00'
title = 'Аргументы в функциях JavaScript'
categories = [ "javascript" ]
+++

В JavaScript аргументы — это значения, которые передаются в функцию при её вызове. Они позволяют функциям принимать данные и работать с ними. Аргументы могут быть любого типа: числа, строки, объекты, массивы, другие функции и т.д.

В функциях в Javascript есть параметры и аргументы.

Параметры функции - это переменные, указанные в определении функции. Они используются для работы с аргументами, переданными при вызове функции.

```js
function greet(name) { // name — параметр
  console.log(`Hello, ${name}!`);
}
```

Аргументы функции - это значения, которые передаются в функцию при её вызове.
```js
greet("Elle"); // "Elle" — аргумент
```

Аргументы передаются по значению:

1.  Примитивные типы (числа, строки, булевы значения) 
    передаются по значению. Это означает, что функция работает с копией значения, и изменения 
    внутри функции не влияют на оригинальное значение.
  
2.  Объекты и массивы передаются по ссылке. Это означает, что функция работает с оригинальным 
    объектом, и изменения внутри функции влияют на оригинальный объект.

```js
function changeValue(a, b) {
  a = 10;
  b.value = 20;
}

let num = 5;
let obj = { value: 15 };

changeValue(num, obj);
console.log(num); // 5 (не изменилось)
console.log(obj.value); // 20 (изменилось)
```

Функции могут принимать любое количество аргументов:
1.  Если передано больше аргументов, чем параметров, 
    лишние аргументы игнорируются.

2.  Если передано меньше аргументов, чем параметров, 
    недостающие параметры получают значение `undefined`.

```js 
function sum(a, b) {
  return a + b;
}

console.log(sum(1, 2, 3)); // 3 (третий аргумент игнорируется)
console.log(sum(1)); // NaN (b = undefined, 1 + undefined = NaN)
```

Несколько примеров использования аргументов:

Простая функция с аргументами:

```js
function add(a, b) {
  return a + b;
}

console.log(add(2, 3)); // 5
```

Функция с параметрами по умолчанию:

```js
function greet(name = "Guest") {
  console.log(`Hello, ${name}!`);
}

greet(); // Hello, Guest!
greet("Elle"); // Hello, Elle!
```

Аргументы — это значения, передаваемые в функцию.

Параметры — это переменные, которые используются для работы с аргументами.

В JavaScript функции могут принимать любое количество аргументов.