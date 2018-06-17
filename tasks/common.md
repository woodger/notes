# Задачи

## Сумматор

Написать функцию, которая будет выполнять сложение

```js
summ(1)(2)(5)(); // 8

function summ(a) {
  let buf = 0;

  function calc(a) {
    if (a === undefined) {
      return buf;
    }
    else {
      buf += a;
      return calc;
    }
  }

  return calc(a);
}
```

## Сортировщик

```js
sort('lorem ipsum dolor sit amet'); // Sit amet lorem ipsum dolor

function sort(str) {
  const arr = str.split(' ');

  arr.sort((a, b) => {
    return a.length - b.length;
  });

  str = arr.join(' ');

  const res = str[0].toUpperCase() + str.substr(1);

  return res;
}
```
