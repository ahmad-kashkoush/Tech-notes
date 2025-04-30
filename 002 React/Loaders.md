- Used for
	- Fetching data from API on routing
	- Using render as a fetch strategy
- How to create Loaders
	1. Create a loader 
	2. Create a function fetchs api data
	3. [[#Connect loader to route]]
	4. Fetch data in component
		- `useLoaderData()`
# Connect loader to route
```js
// Connect loader to route
 {
	 element: <Element/>,
	 path:"/",
	 loader:loader
  },
```
# Source

- react jonas|section 21| "Fetching data with react-router"
