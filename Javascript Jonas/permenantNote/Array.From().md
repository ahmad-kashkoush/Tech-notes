- A method that creates a shallow copy of an interable

## Example

```js
// Use Array.From Instead of normal For LOOP:star

Array.from({ length: maxRating }, (_, i) => {
	return <Star key={i} />;
});
```

# Source

- [Mdn Link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from)
