# Explanation
- Decisions about [[State]] metadata
1. When to create a state (Or just Derive)
2. [[Types of state.png]] 
	1. **Local**: Data related to its comp & Childs (if Passing props).
	2. **Global**: shared among all components
		- using [[Redux]], [[Context API]]
	3. **Remote**: 
		- [[Asynchronous]] Data fetched from API
		- Needs Update/Re-fetching
	4. **UI**
	- [[state management tools.png]]
3. State Home: Where to place state piece
	- [[State placement table.png]]
4. How state flows through the app
	- Is one way data-flow (parent->child)?
	- Is child->parent communication?
	- Is it global State?
5. Decide State Management lib to use:
	- [[Context API]], [[Redux]], and [[React query]]
- ![[State flowchart - When & Where to create.png]]

# Sources

- Udemy React Jonas| Section 7| State fundamentals
- Udemy React Jonas | Section 18 | Thinking in React: Advanced state management
