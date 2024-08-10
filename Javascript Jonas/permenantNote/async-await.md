## async

- make a function run in the background
- when done return  [Promises](Promises.md).

```js
const fun = async function () {
	lablabla;
};
// the above look like the following
const fun = function () {
	return new Promise(function (resolve, reject) {
		lablabla;
	});
};
```

## await

makes the async code wait untill the promise is fullifilled either resolved or rejected

```js
const fun = async function () {
	const prmse = await fetch("lablabl");
	console.log(prmse);
};
// the above look like the following
const fun = function () {
	return new Promise(function (resolve, reject) {
		const prmse = fetch("lablbla").then((prmse) => console.log(prmse));
	});
};
```
