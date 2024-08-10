# Explanation

- We broadcast state from [Redux](Redux.md) store to react using _Provider_ component

```jsx
 <React.StrictMode>
 // Connect to store
    <Provider store={store}>
      <App />
    </Provider>
  </React.StrictMode>
```

- Then in each component we use _useSelector_ to create a subscribtion to the store

```jsx
function Customer() {
//
  const customer=useSelector((store)=>store.customer);
  console.log(customer);
  return <h2>👋 Welcome, {customer.fullName}</h2>;
}
```

# Sources
