## memo

- used for memoizing _components_
- component wont re-render if its context or prop changes
- used for
    - heavy components
    - components that re-renders often with same props
- remember trade-offs between memory and time

### A Problem in Use memo

If you pass a prop as an object, it won't be memoized because objects with same values are different actually 😂

```js
({}==={})// return false :
```

- Solution is here is to memoize object using useMemo to memoize values

## useMemo

- similar to [useEffect](useEffect.md)
- changes object value depending on dependency array
- Used to avoid prop changing when its value is the same
- Memoizes the result of callback which is different from useCallback

### useMemo Example

- archieveOptions Object will be changed on every render
- which will waste the use of **memo** component that avoid rendering on same props

```js
  const archiveOptions = {
    show: false,
    title: "Archieve Posts"
   }
```

- the solution is to memoize the object using useMemo
- it will only be created on first re-render, object itself wont change again

```javascript
  const archiveOptions = useMemo(() => {
    return {
      show: false,
      title: "Archieve Posts"
    }
  }, []);
```

## useCallback

- simialr to [#useMemo](#useMemo) but it memoizes the callback
