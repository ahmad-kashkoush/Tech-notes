# Explanation
- A [[Redux Toolkit]] function to reduce boilerPlate code (Code: [[#Initial Code]])
1. By defaults accepts single argument (Code: [[#Single paramater code]])
2. A workaround to allow multiple arguments
	1. use prepare before enrolling reducer (code: [[#Using prepare]]).
	2. Pass arguments as a single object (code: [[#Object Passing]])
## Initial Code
```js
const accountSlice = createSlice({
	name,
	initialState,
	reducers:{/*pass your action creators*/}
}
```

## Single paramater code
```js
reducers:{
	actionCreator1(state, action){
	// action.payload will be a single value
	}
}
```

## Using prepare
1. Better for allowing computations before enrolling reducer
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

## Object Passing
```js
actionCreator({prop1:val1, prop2:val2, prop3:val3})
	//action.paylod=passed object
```

# Sources
