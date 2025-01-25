+++
date = '2025-01-22T12:55:24+03:00'
title = 'Callback функции в JavaScript'
categories = [ "javascript" ]
+++

Callback-функции в JavaScript — это функции, которые передаются в качестве аргументов другим функциям и выполняются после завершения определенной операции или события. Они широко используются в асинхронном программировании, обработке событий и функциональном программировании.

Пример передачи callback-функции в другую функцию как
аргумента и вызов внутри нее

```js
function greeting(name) {
    console.log("Hello, " + name);
}

function processUserInput(callback) {
    const name = prompt("Please enter your name.");
    callback(name);
}

processUserInput(greeting); // greeting — это callback-функция
```

Callback-функции часто используются для обработки асинхронных операций, таких как запросы к серверу, чтение файлов или таймеры

```js
setTimeout(function() {
    console.log("Это сообщение отобразится после 2 секунд");
}, 2000);
```

Callback-функции используются для обработки событий, таких как клики мыши, нажатия клавиш и т.д.

```js
document.querySelector("button").addEventListener("click", function() {
    console.log("Button clicked!");
});
```
Но тема про обработчиков событий будет пройдена позже 
и разобрана более детально.

К недостаткам callback-функций можно отнести 
так называемый `Callback Hell` (Ад обратных вызовов)

>При большом количестве вложенных callback-функций код становится сложным для чтения и поддержки.

Пример "Callback Hell":

```js
getData(function(a) {
    getMoreData(a, function(b) {
        getEvenMoreData(b, function(c) {
            console.log("Final result:", c);
        });
    });
});
```

Callback-функции остаются важной частью JavaScript, но в современных приложениях их часто заменяют промисами и async/await для улучшения читаемости и поддержки кода.