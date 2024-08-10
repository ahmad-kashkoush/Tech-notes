# Explanation

- Thunk is a Redux Middleware
- _Redux Middleware_: code runs after dispatch function but before going to the reducer
- [Redux Toolkit](Redux%20Toolkit.md) has a modern way of creating thunks [RTK Thunk](RTK%20Thunk.md)
- aka Thunk
    ![Redux Middleware](Redux%20Middleware.png)

## Scenario

- Say we have to update State from an API call
- where should we fetch data?

### Solution 1: in Reducer

- Not a valid Solution you can't do it
- reducers are a pure functions & don't produce sideffects

### Solution 2: in component

- we fetch data using useEffect inside a component
- then we update state with dispatch
- Why not valid
    - not ideal
    - components must be as clean as possible
    - fetching logic must _encapsulated somewhere_

### Solution 3: in Middleware

- perfection solution for asynchronous code
- Steps

    1.  apply middleware thunk into your store
    2.  return function that returns a dispatch

    ```jsx
 export const deposit = (amount, currency) => {
      if (currency === "USD")
	       return { type: "account/deposit", payload: amount }; 
   return async function (dispatch, getState) {
     // api call
     const host = 'api.frankfurter.app';
     const res = await fetch(`https://${host}/latest?amount=${amount}&from=${currency}&to=USD`)
    const data = await res.json()
    const converted = data.rates.USD;
    // action
    console.log(converted);
    dispatch({ type: "account/deposit", payload: converted });
    }
    }
    ```

# Sources
