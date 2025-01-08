+++
date = '2025-01-08T18:54:24+03:00'
title = 'Оператор typeof() в JavaScript'
categories = [ "javascript" ]
+++

Оператор `typeof()` возвращает тип данных аргумента.

Полезная команда если нужно выяснить, 
например какой тип данных возвращает 
форма на сайте.

У `typeof()` существует два варианта синтаксиса:

>Синтаксис оператора `typeof x`

>Синтаксис функции `typeof(x)`

Оба синтаксиса работают одинаково.

`typeof()` возвращает строку, которая содержит
тип данных.

```js
typeof undefined // "undefined"

typeof 0 // "number"

typeof 1n // "bigint"

typeof true // "boolean"

typeof "foo" // "string"

typeof Symbol() // "symbol"

typeof {} // "object"

typeof null // "object"  

typeof function(){} // "function" 
```

Нужно обратить внимание на `null`, так как это не 
объект а отдельный тип данных. Это официально признанная ошибка в языке.

