# Explanation
When calling Constructors
	- new Empty Object is created
	- `this` refers to this empty Object
	- return object linked to [Prototype](Prototypes.md) of constructor
- Don't Create methods inside constructors
	- lead to method duplication (method is an object) which fucks memory
	- Instead attach it to Prototype
# Sources
- Extends [](OOP%20In%20JS.md#sources)