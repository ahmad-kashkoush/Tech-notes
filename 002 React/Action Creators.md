# Explanation
- Functions return action object
```js
const deposit = (amount) => ({ type: "account/deposit", payload: amount });

// ❌ Without action creator
 store.dispatch({ type: "account/deposit", payload: 500 });


// ✅ with action creator
store.dispatch(deposit(500));
```
1. Use [[Thunks]] for [[Asynchronous]] operations in action creators

# Sources
