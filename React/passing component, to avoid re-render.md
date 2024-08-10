
- If a component doesn't need a state will be re-rendered, pass it as a child or a prob
    1.  This way It will be re-render on parent re-render, not current component state change

```js
export default function Test() {
 const [count, setCount] = useState(0);
  return (
    <div>
    <h1>Slow counter?!?</h1>
    <button onClick={() => setCount((c) => c + 1)}>Increase: {count}</button>
    <SlowComponent /> // 🏆 will be re-rendered without needing count state
  </div>
  );
  }
```

### Solution

```js
function Counter({ children }) {
  const [count, setCount] = useState(0);
  return <div>
    <h1>Slow counter?!?</h1>
    <button onClick={() => setCount((c) => c + 1)}>Increase: {count}</button>
    {children} // already exists from parent
  </div>

}

export default function Test() {
  return (
    <Counter>
      <SlowComponent /> // won't re-render
    </Counter>

  );
}

```
