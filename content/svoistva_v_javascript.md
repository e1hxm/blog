+++
date = '2025-01-16T18:53:24+03:00'
title = 'Свойства строк и чисел в JavaScript'
categories = [ "javascript" ]
+++

В JavaScript у строк и чисел есть свойства, которые предоставляют полезную информацию о них.

#### Свойства строк

Строки в JavaScript имеют одно основное свойство `length`

>Возвращает количество символов в строке

>Это свойство только для чтения (его нельзя изменить)

```js
const str = "Hello, Elle!";
console.log(str.length); 
```

<p class="gray">
Синтаксис свойств строк и чисел в отличие от методов пишется 
без скобок в конце.
</p>

#### Свойства чисел

У чисел есть статические свойства, такие как `MAX_VALUE`, `MIN_VALUE`, `NaN`, `POSITIVE_INFINITY`, `NEGATIVE_INFINITY`, `EPSILON`, `MAX_SAFE_INTEGER` и `MIN_SAFE_INTEGER`, которые предоставляют информацию о числовых константах и ограничениях.

