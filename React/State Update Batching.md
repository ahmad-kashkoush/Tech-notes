# Explanation

- Batch Multiple State Updates from [useState](useState.md)
- [Render + Commit](How%20Components%20are%20Displayed%20on%20Screen.md) the Batched Single Time
- That's why If console.log(State) After setState you won't find it Updated
    - Because It [Fiber Tree](Fiber%20Tree.md) isn't Updated Yet
