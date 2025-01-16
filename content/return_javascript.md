+++
date = '2025-01-15T19:53:24+03:00'
title = 'Оператор return в Javascript'
categories = [ "javascript" ]
+++

Оператор `return` в JavaScript используется для возврата значения из функции. Когда интерпретатор встречает `return`, выполнение функции прекращается, и управление возвращается туда, где функция была вызвана. Если после `return` указано значение, оно возвращается как результат функции.

`return` может вернуть любое значение: число, строку, объект, массив, другую функцию и даже `null` или `undefined`.

Как только выполняется `return`, функция сразу завершает свою работу. Код, который находится после `return`, не выполняется.

Если `return` используется без значения, функция возвращает `undefined`.

```js
function имяФункции() {
  // Код функции
  return значение; // Возврат значения и завершение функции
}
```

Возврат числа:

```js
function sum(a, b) {
  return a + b; // Возвращает сумму a и b
}

const result = sum(2, 3); // result = 5
console.log(result); // Выведет: 5
```

Возврат строки:

```js
function greet(name) {
  return "Привет, " + name + "!";
}

const message = greet("Elle"); // message = "Привет, Elle!"
console.log(message); // Выведет: "Привет, Elle!"
```

Возврат объекта:
```js
function createUser(name, age) {
  return { name: name, age: age }; // Возвращает объект
}

const user = createUser("Mia", 25);
console.log(user); // Выведет: { name: "Мia", age: 25 }
```

Возврат без значения:
```js
function doSomething() {
  console.log("Делаю что-то...");
  return; // Функция завершается, возвращает undefined
  console.log("Этот код не выполнится");
}

const result = doSomething(); // result = undefined
console.log(result); // Выведет: undefined
```

`return` может использоваться для досрочного завершения функции, если выполнение дальнейшего кода не требуется.

```js
function checkAge(age) {
  if (age < 18) {
    return "Доступ запрещён"; // Функция завершается, если age < 18
  }
  return "Доступ разрешён"; // Выполняется, если age >= 18
}

console.log(checkAge(15)); // Выведет: "Доступ запрещён"
console.log(checkAge(20)); // Выведет: "Доступ разрешён"
```

Использование return делает функции более гибкими и мощными, позволяя им взаимодействовать с остальным кодом.