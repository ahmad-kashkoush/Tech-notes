# Explanation

- automatically add middleware and redux extension

## Before

```js
const rootReducer = combineReducers({
  account: accountReducer,
  customer: customerReducer,
});
const store = createStore(rootReducer,
  composeWithDevTools(
    applyMiddleware(thunk))
)
```

## After

```js
const store = configureStore({
  reducer: {
    accountReducer,
    customerReducer
  }
})
```
