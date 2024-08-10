- The set Object store unique types either primitive or non-primitive
- It is not like cpp where it sorts the values for you.
- It just gives you unique values.

```js
// you must add an iterable
const mySet = new Set([5, 1, 2, 3, 4, 2, 1]);
console.log(mySet);
```

### Methods and Properties

```js
const mySet = new Set([5, 1, 2, 3, 4, 2, 1]);
mySet.add(20);
mySet.delete(5);
console.log(mySet.has(20)); // true
console.log(mySet.size);
console.log(...mySet);
```

```js
// Get An array of unique values

const arr = [1, 2, 1, 2, 3, 5, 1, 2, 5];
const arrUnique = [...new Set(arr)];
console.log(arrUnique);
```
