---
description: просто  база ( основа)
---

# React

#### JS

1. Что нужно  знать о  типа  данных

Примитивные:&#x20;

```javascript
// Infinity  - бесконечность 
let i = 2/0
// Nan  - ошибка 
let i = 34/"test"
// null  - ничего или значение неизвестно 
// undefineds - значение не присвоено 
let  x; 
//  (2^53-1) type number(2^53-1) 
// и  стандартные  
```

Объекты:&#x20;

```javascript
{}
```

2. EventLoop&#x20;

> Движок браузера выполняет JavaScript в одном потоке. Для потока выделяется область памяти — стэк, где хранятся фреймы (аргументы, локальные переменные) вызываемых функций.

3. Замыкания

> "Замыкание" - это способность функции запоминать переменные, которые были определены внутри родительской функции, даже после того, как родительская функция была выполнена.

```javascript
function createCounter() {
  // переменная, которую нужно запомнить
  let count = 0;

  function counter() {
    // увеличиваем нашу запомненную переменную
    count++;
    console.log(count);
  }

  // возвращаем функцию
  return counter;
}

// создаем новую функцию (с замыканием)
const incrementCounter = createCounter();

incrementCounter(); // 1
incrementCounter(); // 2
incrementCounter(); // 3

// Создали еще одну новую функци-счетчик
const newIncrementCounter = createCounter();

newIncrementCounter(); // 1
newIncrementCounter(); // 2
newIncrementCounter(); // 3
```

4. Прототип объекта

> Объекты в JavaScript можно организовать в цепочки так, чтобы свойство, не найденное в одном объекте, автоматически искалось бы в другом. Связующим звеном выступает специальное свойство **proto /** prototype

5. Promis&#x20;

> Promise – это специальный объект, который содержит своё состояние. Вначале pending («ожидание»), затем – одно из: fulfilled («выполнено успешно») или rejected («выполнено с ошибкой»).
>
> Внутри промиса  асинхронно выполняются  методы.

6. Static метод

> Ключевое слово static используется в классах для определения статичных методов. Статичные методы функции, принадлежащие объекту класса, но не доступные другим объектам того же класса.

```javascript
class Repo {
    static getName() {
      return "Repo name is modern-js-cheatsheet"
    }
  }

  // нам не нужно создавать объект класса Repo
  console.log(Repo.getName()) // "Repo name is modern-js-cheatsheet"

  let r = new Repo();
  console.log(r.getName()) // необработанная ошибка TypeError: r.getName не является функцией
```

7.
