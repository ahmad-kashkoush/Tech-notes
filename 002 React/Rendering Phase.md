- Internal Process, has no relation with displaying DOM.
- An [[Asynchronous]] operation
	- Rendering can be split, paused, prioritized.
	- Enables Concurrency e.g. [[Suspense component]]
1. Create new [[React element]] 
2. New [[Virtual Dom]] created by React Element
3. Create Updated [[Fiber Tree]]
	- By Appling [[Reconciliation]] + [[Diffing]]
		- On new Virtual Dom
		- With current Fiber tree (Before update)
- ![[Rendering Phase.png]]
# Source
- Udemy React Jonas| Section 11| The rendering phase