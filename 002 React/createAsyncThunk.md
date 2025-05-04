# Explanation
- Function that accepts
	1. Action name
	2. async function: Contains [[Thunks]] logic
1. returns [[Promises]] (Pending, Rejected, Fullifilled).
2. How
	1. Assign [[Action Creators]] logic to createAyncThunk (Code: [[#Assigning Thunk logic]])
	2. Connect it with slice (using _extraReducers_) (Code: [[#Slice Connect]])
	3. Add Status Logic(pending, fullfilled, rejected) (code: [[#Status Logic]])
## Assigning Thunk logic
```js
// create action creator with createAsyncThunk
export const fetchAddress = createAsyncThunk('user/fetchAddress', async () => {
  // action creator logic
}
)
```
## Slice Connect
```jsx
const userSlice = createSlice({
  name: 'user',
  initialState: initalState,
  reducers: {
    updateName(state, action) {
      state.username = action.payload;
    },
 },

  // Connect reducer with thunk here

  extraReducers: (builder) => 
		// ![[#Status Logic]]
});
```
## Status Logic
- add builder cases
```jsx
builder.addCase(fetchAddress.pending, (state) => {
    state.status = 'loading'
  }).addCase(fetchAddress.fulfilled, (state, action) => {
    state.status = 'idle';
    state.position = action.payload.position,
      state.address = action.payload.address;
  }).addCase(fetchAddress.rejected, (state, action) => {
    state.status = 'Error';
    state.error = action.error.message;
  })
```
