+++
date = '2025-01-14T19:55:24+03:00'
title = 'Function Expression в JavaScript'
categories = [ "javascript" ]
+++

Function Expression (функциональное выражение) — это способ создания функции в JavaScript, при котором функция определяется как часть выражения (например, присваивается переменной). В отличие от Function Declaration, Function Expression не поднимается (не hoisted) и может быть анонимной или именованной.

Синтаксис Function Expression:
```js
const имяПеременной = function(параметры) {
  // тело функции
};
```

>`function` — ключевое слово для создания функции.

>`имяПеременной` — переменная, которой присваивается функция.

>`параметры` — аргументы, которые передаются в функцию (необязательно).

>`тело функции` — код, который выполняется при вызове функции.

Пример Function Expression:
```js
const greet = function(name) {
  console.log(`Hello, ${name}!`);
};

greet("Elle"); // Hello, Elle!
```

Function Expression не поднимается вверх области видимости. Это означает, что функцию можно вызвать только после её объявления.
```js
greet("Elle"); // Ошибка: greet is not defined

const greet = function(name) {
  console.log(`Hello, ${name}!`);
};
```

Function Expression может не иметь имени (анонимная функция).
```js
const sum = function(a, b) {
  return a + b;
};
console.log(sum(2, 3)); // 5
```
Function Expression создаётся только тогда, когда выполнение кода доходит до её объявления.

Когда используется Function Expression:

>Function Expression часто используется для создания замыканий, когда функция сохраняет доступ к переменным из внешней области видимости

>Function Expression создаётся только при выполнении кода, что полезно для условного создания функций

>Для передачи функции в качестве аргумента (callback)

Function Expression — это гибкий способ создания функций в JavaScript. Он позволяет создавать анонимные и именованные функции, которые могут быть использованы в различных контекстах, таких как колбэки, методы объектов или замыкания. 