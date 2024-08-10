## What Is it?

like [Array Destructing](Array%20Destructing.md) you want to copy some elements from Objects and assign them to variables

## Object Sample I'm working on

```js
const restaurant = {
	name: "Classico Italiano",
	location: "Via Angelo Tavanti 23, Firenze, Italy",
	categories: ["Italian", "Pizzeria", "Vegetarian", "Organic"],
	starterMenu: ["Focaccia", "Bruschetta", "Garlic Bread", "Caprese Salad"],
	mainMenu: ["Pizza", "Pasta", "Risotto"],

	openingHours: {
		thu: {
			open: 12,
			close: 22,
		},
		fri: {
			open: 11,
			close: 23,
		},
		sat: {
			open: 0, // Open 24 hours
			close: 24,
		},
	},
};
```

## Examples for Destrucing

```js
// {prepertyName In the object}=object==>object.prpertyName
const { name, openingHours } = restaurant;
// console.log(name, openingHours);
```

### Can't assign to the block

```js
let [a, b] = [10, 15];
const obj = { a: 20, b: 30 };
```

Now I want to change the values of variables to be like the object

```js
// this won't work, you can't assign value to a block
{ a, b } = obj;
// solution ⭐⭐
({a, b}=obj);// will work now
```

### Nested Objects

```js
// Nested Objects 🫨
const parentObject = {
	nestedObject: {
		property1: "property1",
		property2: "property2",
	},
};
const { nestedObject: oo } = parentObject;
// what about calling the inner properties?
const {
	nestedObject: { property1: p1 },
} = parentObject;
console.log(p1, p2);
```

---

Links related
[_MOC Javascript Jonas](_MOC%20Javascript%20Jonas)
