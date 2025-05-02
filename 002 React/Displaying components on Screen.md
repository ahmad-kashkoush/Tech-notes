# Explanation
- Illustration: [[Displaying component phases.png]]
1. Trigger a Render
    - By Mounting or re-rendering
2. [[Rendering Phase]]
3. [[#Commit Phase]]
4. Browser Paint
5. Execute Effect ([[useEffect]])
    - Re-render if [[State]] changed
    - Otherwise execute without re-render
    - Illustration ![[Pasted image 20240304134409.png]]
# Commit Phase
- Commits the List of Dom Updates (Using Given Host)
- Differents hosts are responsible for commits 
	- React Dom
	- React Native
	- Remotion, 
	- ... etc
- A Synchronous Operation
	- Never shows partial results