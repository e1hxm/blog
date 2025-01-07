+++
date = '2025-01-06T18:53:24+03:00'
title = 'Hello, World! на Си'
categories = [ "c" ]
+++

Короткий кусок кода из учебника 

>"Программирование на С для начинающих"

Пример вывода простого текста в консоль
с помощью printf()

```c
#include <stdio.h>
main()
{
    printf("Hello, World!");
    return 0;
}
```

Интересно что делают `<stdio.h>` `include` и `return 0` тем более возвращает `0`.

Запустил через `code runner` вроде заработало,
хотя и с ошибками в функции `main()`

```c
tempCodeRunnerFile.c:2:1: warning: return type defaults to ‘int’ [-Wimplicit-int]
    2 | main()
      | ^~~~
Hello, World!
[Done] exited with code=0 in 0.097 seconds
```
