### 数组扩展
1. 扩展运算符
```
console.log(...[1, 2, 3])
// 复制数组
const a1 = [1, 2];
const a2 = [...a1];
// 合并数组
[1, 2, ...more]
```
2. Array.from()
Array.from方法用于将两类对象转为真正的数组：类似数组的对象（array-like object）和可遍历（iterable）的对象（包括 ES6 新增的数据结构 Set 和 Map）。
```
let arrayLike = {
    '0': 'a',
    '1': 'b',
    '2': 'c',
    length: 3
};

// ES6的写法
let arr2 = Array.from(arrayLike); // ['a', 'b', 'c']

Array.from('hello'); // ['h', 'e', 'l', 'l', 'o']
```
5. 数组实例的 find() 和 findIndex()
数组实例的find方法，用于找出第一个符合条件的数组成员。它的参数是一个回调函数，所有数组成员依次执行该回调函数，直到找出第一个返回值为true的成员，然后返回该成员。如果没有符合条件的成员，则返回undefined。
```
[1, 4, -5, 10].find((n) => n < 0) // -5
[1, 5, 10, 15].find(function(value, index, arr) {
  return value > 9;
}) // 10
[1, 5, 10, 15].findIndex(function(value, index, arr) {
  return value > 9;
}) // 2
```
8. 数组实例的 includes()
```
[1, 2, 3].includes(2)     // true
[1, 2, 3].includes(4)     // false
[1, 2, NaN].includes(NaN) // true
```