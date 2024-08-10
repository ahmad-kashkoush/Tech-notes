# Explanation

- Global Scope: accessed from everywhere
- _block scope_: can't be accessed outside if else, loop block
    - let, const, function declarations
- function scope
    - can be accessed from anywhere inside a function

## Implementation

```js
function func() {
	function func2() {
		//function scope
		if (true) {
			// block scope
			const ahmed = "ali";
			var ali = "ahmed";
		}
		console.log(ali); // works because var is function scope
		//console.log(ahmed); // doesn't work
	}
	func2();
	//console.log(ali); // doesn't work because its functionally scoped
}
func();
```
