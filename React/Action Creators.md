# Explanation

## Action Creators

- Functions that return action object
- [Thunks](Thunks.md) are used for asynchronous operations inside action creators

```js
// ⭐ Action Creator
const deposit = (amount) => ({ type: "account/deposit", payload: amount });
// ❌ Without action creator
// store.dispatch({ type: "account/deposit", payload: 500 });
// ✅ with action creator
store.dispatch(deposit(500));
```

# Sources
