+++
date = '2025-02-18T18:53:24+03:00'
title = 'Вложенность в препроцессоре SASS'
categories = [ "css" ]
+++

Препроцессор SASS позволяет вкладывать 
CSS правила друг в друга.

Правило вложенное в элемент выше, применяется
только для его селекторов.

Например:

```css
#main p
    color: #F0F0F0;
    width: 100%;
    .graybox: 
        background-color: #A9A9A9;
```

В результате получим в CSS файле:

```css
#main p {
    color: #F0F0F0;
    width: 100%;
}

#main p .graybox {
    background-color: #A9A9A9;
}
```

Использование препроцессора в проекте, 
помогает избежать повторения написания 
родительских селекторов. Что значительно 
облегчает написание макетов с большим
объемом вложенных CSS селекторов.

Еще один пример:

```css
#main 
    width: 100%;

    p, div 
        font-size: 2rem;

        a 
            font-weight: bold;
    pre
        font-size: 3rem;
```

После обработки получаем CSS код:

```css
#main {
    width: 100%;
}
#main p, #main div {
    font-size: 2rem;
}
#main p a, #main div a {
    font-weight: bold;
}
#main pre {
    font-size: 3rem;
}
```

Стоит привыкнуть к синтаксису 
препроцессора поскольку это намного
экономит написание CSS правил.