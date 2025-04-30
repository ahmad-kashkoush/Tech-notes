- A compositional React pattern
- Parent dynamically decides what to render based on **Render function**
- Render function: 
	- passed as prop
	- returns JSX element
- Delegates rendering to parent
    - Ensures Reusability:
	    - Logic decoupled from UI
	- Ensures Flexibility:
		- Same component with multiple UIs
    - Polymorphismic: like in OOP
- [[#Code Example]] 
# Code Example
```jsx
<DataFetcher url="/api/data">
  {(data, error) => (  // ← Render function (passed as prop)
    error 
      ? <Error message={error} /> 
      : <DataList items={data} />  // ← Parent decides JSX
  )}
</DataFetcher>
```
# Sources

- [Render Props chatgpt](https://chatgpt.com/share/6dc48293-74e5-48e1-ab28-b36c48e36067)
