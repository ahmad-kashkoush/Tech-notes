1. Called top level, not inside blooks
	- [[#Why Only on top Level]]
2. Called in _React functions_, Not in regular functions, class components
# Why Only on top Level
- To ensure being called in same order 
- Hooks are stored using Linked list (in [[Fiber Tree]])
	- Random order leads to losing next hook pointer.
- ![[Linked list of hooks.png]]
-
