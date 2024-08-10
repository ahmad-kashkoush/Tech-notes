# Explanation

- _Module Pattern_: Functionality Encapsulation to
    1.  Have private Date
    2.  Expose public API
- It Depends on
    - IFFE Function: Destroyed after a single callback
    - with [closure](../../React/closure.md) I can return public data as an API

```js
// iffee
const objectIExport=(function(){
// Closure Concept
// 1. code destroyed
return{
// 2. public data returned
	var1,
	fun2,
	fun3
}
})()
export objectIExport;
```
