# Explanation
- Any values added between tags
1. Reached from wrapper comp using _children prop_
```js
// Component
<Button prop1="" prop2="">
	<span> Click me </span>
</Button>

// how to get it
function Button({prop1, prop2, **children**}){
	reutrn (<button>{children}</button>)
}
```
