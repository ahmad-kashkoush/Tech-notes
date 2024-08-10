### What is it?

- It is the opposite of array destructering
- It packets values into an array or a datastructure in general
- can be used to add as much arguments as you can to a prameter and deal with it as an array check this [#Rest Pattern with Functions](#Rest%20Pattern%20with%20Functions)

### Some Examples

#### Destructring On Arrays

```js
// packets values into array
const [a, b, , ...arrWithRestPattern] = [1, 2, 3, 4, 5]; // arrWithRestPattern=[allElements after last variable assigned];
console.log(a, b, ...arrWithRestPattern);

const [pizza, , Risotto, ...allOtherFood] = [
	...restaurant.mainMenu,
	...restaurant.starterMenu,
];
//allOtherFood will take all values after third element of the array
// doesn't contain **skipped** Element
console.log(pizza, Risotto, allOtherFood);
```

#### Destructuring On Objects

```js
// I want to take sat and all others be stored in weekDays
const { sat, ...weekDays } = restaurant.openingHours;
console.log(weekDays);
```

#### Rest Pattern with Functions

```js
// [Problem] create a function that accept any number of parameters and sum all of them
const add = function (...numbers) {
	// arguments will packed into array called number
	let sum = 0;
	for (let i = 0; i < numbers.length; i++) sum += numbers[i];
	return sum;
};
console.log(add(1, 2));
console.log(add(1, 2, 3, 4));
const arr10 = [2, 3, 4, 5, 3, 2];
console.log(add(1, 2, 3, 4, 5, 5, 5, 242, 23, 4, ...arr10)); // arr10 will be expeanded
```


