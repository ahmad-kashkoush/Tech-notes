# Blocking waterfall
- Waiting of multiple data pieces to be fetched (in sequence).
- waiting time will be summed (fucks performance)  ![[Pasted image 20240902161239.png]]
# Promise.all()
- awaits will run in parallel
- waiting time == slowest promise (better performance) ![[Pasted image 20240902162529.png]]
# Isolating promises
- Finished promise is displayed independently
- [[SC]] will be
	- Isolated with its fetching logic
	- Wrapped with [[Suspense component]]
- Best perofmrance