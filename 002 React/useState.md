- State Initialization:
	- Can be Hard coded (Code: [[#Hard code initalization]])
	- Can be computed using _lazy Initializing_ (Code: [[#Lazy initialization]])
- State Updating: using setState
	- Check [[#How setState works]].
- ![[useState - Definning & updaing.png]]
# How setState works
1. React scheduels changes to component and its children
2. Batches updates
	- Proccess multiple setState calls before re-rendering
	- 1 re-render for multiple updates
	- better performance 
- Asyncronous nature
    - Creates a pending state transition on mutating state.
    - New state value is available **after rendering**
- Callbacks (as second argument) executed after commiting update.
- Passing a callback  ensures working with correct previous state:(Code: [[#setState callback]]).
# Hard code initalization
```js
const [query, setQuery] = useState("");
```

# Lazy initialization
- Based on a function
```js
const [watched, setWatched] = useState(function () {
    const storedWatched = localStorage.getItem("watched");
    return storedWatched ? JSON.parse(storedWatched) : [];
  });

```
# setState callback 
- receives the previous state as its argument
- returns an object to merge into the new state
```js
function Hello() {
	const [state, setState] = useState(0);
	setState(state + 1); // Previous state Update
	setState(state + 1); // won't work ❌
	setState((prevState) => prevState + 1); // will work ✅
	return <div>{state}</div>;
}
```

# Sources

- [Phind](https://www.phind.com/agent?cache=clsdjk2fp002cjs08tkbn81t5&source=sidebar)
- Udemy React Jonas | section 6 | Updating State based on currenct state
