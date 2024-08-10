# Explanation

- Write, Mutate data
- not read like [react-router Loaders](react-router%20Loaders.md)

## How

### Create `<Form></Form>`

- A react-router element
- its action need a route `action="/order/new"`
- if you don't add action route then it will submit to closest route
- _onSubmit_: form submits a request passed as an argument to action function

### create action function that contains _POST_ code:

1. get request
2. customize or derive object from request
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

### connect router with action

# Sources
