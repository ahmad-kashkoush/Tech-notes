# Explanation

- a [Redux Toolkit](Redux%20Toolkit.md) function
- forces you to type your reducer and its action creators in a different way
- Reduces boilerPlate code

```js
const accountSlice = createSlice({
	name,
	initialState,
	reducers:{/*pass your action creators*/}
}
```

## multiple arguments action creators

- by default actions creators accepts 1 argument

```js
reducers:{
	actionCreator1(state, action){
	// action.payload will be a single value
	}
}
```

- Solution is to use `prepare` before enrolling reducer
- also if there is some computations do them inside prepare function

```js
reducers: {
	prepare(parameter1, parameter2){
		return {payload:{parameter1, parameter2}}
	reducer(state, action){
		// action.payload will container all parameters
	}
	}
}
```

- Another Solution is to pass an object

```js
actionCreator({prop1:val1, prop2:val2, prop3:val3})
	//action.paylod=passed object
```

# Sources
