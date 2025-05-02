# Explanation
- Re-render component without dom change
1. Re-render 
	1. recalling component function (Not Update the dom)
	2. Happens on context change, state change, parent re-render.
2. Avoid Wasted renders we should
	1. Pass the slow comp as child  if it doesn't need current comp state  (Prevent render on current state change)
	2. Check [[#Code before]], [[#Code After]]

# Code before
- SlowComponent renders without needing count state
```js
export default function Test() {
 const [count, setCount] = useState(0);
  return (
    <>
	    <button 
		    onClick={() =>(
		     setCount((c) => c + 1)
	     )}>
			Increase: {count}
    </button>
    <SlowComponent /> // Wasted Render
  </>
  );
  }
```

# Code After
- Passed `SlowComponent` as child
- Isolated Counter and its state (To re-render alone).
```js
function Counter({ children }) {
  const [count, setCount] = useState(0);
  return <>
    <button 
	    onClick={() => ( 
	    setCount((c) => c + 1)
	    )}>
		    Increase: {count}
	</button>
    {children} // passed slowComponent
  </>

}

export default function Test() {
  return (
    <Counter>
      <SlowComponent /> // No-re-render
    </Counter>

  );
}

```

# Sources
