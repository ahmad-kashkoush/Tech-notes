```js
// create action creator with createAsyncThunk
export const fetchAddress = createAsyncThunk('user/fetchAddress', async () => {
  // action creator logic
}
)
const userSlice = createSlice({
  name: 'user',
  initialState: initalState,
  reducers: {
    updateName(state, action) {
      state.username = action.payload;
    },
 },
  // Connect reducer with thunk here
  // add builder cases
  extraReducers: (builder) => builder.addCase(fetchAddress.pending, (state) => {
    state.status = 'loading'
  }).addCase(fetchAddress.fulfilled, (state, action) => {
    state.status = 'idle';
    state.position = action.payload.position,
      state.address = action.payload.address;
  }).addCase(fetchAddress.rejected, (state, action) => {
    state.status = 'Error';
    state.error = action.error.message;
  })

});
```
