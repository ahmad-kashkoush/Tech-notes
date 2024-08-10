## What Is it?
It is a way to get copy of certain elements from the array and assigning them to variables

## Examples
```JS
    // ! Array destructing
const arr = [2, 3, 4];
const [a, b, c] = arr;
console.log(a, b, c);
//  to take first and third
const [x, , y] = arr;
console.log(x, y); //2, 4
```

### Nested Destructing 🥤
```js
const arr1 = [1, 2, 3, [4, 5]];
const [i, , , [j, k]] = arr1;// need first and last
console.log(i, j, k);
```
### You can set Default values before destructing
```js
const [h = 1, m = 1, n = 1, t = 10] = arr;
console.log(h, m, n, t);
```

---
Links Related
[000 Javascript](000%20Javascript.md)
