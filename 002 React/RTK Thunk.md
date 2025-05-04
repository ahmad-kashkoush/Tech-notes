# Explanation

- the [[Redux Toolkit]] approach of creating thunks
- What is createAsyncThunk?
    - function that accepts
        - action name
        - async function contains thunk code or logic
    - returns [[Promises]] with 3 cases
        - pending
        - fullfilled
        - rejected

## Steps

1. create action create
2. assign to it _createAsyncThunk_ with your parameters
3. connect it with slice using _extraReducers_
4. add logic for pending, fullfilled, rejected status
- Check [[createAsyncThunk code]] for better understanding

