- Holds Ref object (Mutable object)
- Ref obj doesn't reset across renders (same memory reference and value)
- Used for
    - Selecting/Keeping Dom nodes
    - Persistent variables
	    - Stay the same across renders
	    - e.g. timer IDs, previous values
- Not used in render logic (Check: [[React  Logic]]).

![[Refs vs State.png]]

# Sources

- udemy React Jonas| section 13| useRef Intro
