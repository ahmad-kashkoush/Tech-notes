- A pattern for enhancing component features without modifying orginial component.
- How?
	- By creating [[#Wrapper component]]
	- Returns enhanced componetn
# original component
- Unmodified
```jsx
Comp1(a, b){
	returns c;
}
```
# Wrapper component
- Accepts [[#original component]]
- Returns enhanced component (With new logic)
```jsx
// b needs to be passed by logic
WithBLogic(comp1){
	return function EhancedComp(props){
		updatedB=newLogic;
		return (
			<comp1 {...props} b={updatedB}/>
		);
	}
}
```

# usage
```jsx
const Comp1WithBLogic=WithBLogic(comp1);
function App(){
	return (
		<>
			<Comp1 
			 a={a} 
			 b={b}
			 />
			// b will be updated inside
			<Comp1WithBLogic
			 a={a}
			  b={b}
		   />
		</>
	);
}
```
