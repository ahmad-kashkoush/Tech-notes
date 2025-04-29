- Used for Writing and mutating data
- Not used for reading like [[Loaders]]
- How to create Actions
	1. [[#Create `<Form></Form>`]]
	2. [[#Create Action Function]]
	3. [[#connect router with action]]

# Create `<Form></Form>`
- A React router element with action route
- action route submits to closest route if not provided.
- Form submits  request passed as an argument to action function
# Create Action Function
- A Function with POST code
1. Get request using formData
2. Customize or derive request Object
3. create, mutate data with new object created
4. store response if you want its id

```js
export async function action({ request }) {
  // get request
  const formData = await request.formData();
  // customize request object
  const data = Object.fromEntries(formData);
  const order = {
    ...data,
    priority: data.priority === 'on',
    cart: data.cart ? JSON.parse(data.cart) : [],
  };
  //  mutate, write data
  const res = await createOrder(order);
  //
  return redirect(`/order/${res.id}`);
}
```

# Connect router with action

# Sources
