# Array_in_JS

# Array 

---

<div align="center">
  <img src="https://miro.medium.com/v2/resize:fit:2000/1*dhTC_FFgiH3mKROrnDj12w.gif" width="600px" height="300px">
</div>

---


В JavaScript массив (array) — это структура данных, которая используется для хранения упорядоченных коллекций элементов. Каждый элемент массива имеет индекс, начиная с 0. Массивы могут содержать данные любых типов: числа, строки, объекты, другие массивы и т. д.

### Создание массива
> С помощью литерала массива:
```js
const arr = [1, 2, 3, 4, 5];
```

### С помощью конструктора Array:
```js
const arr = new Array(5); // Создаст массив длиной 5
const arr2 = new Array(1, 2, 3); // Создаст массив [1, 2, 3]
```
### Доступ к элементам массива
> Элементы массива можно получить, указав их индекс:
```js
const arr = ['яблоко', 'банан', 'вишня'];
console.log(arr[0]); // 'яблоко'
console.log(arr[2]); // 'вишня'
```

## Методы массивов
### Добавление и удаление элементов:

* push() — добавляет элемент в конец массива:
```js
const arr = [1, 2, 3];
arr.push(4);
console.log(arr); // [1, 2, 3, 4]
```
* pop() — удаляет последний элемент массива:
```js
const arr = [1, 2, 3];
arr.pop();
console.log(arr); // [1, 2]
```
* unshift() — добавляет элемент в начало массива:
```js
const arr = [1, 2, 3];
arr.unshift(0);
console.log(arr); // [0, 1, 2, 3]
```
* shift() — удаляет первый элемент массива:
```js
const arr = [1, 2, 3];
arr.shift();
console.log(arr); // [2, 3]
```

### Итерация по массиву:

* for:
```js
const arr = [1, 2, 3];
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
forEach():
arr.forEach(element => console.log(element));
```
### Поиск и фильтрация:

* find() — возвращает первый элемент, удовлетворяющий условию:
```js
const arr = [5, 12, 8, 130, 44];
const found = arr.find(element => element > 10);
console.log(found); // 12
```

* filter() — возвращает новый массив с элементами, удовлетворяющими условию:
```js
const arr = [1, 2, 3, 4, 5];
const result = arr.filter(num => num > 2);
console.log(result); // [3, 4, 5]
```

### Изменение массива:

* map() — создаёт новый массив, преобразуя элементы:
```js
const arr = [1, 2, 3];
const squared = arr.map(num => num * num);
console.log(squared); // [1, 4, 9]
```

### Объединение и разделение:

* concat() — объединяет массивы:
```js
const arr1 = [1, 2];
const arr2 = [3, 4];
const result = arr1.concat(arr2);
console.log(result); // [1, 2, 3, 4]
```
* join() — объединяет элементы массива в строку:
```js
const arr = ['а', 'б', 'в'];
console.log(arr.join('-')); // 'а-б-в'
```

### Сортировка:

* sort() — сортирует массив:
```js
const arr = [3, 1, 4, 1, 5];
arr.sort();
console.log(arr); // [1, 1, 3, 4, 5]
```

### Проверка массива:

* Array.isArray() — проверяет, является ли объект массивом:
```js
console.log(Array.isArray([1, 2, 3])); // true
console.log(Array.isArray({})); // false
```

### Длина массива
> Свойство length показывает количество элементов в массиве:
```js
const arr = [1, 2, 3];
console.log(arr.length); // 3
```

## Особенности массивов в JavaScript
* Массивы в JavaScript являются объектами.
* Индексы массива не обязательно должны быть последовательными.
* Можно хранить элементы разных типов:
```js
const arr = [1, 'строка', { ключ: 'значение' }, [1, 2, 3]];
```

# Js mechanism

---


<div align="center">
  <img src="https://miro.medium.com/v2/resize:fit:900/1*suCZqN8rjlN6MWcQs6pHhg.png" width="600px" height="300px">
</div>


---

# Destructuring

Деструктуризация (destructuring) в JavaScript — это удобный способ извлечения значений из массивов или свойств объектов и присваивания их переменным с помощью синтаксиса, похожего на литералы массива или объекта. Этот метод делает код более лаконичным и читаемым.

### Извлечение значений из массива:
```js
const arr = [1, 2, 3];
const [a, b] = arr;
console.log(a); // 1
console.log(b); // 2
```

### Пропуск элементов:
```js
const arr = [1, 2, 3];
const [, second] = arr;
console.log(second); // 2
```

### Деструктуризация объекта
> Извлечение значений из объекта:
```js
const user = { name: 'John', age: 30 };
const { name, age } = user;

console.log(name); // 'John'
console.log(age);  // 30
```

