
# Explanation
- ![useState hook summary](useState%20hook%20summary.png)
## useState for initial mounting

- I can Hard code Initial value of the state

```js
const [query, setQuery] = useState("");
```

- I can also initialze it from a certain computing using _lazy Initializing_

```js
const [watched, setWatched] = useState(function () {
    const storedWatched = localStorage.getItem("watched");
    return storedWatched ? JSON.parse(storedWatched) : [];
  });

```

## setState for Update

> [!warning]- You Shouldn't setState in [Render Logic](React%20%20Logic.md)
>
> -   Because You'll cause the Componenet to have inifinte re-renders
> -   ⭐ Solution: [useEffect](useEffect.md)
> -

- `Update State`: setState Used to schedule updates component's state Object
- `Asynchronous nature`:
    - defer updates for performance Optimization
    - If call `this.state` after setState=> you'll find the old value
- `callbacks`:
    - executed after update is commited, and component is re-rendered

```JS
function Hello(){
	const [state, setState]=useState(0);
	setState(state+1);
	return (<div>{state}</div>);
}
```

## Update based on current

### callback as setState argument

- ` setState((prevState) => prevState + 1);`
    - receives the previous state as its argument
    - returns an object to merge into the new state
    - ensures I'm working with correct previous state

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
