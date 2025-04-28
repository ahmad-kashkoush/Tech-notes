- A function, executed in two ocasions:
    -  Before [[useEffect]] execution
    -  After componenet has unmounted
- Cleanup Is necessary to
    - Prevent side effect from occuring on re-rendering, or mounting.
    - Prevent multiple request overlab
	    - Leading to [[Race Condition]]
		- By Cancelling previous requests 
		- [[#Requests with/without cleanup]]
    - prevent _accumulative event Listener_ 
        - By removing the events on unmount and re-render
# Requests with/without cleanup
- Without cleanup request overlab ![[before clean up function.png]]
- With Cleanup function
	- Cancelled all requests before accepting request(The target)
	- ![[after cleanup function.png]]
# Potential Cleanup

![[potential cleanup.png]]