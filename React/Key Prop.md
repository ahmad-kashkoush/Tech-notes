# Explanation

- Definition: special Prop to tell [Diffing](Diffing.md) Algorithm that the element is Unique
- We need key:
    - on Item change: we can target only changed item and re-render it
        - this better than rerendering the entire list
- I Can Change key If I want Reset State of a component Instance
- key generation best Practice
    - to be from data itself
    - not generated on the fly
