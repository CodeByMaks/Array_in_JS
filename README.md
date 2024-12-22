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
