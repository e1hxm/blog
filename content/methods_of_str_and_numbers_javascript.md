+++
date = '2025-01-16T19:53:24+03:00'
title = 'Методы строк и чисел в JavaScript'
categories = [ "javascript" ]
+++

Самые простые и часто используемые методы для строк и чисел в JavaScript. 
Эти методы помогут выполнять базовые операции без сложностей.

### Простые методы строк

#### toUpperCase()

Преобразует строку в верхний регистр

```js
const str = "hello";
console.log(str.toUpperCase()); // "HELLO"
```

#### toLowerCase()

Преобразует строку в нижний регистр

```js
const str = "HELLO";
console.log(str.toLowerCase()); // "hello" 
```

#### trim()

Удаляет пробелы с начала и конца строки

```js
const str = "  Hello  ";
console.log(str.trim()); // "Hello"
```

#### slice(start, end)

Возвращает часть строки от start до end (не включая end)

```js
const str = "Hello World";
console.log(str.slice(0, 5)); // "Hello"
```

#### replace(old, new)

Заменяет первое вхождение подстроки `old` на `new`

```js
const str = "Hello World";
console.log(str.replace("World", "JavaScript")); // "Hello JavaScript"
```

### Простые методы чисел

#### toFixed(digits)

Возвращает строку, представляющую число с 
фиксированным количеством цифр после запятой

```js
const num = 3.14159;
console.log(num.toFixed(2)); // "3.14"
```

#### toString(radix)

Преобразует число в строку.

```js
const num = 10;
console.log(num.toString()); // "10"
```

#### Number()

Функция `Number()` преобразует значение в число

```js
console.log(Number("42")); // 42
```

#### parseInt()

Преобразует строку в целое число

```js
console.log(parseInt("42")); // 42
console.log(parseInt("42abc")); // 42
```

#### Унарный плюс (+)

Унарный плюс преобразует значение в число

```js
console.log(+"42"); // 42
console.log(+"42abc"); // NaN
console.log(+true); // 1
console.log(+false); // 0
```