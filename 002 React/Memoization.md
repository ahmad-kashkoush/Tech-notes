# Explanation
-  Illustration: [[memoization proccess.png]]
- Optimization Technique for caching results of arguments
1. Calling function with same arguments return pre-computed results in cache
	- Optimize performance
2. Trade-offs between memory and time
- and application on memoization is
	-  [[#Memo]]
	- [[#useMemo]]
	- [[#useCallback]]
## Memo
- No re-render for same context/prop 
1. Memoizes componenets
2. used for
	1. heavy components
	2. Frequently rendered comps (With same props)
3. Won't work for object prop
	1. Same value, different obj
	   `{}!=={}`
## useMemo
1. Memoizes Callback result (Different from [[#useCallback]])
2. Used to avoid prop change on same value (i.e. prop objects)
3. Object value changes based on [[Dependency Array]] 
4. useMemo Example
	- Object will be created on first re-render, and  wont change again.
```javascript
  const archiveOptions = useMemo(() => {
    return {
      show: false,
      title: "Archieve Posts"
    }
  }, []);
```
## useCallback
1. Memoized callback (Same as [[#useMemo]])
# sources

- section 19| react| jonas|
