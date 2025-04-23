<!-- Don't know Image purpose yet ![[Pasted image 20240819143556.png|500]] -->

- Data structure Contains
	1. [[Virtual Dom]] of [[SC]]
	2. CC
- RSC Payload describes UI as data
- Why RSC Payload? not HTML?
    1. Because of ability to apply [[Reconciliation]], [[Diffing]] with [[Fiber Tree]] on [[SC]] rerenders
		- check [[How Components are Displayed on Screen]]
    2. HTML leads to loss of current UI state
	    - because of generating new page
