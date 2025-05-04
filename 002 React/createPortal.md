# Explanation
- Allow changing component place in the dom tree.
1. Why Placing comps in dom tree matters?
	1. Comp css style is affected by its dom parent (e.g. Inheritence, overflow)
	2. Ensures component reusability
```jsx
return createPortal(
		<> {/* jsx */} </>
		, selectedParentInDom
	);
)```
# Sources
