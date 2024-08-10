# Explanation

- min and max: does **Type Coersion** not parsing
- **_Type Coersion_**: if there is units, then Nan
- **_parsing_**: Removing Units

```js
console.log(Math.max("23", 1, 2, 3)); //23
console.log(Math.max("23px", 1, 2, 3)); //NaN
```
