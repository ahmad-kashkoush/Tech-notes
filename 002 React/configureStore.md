# Explanation
1. Automaticall adds middleware and redux extension
## Code Before

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

## Code After

```js
const store = configureStore({
  reducer: {
    accountReducer,
    customerReducer
  }
})
```

# Sources
