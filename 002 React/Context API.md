# Explanation
- React feature, enables direct data share from parent to any nested child.
1. `useContext`: give access to data provided by parent `context.Provider`.
2. Avoid manual passing props to unrelated middle compoenents 
	- Solve [[Prop Drilling Issue]]
	- ![[ContextAPI providing.png]]
3. Factors
	1. **Provider**: global value broadcaster
	2. **Value**: Accessed through app
	3. **Consumer**: 
		1. Any component that subscribes to context value.
		2. re-rendered on value update