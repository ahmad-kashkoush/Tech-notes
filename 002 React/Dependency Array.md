- Dependency array change triggers [[Hooks]] execution (Executed [[Asynchronously]]).
- Synchronize _state_ with _side effects_![[Pasted image 20240304133716.png]]
- Determines when [[useEffect]] executed:![[Pasted image 20240304132925.png]]
- [[#How to use]]
- Rendering Phase
	1. mount->commit->browser paint
	2. effect: Rerender on state change
## How to use
1. Include the following values:
	1. [[props]]
	2. state variables
	3. contexts  
	4. Reactive Values
		- References probs, states, and contexts
2. No Objects & Arrays are included
	- `{}!=={}`: same value different obj
3. Remove unnecessary deps:![[Rules to Remove unnecessary dependencies.png]]
