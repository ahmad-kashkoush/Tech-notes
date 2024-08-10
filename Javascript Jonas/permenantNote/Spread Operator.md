## ... spread operator😶‍🌫️

#### It works on all **Iterables**
1. Strings
2. Arrays
3. maps
4. Sets
5. doesn't work on objects


spread operators create multiple values seperated by comma
Muliptle values seperated by comma only for
1. function arguments
2. array assignments --> const a=...dflj;a

#### Used to avoid array shallow copy

```js
const arr = [1, 2, 3];
const arrCpy = arr;
arrCpy[0] = 10; // I only need to change arrCpy[0] not arr[0]
console.log(arr[0], arrCpy[0]); // arr[0] is changed

// Solution⭐⭐⭐⭐⭐
const deepCpy = [...arr];
deepCpy[2] = 15;
console.log(deepCpy[2], arr[2]); // only deepCpy is changing
```

#### Joining two arrays

```js
const mergedArrays = [...restaurant.starterMenu, ...restaurant.mainMenu];
console.log(mergedArrays);
```

#### passing arguments to functions

```js
const arrIngredients = ['chicken', 'meat', 'cheese'];
restaurant.orderPasta(...arrIngredients);
```

#### Deep Clone for objects and avoid shallow copy 🏆

```js
const newObj = {
  p1: [1, 2, 3, 4, 5, [1, 2, 3]],
};
const newObjCpy = { ...newObj };
// but this copy is for top level properties only
newObjCpy.p1 = [50, 60];
console.log(newObj.p1, newObjCpy.p1);
```
