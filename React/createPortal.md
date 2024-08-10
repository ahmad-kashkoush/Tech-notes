- by default component is placed in dom tree like it is in component tree
- createPortal is a method used to customize that

```jsx
return createPortal(
		<> {/* jsx */} </>
		, selectedParentInDom
	);
)
```

## Why do I need that?

Let's say I have a _modal window_ used different places and inside different component parents

- If I don't use _createPortal_
    - modal will get affected by its parent css style
        - either by _inheritence_
        - or by _overflow_ which may make pieces from it hidden
- if I use _createPortal_
    - I can put it inside any component parent comfortably
    - change its place in dom tree to avoid style issues
    - insure component reusability
