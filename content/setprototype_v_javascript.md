+++
date = '2025-02-14T18:53:24+03:00'
title = 'Метод setPrototypeOf в JavaScript'
categories = [ "javascript" ]
+++

Метод `Object.setPrototypeOf()` в JavaScript позволяет динамически установить прототип `[[Prototype]]` для указанного объекта. Это способ изменить прототип объекта после его создания.

```js
Object.setPrototypeOf(obj, prototype);
```

Тут `obj` это объект, прототип которого нужно установить
или изменить.

А `prototype` это новый прототип.

Давайте разберем небольшой пример.

```js
//Прототип
let skillsOfGirls = {
    intro() {
        console.log(`Привет, меня зовут ${this.name}`)
    },
    dance() {
        console.log(`${this.name} танцует!`)
    }
};
//Новый объект
let girl = {
    name: "Elle"
};
//Укажем прототип для girl
Object.setPrototypeOf(girl, skillsOfGirls);

//Обращаемся к методам и используем
girl.intro(); // Привет, меня зовут Elle
girl.dance(); // Elle танцует"
```

Здесь объект `girl` получает доступ к методам `intro` и `dance`
через прототип `skillsOfGirls`

Изменение прототипа на лету может привести к проблемам с производительностью. 

Метод полезен для понимания работы прототипов и наследования в JavaScript.

В большинстве случаев лучше использовать `Object.create()` или классы (ES6) для работы с прототипами.