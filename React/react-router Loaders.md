# Explanation

- Used to fetch data

## What do I want?

- Fetching data from API on routing
- Use render as a fetch strategy

## Steps

1. Create a loader 2. a function fetchs api data
2. Provide/Connect loader to route

```js
 {
	 element: <Element/>,
	 path:"/",
	 loader:loader
  },
```

1. Fetch data into component : `useLoaderData()`

# Source

- react jonas|section 21| "Fetching data with react-router"
