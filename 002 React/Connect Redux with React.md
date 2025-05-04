# Explanation
1. [[State]] broadcasted to React using Provider (code: [[#Provider component]])
2. Subscripe to store using _useSelector_ (Code: [[#useSelector]])
## Provider component
```jsx
 <React.StrictMode>
 // Connect to store
    <Provider store={store}>
      <App />
    </Provider>
  </React.StrictMode>
```

# useSelector
```jsx
function Customer() {
//
  const customer=useSelector((store)=>store.customer);
  console.log(customer);
  return <h2>👋 Welcome, {customer.fullName}</h2>;
}
```

# Sources