### Переименование переменных:
```js
const user = { name: 'John' };
const { name: userName } = user;

console.log(userName); // 'John'
```

### Дефолтные значения
> Для массива:
```js
const arr = [1];
const [a, b = 2] = arr;

console.log(b); // 2
```

> Для объекта:
```js
const user = { name: 'John' };
const { age = 25 } = user;

console.log(age); // 25
```

# Spread syntax

Spread syntax в JavaScript используется для удобного копирования элементов массивов, свойств объектов или передачи аргументов в функции. Она представлена тремя точками (...) перед массивом, объектом или выражением.

## Spread в массивах
### Копирование массива:
```js
const arr1 = [1, 2, 3];
const arr2 = [...arr1];
console.log(arr2); // [1, 2, 3]
```

### При этом сохраняется независимость массивов:
```js
arr2.push(4);
console.log(arr1); // [1, 2, 3]
console.log(arr2); // [1, 2, 3, 4]
```

### Объединение массивов:
```js
const arr1 = [1, 2];
const arr2 = [3, 4];
const combined = [...arr1, ...arr2];
console.log(combined); // [1, 2, 3, 4]
```
### Добавление элементов:
```js
const arr = [2, 3];
const newArr = [1, ...arr, 4];
console.log(newArr); // [1, 2, 3, 4]
```

## Spread в объектах
### Копирование объекта:
```js
const obj1 = { a: 1, b: 2 };
const obj2 = { ...obj1 };
console.log(obj2); // { a: 1, b: 2 }
```
> Как и с массивами, объект obj2 независим от obj1.

### Объединение объектов:
```js
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };
const combined = { ...obj1, ...obj2 };
console.log(combined); // { a: 1, b: 3, c: 4 }
```
> Если свойства совпадают, значения из последнего объекта (obj2) перезаписывают предыдущие.

### Добавление новых свойств:
```js
const obj = { a: 1, b: 2 };
const updated = { ...obj, c: 3 };
console.log(updated); // { a: 1, b: 2, c: 3 }
```

## Spread для передачи аргументов
### Использование с функциями:
```js
const nums = [1, 2, 3];
const sum = (x, y, z) => x + y + z;
console.log(sum(...nums)); // 6
```

## Примечания
* Spread создаёт поверхностную копию. Если объект или массив содержат вложенные структуры (например, массивы или объекты), они сохраняют ссылку:
```js
const nested = { a: 1, b: { c: 2 } };
const copy = { ...nested };
copy.b.c = 42;
console.log(nested.b.c); // 42
```

# Rest parametr

Rest-параметры в JavaScript позволяют объединять неограниченное количество аргументов функции в массив. Они определяются с помощью тех же трёх точек (...), что и spread-синтаксис, но используются в другом контексте — при объявлении функции.

### Основные особенности:
* Rest-параметры собирают оставшиеся аргументы в массив.
* Они всегда должны быть последними в списке параметров функции.
* В одной функции может быть только один rest-параметр.

### Синтаксис Rest-параметров
```js
function myFunction(a, b, ...rest) {
  console.log(a); // Первый аргумент
  console.log(b); // Второй аргумент
  console.log(rest); // Массив с остальными аргументами
}

myFunction(1, 2, 3, 4, 5);
// a = 1
// b = 2
// rest = [3, 4, 5]
```

### Примеры использования:
* Суммирование всех переданных аргументов:
```js
function sum(...numbers) {
  return numbers.reduce((total, num) => total + num, 0);
}

console.log(sum(1, 2, 3, 4)); // 10
console.log(sum(5, 10)); // 15
```

### Разделение первых аргументов и остальных:
```js
function greet(first, ...names) {
  console.log(`Hello, ${first}!`);
  console.log(`Also greeting: ${names.join(', ')}`);
}

greet('Alice', 'Bob', 'Charlie', 'Dave');
// Hello, Alice!
// Also greeting: Bob, Charlie, Dave
```

### Создание функций с переменным числом аргументов:
```js
function logAll(...args) {
  args.forEach((arg, index) => console.log(`Argument ${index}:`, arg));
}

logAll('a', 42, true, { key: 'value' });
// Argument 0: a
// Argument 1: 42
// Argument 2: true
// Argument 3: { key: 'value' }
```

## Отличие Rest от Spread:
### Rest собирает аргументы в массив:
```js
function example(...args) {
  console.log(args); // Массив аргументов
}

example(1, 2, 3); // [1, 2, 3]
```

### Spread "разворачивает" массив или объект в отдельные элементы:
```js
const arr = [1, 2, 3];
console.log(...arr); // 1 2 3
```

---

<div align="center">
  <img src="https://a.d-cd.net/fGkj61MC91njUbKjZUahzEm1-IA-960.jpg" width="600px" height="300px">
</div>

---
