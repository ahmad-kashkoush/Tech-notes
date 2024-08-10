- _Definition_:
    - a technique or pattern
    - use to enhance component features without modifying anything in it
    - By Creating a component that:
        - accepts component needs modification
        - returns a new component with new logic wrapped or added to old component

```jsx
Comp1(a, b){
returns c;
}
// b needs to be passed by logic
WithBLogic(comp1){
	return function comp(props){
		updatedB=newLogic;
		return (
			<comp1 {...props} b={updatedB}/>
		);
	}
}

const Comp1WithBLogic=WithBLogic(comp1);

function App(){

	return (
		<>
			<Comp1  a={a} b={b}/>
			// b will be updated inside
			<Comp1WithBLogic a={a} b={b} />
		</>
	);
}

```
