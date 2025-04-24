- Async functions runs only on the server
	- Mutates data (Fetched by [[SC]]) in [[RSC]]
	- Make fullstack app interactive
- [[#Definitions]] 
# Server Actions behind the scenes?
1.  API endpoint is created for server action
2.  POST request is made to its URL on server action call
- A web server is required
	- Because server action is endpiont
-  function itself never reachs client
- [[#Copying endpoint issue]]
- [[#Why Cache revalidastion]]
# Definitions
1. A Standalone file
	- where exported functions are async actions
	- can be imported into any component
2. async function in [[sc]], passed to client
# Copying endpoint issue
 - endpoint can be copied from the browser and used to mutate data.
- Sol: Not allowed Ids should be handled  at the beginning of the server action
