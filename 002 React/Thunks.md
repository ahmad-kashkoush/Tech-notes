# Explanation
- A [[Redux Middleware.png]]
1. _Redux Middleware_: Code runs
   2. After dispatch function
   3. before going to the reducer
- [[Redux Toolkit]] has a modern way of creating thunks [[createAsyncThunk]]
1. Used for update [[State]] from an API call (Check [[#Solutions comparison]])
2. How to create? (Code: [[#Creation steps]]).
# Solutions comparison
- Scenario is Updating state from An API call
1. Where to fetch data?

|            | Possible    | Steps                                                             | Why?                                                              |
| ---------- | ----------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| Reducer    | No          | --                                                                | Reducers are pure                                                 |
| Component  | Not optimal | 1. Fetch data with [[useEffect]]<br>2. Update state with Dispatch | 1. Components Must Be clean<br>2. Must encapsulate fetching Logic |
| Middleware | Yes         |                                                                   | 1. Solves Comp/Reducer Problems                                   |

# Creation Steps
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

# Source

