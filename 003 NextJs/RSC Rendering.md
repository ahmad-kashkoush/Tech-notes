- CC: client component
- Rendering steps don't work sequencial
- Completed render will be Streamed
1. [[#SC rendered to react elements]]
2. A Holes reserverd for CC Includes:
    - serialized Props (SC->CC)
    - URL to component code script
3. [[RSC Payload]] (generated from past 2 steps) will be sent to client
4. CC rendered to React Elementes

# [[SC]] rendered to react elements
- contains Dom info
- Not necessary code for rendering
- code must be serilazable 
	- to be sent to client later
	- This is the reason for not sending functions
- ![[Rendering SC->react elements.png]]