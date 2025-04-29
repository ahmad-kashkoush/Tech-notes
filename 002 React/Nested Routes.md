- Allows components to render inside their parents while maintining URL hirarchy
    - e.g. [[Nested route example.png]]
- Parent comp Wraps child routes
- Configured by adding nested route element (code: [[#Configuration]])
- Rendered by including <Outlet /> in parent (code: [[#Parent setup]])
- Served as default by adding **Index**

# Configuration
```js
// Main router file
<Routes>
  <Route 
	  path="parent" 
	  element={<Parent />}
  >
  // Nested default child route
	    <Route 
		    index 
		    element={<DefaultChild />} 
		/>   
	// Regular nested route: 
	// URL: /parent/child1
	    <Route 
		    path="child1" 
		    element={<Child1 />} 
		/>    // 
	</Route>
</Routes>
```

# Parent setup
```js
function Parent() {
  return (
    <div className="parent">
      <h2>Parent Layout</h2>
      <Outlet />  
      {/* This renders the nested child components */}
    </div>
  );
}
```