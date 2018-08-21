
### Вывести первые (по лексикографическому порядку) 10 строк (без повторений) из файла  file.txt

```bash
cat file.txt | sort | uniq | head
```

### Что возвращает typeof null?

```js
'object'
```

### Что вернет typeof typeof foo

```js
'string'
```

### Что вернёт этот код typeof (function(){})()

```js
'undefined'
```

### Что вернет следующий код

```js
['1', 'z', '0', 2, true, false, {}, [], undefined, [0], ''].filter(Boolean);
// ['1', 'z', '0', 2, true, {}, [], [0]]
```

### Что выведет данный код?

```js
var b = {};
var c;

b.b = 1;
c = b;
c.b = 2;

console.log('1)', b.b); // ?
console.log('2)', c.b); // ?

var a = { counter: 1 };
function inc(obj) {
    obj.counter++;
    obj.changed = true;
}

inc(a);
console.log('3)', a);   // ?

var d = 'test';
d.d = 1;
console.log('4)', d.d); // ?

/*
1) 2
2) 2
3) {counter: 2, changed: true}
4) undefined
*/
```

### FizzBuz

Вывести на экран числа от 1 до 100.
При этом вместо чисел, кратных трем, программа должна выводить слово «Fizz»,
а вместо чисел, кратных пяти — слово «Buzz». Если число кратно и 3, и 5,
то программа должна выводить слово «FizzBuzz».

```js
((a, b) => {
  for (; a <= b; a++) {
    let buf = '';

    if (a % 3 === 0) {
      buf += 'Fizz';
    }

    if (a % 5 === 0) {
      buf += 'Buzz';
    }

    console.log(buf === '' ? a : buf);
  }
})(1, 100);
```

### Реализовать map и filter на reduce

```js
Array.prototype.map = function (callback) {
  if (typeof callback !== 'function') {
    throw new TypeError('undefined is not a function at Array.map (<anonymous>) at <anonymous>');
  }

  return this.reduce((buffer, current) => {
    const value = callback(current);
    buffer.push(value);

    return buffer;
  },
  []);
};

Array.prototype.filter = function (callback) {
  if (typeof callback !== 'function') {
    throw new TypeError('undefined is not a function at Array.filter (<anonymous>) at <anonymous>');
  }

  return this.reduce((buffer, current) => {
    const value = callback(current);

    if (value) {
      buffer.push(current);
    }

    return buffer;
  },
  []);
};
```

### Палиндром

Написать функцию, определяющую, является ли переданная строка палиндромом (читается слева-направо и справа-налево одинаково).
Примеры палиндромов приведены ниже.

```js
isPalindrome('Казак') // true
isPalindrome('А роза упала на лапу Азора') // true
isPalindrome('Do geese see God?') // true
isPalindrome('Madam, I’m Adam') // true
isPalindrome('Бряк') // false

function isPalindrome(str) {
  str = str.replace(/[^а-яa-z]/gi, '').toLowerCase();

  return Array.prototype.every.call(str, (a, index) => {
    return a === str[str.length - 1 - index];
  });
}
```

### Бинарный поиск
