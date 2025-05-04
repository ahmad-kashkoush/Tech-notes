# Explanation
- A Redux Middleware
1. _Redux Middleware_: Code runs
	1. After dispatch function 
	2. before going to the reducer
- [[Redux Toolkit]] has a modern way of creating thunks [[RTK Thunk]]
- aka Thunk
    ![[Redux Middleware.png]]

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
