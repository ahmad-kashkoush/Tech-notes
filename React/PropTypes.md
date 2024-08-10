# Explanation

- Used to validate types of props to avoid silly Mistakes

## Implementation

```js
//  You can add Prob types, to specify what types for each prob
StarRating.propTypes = {
    maxRating: ProbTypes.number,
    size: ProbTypes.number,
    defaultRating: ProbTypes.number

}
export default function StarRating({
    maxRating = 5,
    color = '#fcc419',
    size = 48,
    defaultRating = 3,

}) {
```

# Sources

- Udemy-React Jonas- Section 10 : Prob types
