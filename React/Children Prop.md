- add HTML between component tags
- to get them in component use _Children Prop_

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
