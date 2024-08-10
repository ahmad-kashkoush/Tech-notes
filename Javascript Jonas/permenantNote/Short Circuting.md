#### It will return **OR ||** 🚀

1. first truthy value for
2. last **falsy Value** if no truthy💥

```js
console.log(3 || 'Kashkoush'); // 3
console.log(0 || NaN || null || undefined); // undefined because it is the last
```

#### It will return **AND &&**🚀

    1. first falsy Value if exists
    2. last truty Value if no falsy

```js
console.log(0 && 'kashkoush'); //0
console.log('ahmed' && 'mohamed' && 1 && 'last truty Value'); // last Truthy Value
```

### Nullish Value Operator ??

- It is the same as ||
- || falsy values are (0, '',Undefined, null,false)
- ?? falsy values or **nullish values** are (null, undefined)

```js
const value = 0;
// ! I want to get the value if it is defined
let guess = value || 10; // 10 which is wrong
guess = value ?? 10; // 0 which is true
```
