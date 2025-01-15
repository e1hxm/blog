+++
date = '2025-01-14T18:55:24+03:00'
title = 'Function Declaration в JavaScript'
categories = [ "javascript" ]
+++

Function Declaration (объявление функции) — это один из способов создания функций в JavaScript.

Синтаксис Function Declaration:
```js
function имяФункции(параметры) {
  // тело функции
}
```

>`function` — ключевое слово, которое указывает на объявление функции.

>`имяФункции` — имя функции, которое используется для её вызова.

>`параметры` — аргументы, которые передаются в функцию (необязательно).

>`тело функции` — код, который выполняется при вызове функции.

Пример Function Declaration:

```js
function greet(name) {
  console.log(`Hello, ${name}!`);
}

greet("Elle"); // Hello, Elle!
```

Особенности Function Declaration:

>Function Declaration "поднимается" (hoisted) вверх своей области видимости. Это означает, что функцию можно вызвать до её объявления в коде.

```js
greet("Elle"); // Hello, Elle!

function greet(name) {
    console.log(`Hello, ${name}!`);
}
```

Function Declaration — это классический способ объявления функций в JavaScript. Он удобен для создания именованных функций, которые могут быть вызваны до их объявления благодаря hoisting. Однако в современных проектах часто используются стрелочные функции и Function Expression для более гибкого и компактного кода.