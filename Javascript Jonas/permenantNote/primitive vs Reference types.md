# Explanation
- _Primitive types_: Restores the value in stack
- _Reference types_: 
	- Restores reference to address in stack
	- address referers to value in _heap_
	- you can update same value from multiple references to same address which cause _shallow copy Issue_
- Illustration: ![ReferenceVsPrimitiveType 1](ReferenceVsPrimitiveType%201.png)
