# Explanation
- [Higher Order Function](Higher%20Order%20Function.md) that Builds Generic Functions like addEventListener
## Implementation
```js
const oneWord = function (str) {
  return str.replaceAll(' ', '').toLowerCase();
};
const firstUpper = function (str) {
  const [first, ...other] = str.split(' ');
  return [first.toUpperCase(), ...other].join(' ');
};

// Notice that transform is a ⭐⭐generic function⭐⭐ [interface] 
// [reflect] on factory Design Pattern 🤔

const transform = function (str, func) {
  // higher Order Function
  console.log(func(str));
  console.log(func.name);
};
transform('ahmed Kashkoush', oneWord);
transform('ahmed Kashkoush', firstUpper);
```

# Sources
- Extends [](Higher%20Order%20Function.md#Sources)