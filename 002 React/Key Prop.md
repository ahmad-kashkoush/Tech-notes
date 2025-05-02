# Explanation
- A special Prop to acknowledge element's uniqueness to the [[Diffing]] Algorithm.
1. Used:
    1. on Item change: target only changed 
        - Saves renders (Instead of rendering entire list).
	2. To Reset [[component Instance]] [[State]].
		- By changing the Key prop
2. Key generation tips
    1. Generate from Data itself
    2. Don't generate on the fly
# Source
