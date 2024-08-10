# Explanation

- similar to [useState](useState.md) when updating _next State_ based on _previous state_
- Why it is better _useState_?
    - can updated multiple states at the same time
    - can manage all states in one place, which will help to manage
    - Simial to config files in [MVC](../../../Projects/18-Forkify/MVC.md) Architecture, Check forkify project
    -
- action type have a specified naming convention _stateDomain/action_

```
account/deposit
app/load
app/loading
questions/next
```

# Implementation

```js
function reducerFunc(previousState, action){

	return {newState};// based on action type
}
function Component(){
	const [state, dispatch]=useReducer(reducerFunc, initialState);

	// update state
		dispatch({type:hello, payload:10});// dispatch(action);
}
```

# Sources

- Udemy React Jonas| section 14
