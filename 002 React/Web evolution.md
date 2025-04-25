1. Server-side Rendering
	- Server is requested by client
	- Server code painted by browser on screen
	- **Issue**: No UI/[[State]] syncing
		- Server data !== displayed data
		- Needs re-requesting server (by page reloading).
2. [[#Single Page & client rendering]]
- Why Use Frameworks?
    - Abstracts UI/[[State]] syncing (Leading clean structured code).
# Single Page & client rendering
- [[Front End Application Job.png]]
- A solution for UI/State syncing
- Pages are rendered on client (No page reloading)
- UI/State syncing is hard with JS
	- Lots of DOM manipulation (Spagitti code).
	- State is shared across the whole app, leading to [[Race Condition]].
# Sources
- Udemy |Jonas-Section3| Why Frameworks exist
