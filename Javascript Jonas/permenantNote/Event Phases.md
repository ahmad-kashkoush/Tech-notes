# Explanation

## Phases

![Capturing, Bubbling](Capturing,%20Bubbling.png)

1. _Capturing Phase_: event Travels from root Dom to target element
    - Make use of it by using [Event Delegation](Event%20Delegation.md)
    - `document.addEventListener(event, callback, useCapture:boolean`
1. _Target Phase_: apply callback
1. _Bubling Phase_: event travels to parent element back
    - events are executed in this phase by default
    - [Event Propagation](Event%20Propagation.md)

## Note

- callback functions are applied to each parent element has the event
- Stopped by `e.stopPropogation()`

# Sources
