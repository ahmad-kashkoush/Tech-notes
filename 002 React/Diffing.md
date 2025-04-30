- An algorithm based on 2 Assumptions
    - Different element types Produce different Trees
    - No re-render for elements with stable Key ([[Key Prop]] didn't change)
- Changing Position leads to re-render
	- Considered element change at that position
- Changing [[Key Prop]] leads to full re-render
- Changing [[props]] leads to mutation
    ![[Diffing Slide.png]]
# Source
Udemy React| Jonas | section 11 | How diffing works