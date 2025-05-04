# Explanation
- A [[State Management]] Hook
- Update next based on previous (similar to [[useState]])
- Why use over [[useState]]?
    - Update multiple states at same time
    - All states are managed in same place
    - Simial to config files in [[MVC]] Architecture, Check forkify project
- Code: [[#Initialization]], [[#Reducer function]]
- Action Type naming convention 
```
# state-domain/action
account/deposit
app/load
app/loading
questions/next
```

# Initialization
```ts
function Component(){
	const [state, dispatch]=useReducer(reducerFunc, initialState);
	dispatch({type:hello, payload:10});// dispatch(action);
}
```

# Reducer function
```js
function reducerFunc(previousState, action){

	return {newState};// based on action type
}

```

# Sources

- Udemy React Jonas| section 14

