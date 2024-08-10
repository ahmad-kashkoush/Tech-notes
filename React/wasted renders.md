# Explanation

Keep in mind that re-render doesn't mean change in the dom, but mean that _component function get recalled_

## Component Re-render when

- Parent re-render
- context change
- state change

> [!note] Important
> Component doesn't re-render on _prop-change_ because of prop-change, but because of parent state change that cause _parent re-render_

## Wasted Render

- It is re-rendering a component without any Change in the dom
- Solutions or Tricks to avoid it
    - [passing component, to avoid re-render](passing%20component,%20to%20avoid%20re-render.md)
